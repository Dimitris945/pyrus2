# pyrus2
# pyrus
Overview
This Python script creates a full-screen window that overlays the desktop, simulates a virus or malware attack by displaying a sequence of images (likely mimicking a Blue Screen of Death or similar visual effects), plays a sound, and responds to mouse clicks. It leverages several libraries including Tkinter for GUI, PIL for image processing, PyAutoGUI for keyboard/mouse control, winsound for audio, and standard OS modules for file handling.

Features
Opens a full-screen, topmost window covering the entire display.
Takes a screenshot of the desktop background.
Displays a sequence of images (bsod1.png, bsod2.png, etc.) to simulate a visual attack.
Plays a sound asynchronously during the sequence.
Initiates the sequence when the user clicks anywhere on the window.
Simulates minimizing all windows at the start (Win + D).
How It Works
Key Components:
Resource Path Handling (resource_path): Ensures images and sounds load correctly whether running as a script or as a packaged executable.
Image Update Function (updateImg): Loads, resizes, and displays images for specified durations.
Virus Trigger (virus): Starts the sequence of images and sound playback upon mouse click.
Main Window Setup:
Takes a screenshot of the desktop.
Creates a full-screen, topmost Tkinter window.
Sets the desktop screenshot as the background.
Binds mouse clicks to trigger the virus sequence.
Hides the cursor (not implemented explicitly but can be added).
Ensures the window stays above other windows.
Sequence:
Waits briefly, then minimizes all windows (Win + D).
Takes a screenshot of the desktop.
Creates a full-screen window with the desktop as background.
Waits for the user to click on the window.
On click, runs the sequence:
Displays multiple images in succession.
Plays a sound asynchronously.
The program runs indefinitely until closed manually (though closing is disabled in this code).
Usage Instructions
Prerequisites:

Python 3.x installed.
Required libraries:
pyautogui
Pillow
Install missing libraries via pip:

 
pip install pyautogui pillow
Place Resources:

bsod1.png, bsod2.png, ..., sound.wav in the same directory as the script.
Ensure all images are properly named and present.
Run the Script:

 
python your_script_name.py
Interact:

Click anywhere on the full-screen window to trigger the sequence.
Notes & Warnings
The script disables the close button (win.protocol("WM_DELETE_WINDOW", disable())), so it cannot be closed normally.
It minimizes all windows at startup, which may disrupt user activity.
The visual and sound effects are designed for prank or educational purposes; use responsibly.
To exit, you might need to terminate the process from the task manager.
Customization
Change the sequence images or sound by replacing the files.
Adjust durations in updateImg() calls to speed up or slow down the sequence.
Add features like hiding the cursor, disabling keyboard inputs, or restoring windows for enhanced effects.
Disclaimer
Use this script responsibly. It is intended for entertainment or educational demonstrations. Do not run it on systems where unintended disruptions could cause issues.

License
This is an example script; ensure you have permission to run such scripts on your system.
