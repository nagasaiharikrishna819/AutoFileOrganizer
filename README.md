# File Organization Script

Automated script for sorting and organizing files based on their types in a specified directory.

## Overview

This Python script utilizes the watchdog library to monitor a source directory for changes and categorizes files into destination directories based on their types, including audio, video, image, and document files. The script handles naming conflicts and logs file movements for reference.

## Features

- Automated file organization.
- Support for various file types (audio, video, image, document).
- Handling of naming conflicts.
- Logging of file movements.

## Setup

It looks like you've provided a set of instructions for setting up and running a Python script using the Watchdog library to automate file organization. I appreciate the detailed steps you've outlined. Here's a more detailed explanation:

### Instructions for Running a Python Script with Watchdog:

1. **Install Python:**
   - Follow the steps outlined in the provided link or refer to the [official Python website](https://www.python.org/downloads/) to download and install Python on your system.
   - To install VS Code follow this link [Youtube Link](https://www.youtube.com/watch?v=cUAK4x_7thA)
2. **Create a Python Script:**
   - Open a text editor and paste the provided Python script into a new file. Save the file with a `.py` extension (e.g., `organize_files.py`).

3. **Specify Source and Destination Paths:**
   - Open the Python script (`organize_files.py`) in a text editor.
   - Replace the placeholder paths for `source_dir`, `dest_dir_sfx`, `dest_dir_music`, etc., with the actual paths relevant to your system.

4. **Install Required Dependencies:**
   - Open a terminal (Command Prompt in Windows or Terminal in macOS).
   - Run the following command to install the required `watchdog` library:
     ```bash
     pip install -r requirements.txt
     ```

5. **Open Terminal in Visual Studio Code:**
   - In Visual Studio Code:
     - **Windows:** Press `Ctrl + ~` to open the integrated terminal.
     - **macOS:** Press `Cmd + \` to open the integrated terminal.

6. **Run the Script:**
   - Navigate to the directory where your Python script is located.
   - Run the following command to execute the script:
     ```bash
     py organize_files.py  # Use "python" instead of "py" on some systems
     ```

   Make sure to replace `organize_files.py` with the actual name of your Python script.

Now, the script will continuously monitor the specified source directory and organize files based on their types into the destination directories.

## To Automate this process
To automate the execution of the provided Python script on your PC, you can set up a scheduled task or use a task scheduler. The steps may vary slightly depending on your operating system. Here are instructions for Windows:

### Windows:

1. **Create a Batch File:**
   - Open a text editor (like Notepad) and create a new text file.
   - Copy and paste the following lines into the file:
     ```batch
     @echo off
     python "C:\path\to\your\script.py"
     ```
   - Replace `"C:\path\to\your\script.py"` with the actual path to your Python script.
   - Save the file with a `.bat` extension (e.g., `run_script.bat`).

2. **Schedule the Task:**
   - Press `Win + R` to open the Run dialog.
   - Type `taskschd.msc` and press Enter to open the Task Scheduler.
   - In the right-hand Actions pane, click on `Create Basic Task...`.
   - Follow the wizard to set up a basic task. Choose a name and description for your task.
   - Choose the trigger (e.g., daily, at logon, etc.).
   - For the action, select `Start a Program`, and browse to the location of your batch file (`run_script.bat`).
   - Complete the wizard, and make sure to check the box for "Open the Properties dialog for this task when I click Finish."

3. **Configure Task Properties:**
   - In the Properties dialog, go to the `General` tab and make sure "Run with highest privileges" is checked.
   - Optionally, you can set additional options like running the task whether the user is logged in or not.
   - Click `OK` to save the changes.

Now, your Python script should be executed automatically based on the schedule you set up.

### Linux/Mac:

1. **Create a Shell Script:**
   - Open a text editor and create a new shell script (e.g., `run_script.sh`).
   - Add the following lines to the script:
     ```bash
     #!/bin/bash
     python3 /path/to/your/script.py
     ```
   - Save the file.

2. **Set Execute Permissions:**
   - Open a terminal and navigate to the directory containing your script.
   - Run the command:
     ```bash
     chmod +x run_script.sh
     ```

3. **Schedule with Cron:**
   - Open the crontab file for editing:
     ```bash
     crontab -e
     ```
   - Add a line to schedule your script (e.g., run the script every day at 3:00 AM):
     ```bash
     0 3 * * * /path/to/your/run_script.sh
     ```
   - Save and exit the editor.

Now, your Python script will be executed automatically based on the schedule you set up with Cron.

Adjust the paths and schedule timings based on your specific requirements. If you encounter issues or need more specific guidance, feel free to ask!
