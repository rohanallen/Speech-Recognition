# Speech-Recognition
Speech Recognition programs in Python capable of recognizing speech from short files, large files and also from your microphone input and convert them into text.

pip3 install SpeechRecognition pydub
To execute

short speech
python3 simple_speech_recognizer.py simple.wav

long speech
 python3 speech_recognizer.py long_speech.wav

microphone input from computer
python3 live.py 10 (time in sec)

Description:

the first program (simple_speech_recognizer.py) takes a very short speech sample (simple.wav) and recognizes what is being said and converts it to text. pass the test sound file as an argument.
we need to import the speech_recognition module to get sound recognition functionalities. then we load the sound file and record it. then recognise it using google's ml algo and convert it to text.
Works best for extremely small speech files. Preferably less than 5 or 10 seconds.
WE can use ibm watson,wit,houndify,etc for better accuracy but that also requires getting valid credentials which you can do by making an account.

The second program (speech_recognizer.py) deals with longer speech files and converts it to text. there is a function which splits the speech files
into chunks using a min silence interval in milliseconds. This is adjustable as per the audio file requirement. then it is converted to text chunk
by chunk. So, this function automatically creates a folder for us and puts the chunks of the original audio file we specified, and then it runs speech recognition on all of them.

the third program live.py recognizes speech from your microphone input and converts it to text. You can pass a time in seconds as an argument
when running the program. This specifies for how long the programs will run and identify your speech.
