# accumulated-memory-landscapes

###Description

Accumulated-Memory-Landscapes is Inspired by Jim Campbell's “Accumulated Psycho”, a piece which collects and interprets by averaging the monolith of cultural memory stored in Hitchcock's film “Psycho” as specific, precise data, transforming it, staging it in present experience; a transformation which devours memory, erasing its perceptual vividness by literally overwriting it with fuzzy averages - condensations of computational memory. Accumulated-Memory-Landscapes, as a conceptual process, explores how technology can mediate and enhance human memory as a process; expanding the possibilities of interaction, experiencing and sharing of these packages of information. This project, rethinks the 3 main steps involved in human memory (Encoding → Storage → Retrieval) by finding parallels between the biological human process and the technological devices and algorithms used for capturing, storing and recalling data. Using a custom-made electroencephalogram (EEG) with an embedded camera and internet access we have built a wearable device able to measure attention levels (proven to be responsible in many ways for memory capturing and retrieval) and alpha-waves patterns (used to measure visual cortex activity) of a user, in any given moment. The device records significant moments of the wearer, in the form of image sequences, which are sent in real-time to a server that algorithmically processes these. The result is an immersive 3D procedural landscape built from these memories; a space where the wearer and any other individual can experience and share (as in the model of a social network) these accumulated memories in more spacial ways.

###IMPORTANT NOTES:

1. The server has been sucssesfully tested on ubuntu-mate 15.04. 
2. The Front end runs smoothly on latest versions of chrome and firefox. 
3. The mobile App tested on Android 4.4.4. 

###Dependencies

1. Requirements on the server side:

  a) ImageMagick NEEDS to be installed on the server [INSTALLATION](https://help.ubuntu.com/community/ImageMagick)

  b) NodeJs and Npm [INSTALLATION](https://nodejs.org/en/)

  c) Google-Chrome or Firefox


2. Processing 3.0 [PROCESSING](https://processing.org/) and processing-android mode. Please follow intructions to install Android Developer Tools at [Android Mode](https://github.com/processing/processing-android/wiki)

3. Ketai library for processing [DOWNLOAD](http://ketai.org/)

4. Android Phone with Developer Tools enabled. The activation of these tools varies from phone o phone.

5. Bluetooth EEG (I'm using Neurosky's Mindwave Mobile for the first prototype). Any thinkgear enabled EEG system should work fine with this project, as long as it is compatible with the thinkgear socket protocol.

###Installation

__1. Server:__

  a) Make sure you have installed NodeJS and Npm on the server you will be using.

  b) Clone this repository:

	git clone https://github.com/fitosegrera/accumulated-memory-landscapes.git

  c) cd into the server directory and install node packages:

	cd server
	sudo npm install

__2. Mobile App:__

  a) After installing Android Developer Tools and Processing on your computer, open processing and make sure in is in android-mode.

  b) Connect your phone to the computer via USB (remember to activate developper options)

  c) If all is right; you should see your phone's name under the processing menu>android>device. If so run your App and it should appear a blanck screen on your phone after a few seconds. This means everything worked well!

###Running the whole thing

1. On your server cd into the accumulated-memory-landscapes/server and run it:
	cd /YOUR/PATH/accumulated-memory-landscapes/server
	node server.js

__Note:__ If you want persistence and chrash-proof you should install forever on your server [FOREVERJS](https://github.com/foreverjs/forever). Also make sure your server (if it is a remote one) has domains and ports available for public access.

2. Power your brain scanner (thinkgear) and pair it with your phone via bluetooth.

3. On your laptop: connect your phone, open the processing sketch located at phoneApp/AML and compile it from the processing IDE. You should now have the app running on your phone.

4. Finally, open a web browser like chrome or firefox and go to your server url on port 3000. For example if you are running the server locally:

	http://localhost:3000

If you are running it remotely you should use your Global IP address or domain name (in case you have one):

	43.565.763.23:3000
	http://my.domain.com:3000

You should now see the landscape rendered on your browser based on your brain data and captured imagery and sound.
