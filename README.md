# 🧁 Papa’s Cupcakeria (FPGA Game)

An interactive cupcake-making game inspired by *Papa’s Cupcakeria*, built on the DE1-SoC FPGA platform. The game simulates a full order workflow where players assemble cupcakes based on customer requests and are scored on accuracy and timing.

---

## 🎮 Overview  

This project recreates the experience of running a cupcake shop using a hardware-software system. Players move through multiple stages including order taking, base selection, icing, and decoration, with real-time visual and audio feedback.

The game was built to explore low-level graphics, input handling, audio output, and state-driven design on FPGA systems.

---

## ⚙️ Features  

- Multi-stage gameplay (order → base → icing → decoration → scoring)  
- Real-time user input using keyboard controls  
- VGA display output (320x240 resolution)  
- Smooth rendering using double buffering  
- Audio feedback through onboard speakers  
- Dynamic scoring system based on accuracy and timing  
- Visual UI elements including instructions, overlays, and customer feedback  

---

## 🧠 System Design  

The game is structured as a finite state machine, where each state represents a stage of the cupcake-making process.

- Each frame is rendered to a back buffer and swapped using vsync  
- Pixel-level drawing is handled through direct memory access  
- UI elements and sprites are preloaded and rendered onto the screen  
- Input is processed using PS/2 keyboard signals  
- Audio output is generated through onboard speakers to provide real-time feedback during gameplay  

---

## 🛠️ Tech Stack  

- **Language:** C  
- **Platform:** DE1-SoC FPGA (Nios II / Nios V environment)  
- **Graphics:** VGA pixel buffer (RGB565 format)  
- **Input:** PS/2 Keyboard  
- **Audio:** Onboard speakers (memory-mapped I/O)  
- **Concepts:**  
  - Double buffering  
  - Memory-mapped I/O  
  - Finite state machines  
  - Real-time rendering  

---

## 🕹️ How to Play  

1. Follow the customer’s order  
2. Select the correct base and liner  
3. Add icing and decorations using keyboard controls  
4. Match the order as closely as possible  
5. Receive a score based on accuracy and speed  

---
 
