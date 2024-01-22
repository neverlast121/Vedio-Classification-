# Video Organization Script

This Python script organizes a collection of videos by their duration. It iterates through a specified directory containing video files, calculates the duration of each video, and then creates folders based on the duration. Each folder is named after the duration (in seconds), and the corresponding videos are moved to their respective folders.

## Dependencies

- `cv2`: OpenCV library for computer vision and video processing.
- `os`: Module for interacting with the operating system, including file and directory operations.
- `shutil`: Module for high-level file operations.

## Code Overview

1. **Video Directory:**
   - Define the path to the directory containing the videos (`video_directory`).

2. **Duration Tracking:**
   - Create a dictionary (`videos_by_duration`) to keep track of videos based on their duration.

3. **Video Iteration:**
   - Iterate over the videos in the specified directory.
   - For each video, load it and extract its duration (in seconds).

4. **Dictionary Population:**
   - Add the video file to the dictionary, organized by its duration.
   - If the duration is not already a key in the dictionary, create a new list for that duration.

5. **Folder Creation and Video Movement:**
   - Create a folder for each unique duration (named as '{duration}s').
   - Move the corresponding videos to the newly created folders.

6. **Execution:**
   - Replace 'video directory' with the path to the actual directory containing the video files.
   - Execute the script to organize the videos into folders based on their durations.

## Example
Suppose the script is run on a directory containing the following videos:
- `video1.mp4` (duration: 60 seconds)
- `video2.mp4` (duration: 120 seconds)
- `video3.mp4` (duration: 60 seconds)

After execution, the directory structure will look like this:
|-- 10s
| |-- video1.mp4
| |-- video3.mp4
|-- 20s
| |-- video2.mp4


This organization helps in categorizing and managing videos based on their durations.
