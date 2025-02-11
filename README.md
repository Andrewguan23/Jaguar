# Jaguar: Your Voice-Controlled, Vision-Following Companion

## Introduction

Jaguar is a cutting-edge robotic companion designed to follow its owner and respond to voice commands. It's built using a Raspberry Pi 4 and operates on top of a versatile robotic car kit. With the integration of OpenCV for vision processing, voice2json for voice command processing, and the power of Python's threading module to perform tasks concurrently, Jaguar aims to bring a seamless interaction experience for its users.

Feel free to take a look at our [video](https://www.youtube.com/watch?v=wQcw5l1Z3wA) and [write-up](https://docs.google.com/document/d/1ztQf92YcndKGzKyTzCXy-8aizcrnh6dniFlokOzctGc/edit?usp=sharing) for more information!

## Components Used

- **Main Board**: Raspberry Pi 4
- **Mobility**: Robotic car kit composed of 4 DC drivetrain motors
- **Positional Adjustment**: 2 servo motors
- **Visual Input**: Raspberry Pi camera module
- **Audio Input**: USB microphone
- **Feedback**: Buzzer for auditory signals.
- **Distance Measurement**: 3 ultrasonic sensors

## How it Works

### Following its Owner using OpenCV

Using the Raspberry Pi camera module, Jaguar captures visual data of its surroundings. OpenCV processes this data to identify and track the owner. Algorithms detect specific color patterns or shapes that the owner may wear (e.g., a unique hat or badge), enabling Jaguar to differentiate its owner from others.

### Voice Command Processing with voice2json

The USB microphone captures audio data, and voice2json processes this to identify specific voice commands. Commands like "come here," "stop," and "turn around" have been pre-configured, but Jaguar's capabilities can be extended by adding more voice patterns.

### Multi-threading with Python

To ensure Jaguar can track its owner and listen for voice commands simultaneously, we utilized Python's threading module. This allows Jaguar to process visual and auditory data in parallel, ensuring prompt reactions to both visual cues and voice commands.

### Navigation and Feedback

The 3 ultrasonic sensors help Jaguar navigate its environment by measuring distances to obstacles. This ensures it doesn't bump into objects while following its owner. The buzzer provides feedback to the owner, such as acknowledgment of a command or a warning when the battery is low.
