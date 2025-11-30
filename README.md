# Mini Paint – C++ Image Processing Pipeline

This project implements a **pipeline for handling RGB images** with 8 bits per channel using **C++**.  
It supports image manipulation via a simple script language called **Scrim** (Script for images).

This project was developed by David Ferreira (up202406798@edu.fe.up.pt), Eduardo Santos (up202406938@edu.fe.up.pt) and Tiago Ribeiro (up202404941@edu.fe.up.pt) for **Programing L.EIC** 2024-25.

**Final Grade:** 19.9 / 20

## 🛠️ Features

- **Color Class** – Represents RGB colors with 8-bit channels.  
- **Image Class** – Represents images as 2D matrices of Color objects.  
- **Command Hierarchy** – Implements multiple image manipulation commands:
  - Simple pixel operations: `invert`, `to_gray_scale`, `replace`, `fill`
  - Geometric transformations: `h_mirror`, `v_mirror`, `move`, `slide`, `crop`, `resize`, `rotate_left`, `rotate_right`, `scaleup`
  - File operations: `blank`, `open`, `save`
- **Scrim Parser** – Reads and executes Scrim scripts containing sequences of commands.  
- **Chaining Commands** – Supports executing multiple scripts sequentially with recursion prevention.  
- **Automated Testing** – Includes a `tester` executable to validate functionality.

## 🚀 How to Build & Run

From the project root:

```bash
cmake -B build
cd build
make

Run Scrim scripts:

./runscrim ../scrims/example.scrim

Run tests:

./tester Color       # Test Color class
./tester invert      # Test invert command
./tester             # Run all tests

