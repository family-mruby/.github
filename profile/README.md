## What is Family mruby?

Family mruby is an environment where you can enjoy Ruby programming on a standalone microcontroller board, without needing a PC.

In the past, it was based on an ESP32 setup using FabGL with a VGA monitor and a PS/2 keyboard.  
The current goal is to run on an NTSC monitor with a USB keyboard.

## Purpose

Once upon a time, BASIC was the first programming language many children encountered.  
Although it was limited, there were products like *Family BASIC* that allowed BASIC programming not only on PCs, but also on platforms such as MSX and the Famicom. Many people discovered the joy of programming through those systems and went on to become programmers.

Today, development environments for most programming languages can be installed on a PC for free. However, there are often *too many* things you can do. It can be hard to know where to start, and even getting from “Hello, World” to making a simple game can require a surprisingly high setup cost.

Family mruby was created to address this: an environment where you can build small games and programs using a scripting language, on a single microcontroller.

## Features

- **Multi-VM**
  - Each FreeRTOS task owns its own independent mruby VM
  - VMs communicate with each other via IPC (Inter-Process Communication)

- **OS-like Architecture**
  - Clear separation of Kernel / App / HAL (Hardware Abstraction Layer)
  - Applications have PIDs and are lifecycle-managed

- **GUI / Window Management**
  - Based on LovyanGFX
  - Applications only need to care about their own drawing area

- **Embedded-oriented I/O Abstraction**
  - A well-defined HAL (Hardware Abstraction Layer)

- **Target Environment**
  - ESP32-S3 with PSRAM
  - Designed to run on a custom board (commonly called the *Narya board*)
