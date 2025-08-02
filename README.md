# Whisper-Local-Install
Whisper is an open-source automatic speech recognition (ASR) system developed by OpenAI. it helps you transcribe audio to Text Locally on your system
This guide helps you install Whisper on any Debian-based Linux distro (like Ubuntu), with optional GPU support via PyTorch.

## ✅ System Requirements

🖥️ Minimum
OS: Ubuntu 20.04+ (or any modern Debian-based distro)
RAM: 8 GB
Disk Space: ~5 GB (to run the model + dependencies)
Python: Python 3.8–3.11

⚡ Recommended (for faster transcription)
GPU: NVIDIA GPU with CUDA support
Drivers: CUDA 11.7+ and cuDNN
VRAM: 6GB+ for medium/large models

## Installation Steps
📦 Install Dependencies
```
sudo apt update
sudo apt install git python3 python3-pip
```

## Set Up Python Environment (Optional but Recommended)
```
python3 -m venv whisper-env
source whisper-env/bin/activate
pip install --upgrade pip
```

## 1) Install Whisper:
```
pip install -U openai-whisper
```

## 2) install ffmpeg 
```
sudo apt update
sudo apt install ffmpeg
```

## 3) Optional) Enable GPU Acceleration
## If you have an NVIDIA GPU, install the PyTorch version with CUDA:
```
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```
Replace cu118 with your CUDA version (cu117, cu121, etc.)

## 4) Locate the file directory
## On windows: Lets say the file is save on desktop, use 
```
cd /mnt/c/Users/YOUR_USERNAME/Desktop
```
## Where "YOUR_USERNAME" is your actual windows username

## To find your Widows username
Open Command prompt, type this code
```
whoami
```
## This should bring out your username.

## 5) Once you have gotten you windows name, Run this Code
/mnt/c/Users/YOUR_USERNAME/Desktop, lets say my windows name is MSI
So the code would be like 
/mnt/c/Users/MSI/Desktop
This would take you to your windows desktop directory on Linux, then enter
```
ls
```
This to bring out all the files on your desktop page

## 6) Once you have seen the audio you want to transcribe to text, use this code in that same directory(desktop)
```
whisper "FILE YOU WANT TO TRANSCRIBE" --model medium
```
lets say the file we want to transcribe is Bike audio.mp3

So the code would be like 

whisper "Bike audio.mp3" --model medium

hen you should let it transcribe the audio, once its done, you can see the txt, srt and json file would be save on you window desktop.

## To Transcribe another audio, just head to the same path the audio is located and run
```
whisper "FILE YOU WANT TO TRANSCRIBE" --model medium
```

