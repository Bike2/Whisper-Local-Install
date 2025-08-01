# Whisper-Local-Install
Whisper helps you transcribe audio to Text Locally on your system

## 1) Install Whisper:
```
pip install -U openai-whisper
```

## 2) install ffmpeg 
```
sudo apt update
sudo apt install ffmpeg
```

## 3) Locate the file directory
## On windows: Lets say the file is save on desktop, use 
```
/mnt/c/Users/YOUR_USERNAME/Desktop
```
## Where "YOUR_USERNAME" is your actual windows username

## To find your Widows username
Open Command prompt, type this code
```
whoami
```
## This should bring out your username.

## 4) Once you have gotten you windows name, Run this Code
/mnt/c/Users/YOUR_USERNAME/Desktop, lets say my windows name is MSI
So the code would be like 
/mnt/c/Users/MSI/Desktop
This would take you to your windows desktop directory on Linux, then press
```
ls
```
This to bring out all the files on your desktop page

## 5) Once you have seen the audio you want to transcribe to text, use this code in that same directory(desktop)
```
whisper "FILE YOU WANT TO TRANSCRIBE" --model medium
```
lets say the file we want to transcribe is Bike audio.mp3

So the code would be like 

whisper "Bike audio.mp3" --model medium

hen you should let it transcribe the audio, once its done, you can see the txt, srt and json file would be save on you window desktop.

