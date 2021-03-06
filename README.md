# Upside-Down


## Summary
Upside Down is a GUI utility which captures the user's picture, analyzes their current emotions and expressions and recommends them entertainment for them to view, based on their current emotional profile.

## How It Works
The application provides a full graphical user interface using the TKinter Python library. In order to capture images using the user's webcam, the program utilizes CV2. After the image is captured, it is uploaded to the Microsoft Azure Cognitive Services Face API, which analyzes the emotions of the person in the image and returns the confidence for each major emotion. The emotional data is then interpreted by our program to determine the mood that the user is most likely feeling at the moment. Given this mood, our program utilizes numerous third-party APIs to return links to content which would correlate with the user's mood. At the moment, the Spotify, Youtube and Giphy APIs are used for returning music, videos and GIFs which line up with the user's mood.

## Usage
### Compilation
The program is dependent on TKinter, pynput, CV2, giphy_client, Spotipy, GoogleAPIClient. It is important that these are installed before the program is run. This can be accomplished by doing:
```
sudo apt-get install python3-tk
sudo apt-get install python-opencv 
sudo apt-get install giphy_client 
sudo pip3 install spotipy 
pip3 install google-api-python-client
```
### Runtime
Run the command "python3 Interface.py" in the Upside-Down directory which will open up the camera. Click on the camera tab then press "s" to take a picture and press "w" to save it. This will close the application then run the same command "python3 Interface.py", this will open up a GUI that will show the results that has links based on the mood the API caught. 
