# Laser Vision

## Project Description

This organisation holds all of the repositories for the laser vision system.

This system can track the intensity deviation of a laser over time.
Information is presented to the user via their browser.
The measurements are made available over the local network.

The system is designed to be reliable and resilient.
If a connection is lost, it can be re-established and measurement will continue.
Camera devices can be hot-plugged as needed.
If an issue is detected with a camera, it is reported through the GUI.

The design of the system is a central server and any number of "Edge computing" devices.
Users can access information from the system by using their browser to navigate to the server's url.
The information is displayed in a user-friendly GUI.
The edge computing device is anticipated to be a Raspberry Pi (RPi), however any device could work.

## Repository Navigation

### The main operation repositories

- **Edge**
	The edge computing tier manages the camera connections and provides the vision processing/image analysis.
	It connects and reports to, the **Server**.
- **Server**
	The central control tier provides the connection point for the **Edge** devices and forwards the information to users via their browser.
- **GUI**
	A browser-based graphical user interface. It displays system information, measurement readings, and provides configuration controls.

### Secondary operation repositories

- **Dataset Assistant**
	A helper program for collecting image data into a dataset for using in machine vision training.
- **Vision CNN**
	A machine vision technique that uses a convolutional neural network.
- **Vision Diff**
	A machine vision technique that uses image metric comparison.

### Supporting repositories

- **API**
	Provides the data structures used in communication over the local network between the **Edge** and **Server**, or **GUI** and **Server**.
- **Dataset Loader**
	A reusable library for reading our dataset from disk and presenting them to our machine vision training crates.
- **Custom RPi Manager**
	A repository that automatically creates an image for a Raspberry Pi, to aid in the deployment process.

We also use a custom fork of a cross-operating-system camera library called `nokhwa`.

## Manuals

User manuals are available at https://laser-vision-system.github.io/
