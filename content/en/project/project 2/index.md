---
title: Peripherals of electronic computing systems
summary: Еxplore the types of peripheral devices,how to connect them to a computer and find out how interaction is provided devices of a computer or information processing system and programs
tags:
  - Deep Learning
date: '2022-05-28'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Follow
    url: https://github.com/aaandrievskaya
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

## Introduction

It is impossible to imagine a computer without means of communication with a person or means of interfacing with external control objects. Such tools are necessary for downloading programs and data, uploading the results obtained, storing huge amounts of information, correcting computer operation by the user, as well as for direct control of production processes and objects. All these functions are assigned to a variety of peripheral devices (PU), which serve to transform the ways of presenting information suitable for a person and used in a computer, to control input / output and organize information storage, regardless of the presence of power.

Thus, I consider it important to systematize and structure information about the peripheral devices of computers, and then determine the significance of the place of peripheral devices in electronic computers.

## 1. Interaction of PU and computer

### 1.1 Definition of peripherals

Peripheral, or external, devices got their name in the 1960s, when the processor and RAM were placed in rack cabinets, forming a kind of "center", and the rest of the devices, mostly electromechanical, were at some distance from it, i.e. on the periphery. But modern PUs are located both inside the computer case and outside, depending on the type of device and its interaction with objects in the outside world.
A peripheral device is an additional auxiliary device external to the central processor and main memory, designed to input and / or output information to a computer and store data, and expanding its functionality. That is, it is by and large an optional device for the operation of a computer, but in most cases it is necessary for the implementation of certain user tasks.
 There are four types of peripherals:
1) input devices;
2) output devices;
3) input-output devices;
4) data storage devices.
Some PUs, called internal, are mounted in the same case with the computer (for example, hard disk, sound card, network card), while others, called external, are outside the case (for example, keyboard, mouse, printer) and are connected to it using a wired or wireless connection.
Peripherals are connected to the central part of the computer through an interface, so it is important to give several definitions of this important concept.


### 1.2 Interface

Interface (interface) - a set of tools and rules that ensure the interaction of devices of a computer or information processing system and (or) programs. In addition to these standard definitions, it is convenient to use one more that expands and refines the above.
 An interface is a set of means and rules that provide interaction:
1) between different nodes of a computer system (hardware interface);
2) between programs (software interface);
3) between hardware and software (hardware and software
interface);
4) between a person and a computer (human-machine interface).

Peripheral devices with such a type of human-machine interface as the USB HID class seem to be very promising for use. USB HID is a class of USB devices that connect to a computer for human interaction. This class includes devices such as keyboard, mouse, game controller.

### 1.3 Tires

So, to connect a peripheral device, you must first provide a hardware interface. In a computer, it is implemented by I / O buses. Modern computers contain two types of buses:
 a) the system bus that connects the central processing unit to the main
memory;
 b) multiple I/O buses connecting various peripherals to the system bus and processor via a bridge
The bus is a subsystem for transmitting data both internally
computer and beyond. Unlike a point-to-point connection, which is designed to connect only two devices, a bus, by using the same set of wires, can provide a logical connection for several peripheral devices.
The main difference between peripherals is the way they are connected - internal or external. The first is implemented using internal buses, represented by internal connectors (slots) on the system board, the second method is implemented by external buses, represented by external connectors (ports).
However, in the general case, an external peripheral device connection scheme is used.
 
Next, we should recall the need for a hardware-software interface, i.e. peripheral controller driver.


### 1.4 Drivers

Driver is a computer software with the help of which another software (operating system) gains access to the hardware of some, in our case, peripheral device. Typically, operating systems ship with drivers for key hardware components that the system cannot function without. However, some devices (such as a video card or printer) may require special drivers, usually provided by the device manufacturer.


## 2. Types of peripherals

### 2.1 Input devices

Input devices are those devices through which information can be entered into a computer. Their main purpose is to implement the impact on the PC. The variety of input devices produced has given rise to entire technologies: from tactile to voice. Although they work on different principles, they are intended to implement one task - to allow the user to communicate with their computer.
KEYBOARD
The main input device of most computer systems is the keyboard. Until the voice recognition system can reliably perceive human speech, the dominant position of the keyboard is unlikely to change.
SCANNER
A scanner is a device that, by analyzing an object (usually an image, text), creates a digital copy of the image of the object.
The process of obtaining this copy is called scanning.
Mouse
Manipulator and coordinate device of the computer. It is an addition to the keyboard and a necessary piece of equipment when using the graphical interface.
Joystick
Computer coordinate and manipulator device in the form of a handle with buttons. Used in simulators and in conjunction with game programs. A variety of game joysticks are "gamepads", made in the form of small-sized panels, equipped with functional buttons and switches.
Webcam
A digital video or still camera capable of capturing images in real time for further transmission over the Internet.

### 2.2 Output devices

Peripheral output devices are designed to output information in the format required by the operator. Among them there are mandatory (included in the basic PC configuration) and optional devices.
 MONITOR
The monitor is a necessary information output device. The monitor (or display) allows you to display alphanumeric or graphical information in a form that is easy to read and control by the user.
 PRINTERS
A printer is a widespread device for outputting information to paper, its name is derived from the English verb to print - to print. The printer is not included in the basic PC configuration.
 PROJECTION TECHNOLOGY
Multimedia projectors have firmly entered our lives at the end of the 20th century, and now it is impossible to imagine many areas of human activity without them. These are the educational process, presentations, show business and home cinema. A multimedia projector allows you to play on a large screen information received from a computer, VCR, camcorder, camera, DVD player, game console.

### 2.3 I/O devices

Peripheral output devices are designed for both input and output of information in the format necessary for the operator and there are several types depending on the purpose.
Audio headset
It is both audio equipment (output device) and a microphone (information input device) 
Virtual reality headset
A head-mounted device that provides virtual reality to the user. Virtual reality is a computer-generated world that completely replaces the real one, while the user can influence it by immersing, for example, in a video game.

### 2.4 Storage devices

Flash drive
A storage device that uses flash memory as a medium and is connected to a computer or other reader via an interface.
hard disk drive, hard disk
A storage device (information storage device, drive) of random access, based on the principle of magnetic recording. It is the main storage medium in most computers.
floppy disk drive, floppy disk
A device for storing small amounts of information, which is a flexible plastic plate in a protective shell.
Used to transfer data from one computer to another.

## Conclusion

Summing up my work, it can be argued that the goal I set was achieved, namely: the types of peripheral devices, ways of connecting them to a computer were investigated; I also learned how the interaction between the devices of a computer and an information processing system or programs is ensured.


