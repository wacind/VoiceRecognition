# VoiceRecognition
An [Event Ghost](http://www.eventghost.org/) plug-in that uses the  [Microsoft Speech API](http://msdn.microsoft.com/en-us/library/hh362873.aspx) to turn voice commands into Event Ghost Events.

WARNING: This is EXPIRIMENTAL
This plugin is derived from Maikhorma's SpeakEasy plugin (https://github.com/maikhorma/SpeakEasy)
What i have added is the ability to configure confidence levels for two sets of words
I have also added a provision for filler words that can help improve accuracy

## Before you begin
If your microphone is not ready for windows to use, the plugin will fail to initialize.

1. Plugin/setup/install your microphone.
2. Open the windows 7 or 8 search and type "Speech Recognition" to find the tool for setting up the microphone and start training.
3. Launch "Windows Speech Recognition".
4. Go AT LEAST as far as where it says "The microphone is ready to use with this computer." You should complete the training for best results, but so far for me just verifying that the mic is setup at least "works".

## Installation instructions

1. Install Event Ghost if you haven't already.
2. Install the MS Speech Platform SDK for your appropriate OS - http://www.microsoft.com/en-us/download/details.aspx?id=27226 
3. Download the plugin by using git's "Download as Zip" feature.
4. Extract zip to your \<Event Ghost Install Dir>\plugins folder. 
5. Launch Event Ghost and add the plugin

## Setup and Tips:
1. When adding words to the configuration, make sure there are no spaces before each phrase

2. I have provided two example eventghost trees. The first one is pretty straight forward
The second one is the example that came with Maikhorma's plugin. It makes use of first identifying a prefix. It may provide better accuracy but in my experience it was much slower

3. The plugin has a 'logging' option that will log out each recognized phrase and what the Speech Engine believes the confidence level is. This should help you determine what confidence levels to use.

4. Go through the Microsoft speach recognition training. You can also add words and phrases to the microsoft voice recognition engine. 


# Credits
* [Simonsays](https://code.google.com/p/simonsays/) - Whoever wrote this script proved to me that it "shouldn't be that hard" so I finally dug in and gave it a try.
* [pyspeech] (https://code.google.com/p/pyspeech/) - Ended up using this as the main driver to start. Saved me a bunch of time due to how much I suck at threading in python.
* [Maikhorma's SpeaskEasy] (https://github.com/maikhorma/SpeakEasy) - This is what I started with. I edited the __init__.py and speech.py files to expand on providing confidence levels
* And of course the whole event ghost team and community. 
