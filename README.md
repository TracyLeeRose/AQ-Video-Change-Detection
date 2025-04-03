# AQ-Video-Change-Detection
Samples 300 frames from video and shows overlay of changed detected

A web-based motion detection tool that analyzes MP4 videos to detect changes between frames, highlighting differences with a translucent red overlay. Built with HTML, CSS, and JavaScript, this application processes up to 300 frames from a user-selected starting point and visualizes motion in an intuitive interface.
Features

Video Upload: Load MP4 videos for analysis.

Frame Selection: Use a slider to choose the starting frame for motion detection.

Motion Detection: Compares up to 300 subsequent frames to the selected start frame, accumulating changes.

Customizable Threshold: Adjust the difference percentage threshold (1-100%) to fine-tune motion sensitivity.

Visual Output: Displays the reference frame with a translucent red overlay (30% alpha) indicating changed pixels.

Progress Tracking: Real-time progress bar during frame extraction and motion detection.

Save Results: Export the result as a PNG image.

Responsive UI: Thumbnail strip for frame previews and a scalable canvas for output.

Usage
Upload a Video:
Click the file input to select an MP4 video.

The video metadata loads, and an initial frame (frame 25) is displayed.

Select Start Frame:
Use the "Start Frame" slider to choose where motion detection begins (0-100% of video duration).

The timestamp updates to reflect the selected position.

Adjust Threshold:
Modify the "Difference % Threshold" slider (default: 15%) to set motion sensitivity.

Detect Motion:
Click "Detect Motion" to extract frames and analyze changes.

Progress is shown via a bar; results appear on the canvas with a red overlay.

Save the Result:
Click "Save Result Image" to download the output as motion_detection_result.png.

Reset:
Click "Reset" to clear the application and start over.

How It Works
Frame Extraction: Extracts up to 300 frames starting from the selected point at an estimated 30 FPS.

Change Detection: Compares each frame to the reference frame, marking pixels with differences above the threshold.

Overlay Rendering: Uses a temporary canvas to apply a 30% alpha red overlay, ensuring proper transparency.

Performance: Asynchronous processing with progress updates to handle large videos efficiently.

Technical Details
Languages: HTML5, CSS3, JavaScript (ES6+)

Key Components:
ImageStack class: Manages frame data and detects pixel changes.

Canvas API: Renders video frames and motion overlays.

Video Element: Handles MP4 playback and frame seeking.

Constants:
NUM_FRAMES_TO_PROCESS: 300

FRAME_RATE_ESTIMATE: 30 FPS

OVERLAY_ALPHA: 0.3 (30% opacity)

CHANGE_COLOR: Red [255, 0, 0, 255]

Limitations
Supports only MP4 video files.

Assumes a constant 30 FPS for frame timing (may vary with actual video frame rates).

Maximum of 300 frames processed to balance performance and memory usage.

Browser-dependent performance for large videos.

Contributing
Fork the repository.

Create a feature branch (git checkout -b feature-name).

Commit your changes (git commit -m "Add feature").

Push to the branch (git push origin feature-name).

Open a Pull Request.

License
This project is licensed under the MIT License - see the LICENSE file for details.
Acknowledgments
Built with inspiration from motion detection algorithms and web-based video processing techniques.

