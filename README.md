FFmpeg Web UI
A simple, self-hosted web interface for FFmpeg that allows you to convert audio files by dragging and dropping them into your browser. This project provides a user-friendly GUI to control common audio conversion settings without needing to use the command line directly.

Features
Easy to Use: Drag-and-drop your audio files right into the browser.

Full Control: Adjust format, bitrate, sample rate, and channels.

Real-time Progress: See the file upload progress before conversion.

Self-Hosted: Runs entirely on your local machine for privacy and speed.

One-Click Setup: Includes batch scripts to install all dependencies and run the application.

Learn FFmpeg: Shows the exact FFmpeg command being used for the conversion.

How It Works
This project consists of two main parts:

Front-End (index.html): A user-friendly HTML page with JavaScript that you interact with in your browser. It sends the file and your chosen settings to the back-end.

Back-End (server.py): A lightweight Python Flask server that receives the data from the front-end. It then uses Python's subprocess module to execute the ffmpeg command-line tool with the specified options and sends the converted file back to your browser for download.

Getting Started
Follow these steps to get the application running on your Windows machine.

1. Download the Project Files
Clone or download this repository to a folder on your computer. You should have the following files:

FFmpegOneClickInstaller.bat

launchFFmpegUI.bat

server.py

index.html

2. Install Dependencies
You only need to do this once.

Right-click on FFmpegOneClickInstaller.bat and select "Run as administrator".

This script will automatically install Chocolatey (a package manager), Python, and FFmpeg, as well as the necessary Python libraries (Flask and Flask-CORS).

3. Run the Application
Simply double-click launchFFmpegUI.bat.

This will automatically:

Start the Python server in a new command prompt window.

Open the converter interface (index.html) in your default web browser.

You are now ready to convert files!

Project Structure
.
├── FFmpegOneClickInstaller.bat  # All-in-one installer for required software.
├── launchFFmpegUI.bat           # One-click script to launch the server and UI.
├── server.py                    # The Python Flask server that runs FFmpeg.
└── index.html                   # The front-end web interface you interact with.

Prerequisites
The FFmpegOneClickInstaller.bat script handles these for you, but for manual setup or troubleshooting, you will need:

Python 3

FFmpeg (accessible from your system's PATH)

Flask and Flask-CORS Python libraries (pip install Flask Flask-CORS)

License
This project is licensed under the MIT License - see the LICENSE.md file for details.
