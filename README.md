webcam-pulse-detector
=====================

An app that detects the heart-rate of an individual using their webcam.

Requirements:
---------------

- Python v2.7+ (http://python.org/)
- OpenCV v2.4+, with the cv2 python bindings (http://opencv.org/)
 
OpenCV is a powerful open-source computer vision library, with a convenient numpy-like interface in the cv2 bindings.

- OpenMDAO v0.5.5+ (http://openmdao.org/)

OpenMDAO is an open-source engineering library that serves as a convenient and readable design enviroment for the required real-time analysis.

Quickstart:
------------
- In a windows command window or Unix/OSX terminal, activate the openMDAO virtual python environment
- Run get_pulse.py

How to use:
----------
- When run, a window will open showing a stream from your computer's webcam
- The application will search for a human face within the camera frames, and attempt to isolate an area on the forehead
- When a forehead location has been isolated, the user should press "S" on their keyboard to lock this location, and remain as still as possible
- The application will then track the variations in this location over time to measure a heartbeat. To view a stream of this data, press "D".
- The data display shows three data traces, from top to bottom: 1) raw optical intensity, 2) extracted heartbeat signal, 3) Power spectral density, with local maxima indicated the heartrate (in beats per minute). 
- With good lighting and minimal motion noise, a stable heartbeat should be isolated in about 10 seconds
