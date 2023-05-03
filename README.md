# Video-Classification-
Create a folder for each unique duration and move the corresponding videos to the folder

This Python code iterates over a directory of video files and groups them based on their duration. It then creates a folder for each unique duration and moves the corresponding videos to the folder. 

The code uses the `os` module to list all files in the specified directory and filter out files that do not end with the `.mp4` extension. It then loads each video file using OpenCV's `cv2.VideoCapture()` method and extracts its duration using the video capture object's `get()` method. The duration is computed as the total number of frames in the video divided by the frames per second. 

Next, the video file path is added to a dictionary that maps each duration to a list of video paths with that duration. If a duration is not already in the dictionary, a new empty list is created for it. 

Finally, the code loops over the dictionary items and creates a folder for each unique duration using the `os.makedirs()` method. It then moves the corresponding videos to their respective folders using the `shutil.move()` method. The `exist_ok=True` parameter is used to avoid raising an error if the folder already exist.
