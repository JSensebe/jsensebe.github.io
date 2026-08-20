---
layout: default  
title: Olly Power Play  
---
# **Olly Power Play**
### **Platform(s):** Meta Quest 2, Pico Neo 4  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** Unity, VR (Meta Quest 2 / Pico Neo 4)  
### **Year:** 2022  

---

## **Overview**
*Olly Power Play* is the result of a long, winding R&D journey that began years before the VR game itself. Olly the Ox was originally created as a mascot for the Chinese market, with a mobile Unity game planned for the Year of the Ox (2021). When funding fell through and the project repeatedly changed direction, I worked on a series of prototypes, animation systems, AI behaviors, and tools that never shipped — but ultimately laid the technical foundation for *Olly Power Play*.

The VR game began as a small catching prototype built in a few days for the Meta Quest 2. That prototype evolved rapidly, eventually becoming a full throwing‑and‑targeting game with custom physics, complex animation systems, particle effects, and VR‑specific optimizations. I wrote the throwing physics from scratch, built Olly’s animator controllers and IK systems, created multiple particle effects, and developed tools to streamline animation integration.

---

## **The Story**

### **1. Origins: Olly as a Chinese‑market mascot**
Olly the Ox was created as a character for the Chinese market, with a Unity mobile game planned for the Year of the Ox (2021). Each year would introduce a new zodiac character, and a tiger character for 2022 was already in development.

My earliest tasks included:

- **Island wandering AI** using a heat‑map system  
  - Areas “cooled” over time  
  - Olly was more likely to wander to places he hadn’t visited recently  

- **Turtle AI** for a minigame  
  - flocking behavior  
  - field‑of‑view detection  
  - turtles fleeing or hiding in shells  
  - sneaking mechanics (approach outside FOV)
  - scalable to more than 50 turtles in play

During this period, I also worked on Olly’s animator controller, IK systems, procedural blinking, and animation tools.

---

### **2. The abandoned projects phase**
The project’s direction changed several times:

- Chinese funding fell through  
- The game pivoted to Middle Eastern tourism  
- The design changed repeatedly  
- Dozens of animations and assets were created but never used  

I was also assigned to several small projects, including an Android app that inserted Olly into photos for convention use.

Although none of these projects shipped (the photo app was used at a convention), the technical work — AI systems, animation logic, IK, and tools — would later become essential.

---

### **3. The VR turning point**
During this limbo period, I was given a **Meta Quest 2** (still branded Oculus at the time) and asked to build a simple catching game:

- Olly throws a ball  
- The player catches it  

There were no throwing animations, so I repurposed part of a kicking animation — inspired by *The Karate Kid* — and had Olly kick balls to you instead. I built the prototype in a few days, and the design began evolving immediately.

This was the moment Olly returned to the forefront of Waysun’s development efforts.

---

### **4. Evolution into a full VR game**
The prototype grew rapidly:

- Olly kicked different colored balls  
- The player threw them into matching hoops  
- Level‑up effect: Olly points to the sky and shoots lightning (particle effect)  
- Kicking replaced by a bucket of balls  
- Hoops replaced by targets  

As the game improved, *Olly Power Play* emerged from the prototype. The changes kept coming:

- Balls replaced by fruit  
- Fruit splattered on impact (particle effect)  
- Sand and grass billboard particles  
- Leaf particles when fruit passed through trees  
- New animations created specifically for the game  
- I worked closely with artists to integrate them

---

## **My Responsibilities**
- Wrote the **throwing physics** from scratch  
- Implemented the **catching mechanic**  
- Built **complex animator controllers** for Olly  
- Developed **custom IK** for Olly’s head to support squash‑and‑stretch behavior (the built‑in IK couldn’t be used)  
- Created the **procedural blinking system**  
- Built tools for managing animation triggers  
- Built a tool to **auto‑detect footsteps** and add sound triggers  
- Created multiple **particle effects**:
  - sand and grass billboard particles  
  - fruit splatter  
  - leaf particles  
- Collaborated on VR performance optimizations  
  - prerendered shadow maps  
  - simplified geometry  
- Helped evaluate third‑party throwing plugins  
  - my throwing code outperformed the commercial solution

---

## **Technical Highlights**

### **1. Throwing Physics**
The throwing mechanic is the core of the game. I wrote the physics from scratch, building on Unity’s foundation but tuning it extensively to feel natural in VR. The system provides:

- intuitive control  
- predictable arcs  
- consistent behavior across frame rates  
- more forceful throws that still felt “right,” allowing players without a powerful throwing arm to reach the farthest targets  
- special fruit power‑ups with enhanced force  

A commercial throwing‑mechanic plug‑in was tested, but my implementation felt more natural and offered better control.

---

### **2. Catching Mechanic**
Olly periodically throws special fruit to the player. Catching it grants extra throwing power. This required:

- precise collision tuning  
- hand‑tracking integration  
- timing adjustments  
- feedback cues  

---

### **3. Animator Controllers and IK**
Olly’s animator controllers were complex, requiring:

- custom IK for head movement  
- animation‑controlled IK toggling  
- procedural blinking  
- coordination between animations and procedural systems  

For example, when Olly closes his eyes and scratches his nose, blinking and head‑tracking must be disabled temporarily so the animation can fully control eyelids and head position.

---

### **4. Animation Tools**
To streamline production, I built:

- a tool to manage animation triggers  
- a tool to automatically detect footsteps and add sound triggers  

These saved significant time across dozens of animations.

---

### **5. Particle Effects**
I created multiple particle systems:

- sand and grass billboard particles  
- fruit splatter on impact  
- leaf particles when fruit passed through trees  

These effects added clarity and personality to the game.

---

### **6. VR Performance Work**
VR requires strict minimum frame rates. Since *Olly Power Play* ran entirely on standalone headsets without PC support, this created technical challenges. I collaborated with other engineers to:

- use prerendered shadow maps  
- simplify geometry  
- reduce rendering overhead  

These optimizations ensured smooth performance on both Meta Quest 2 and Pico Neo 4.

---

## **Outcome**
*Olly Power Play* emerged from years of prototypes, abandoned projects, and VR R&D. The final game features polished throwing physics, expressive animation systems, custom IK, procedural effects, and optimized VR performance. The long development journey — from mobile mascot to VR game — shaped both the character and the technology behind him.

---

## **Links**
- **<a href="https://www.meta.com/experiences/olly-power-play/5087128164632155/" target="_blank" rel="noopener noreferrer">Official Meta Page</a>**  
 The official Meta page for *Olly Power Play*, including a trailer and reviews.  
- **<a href="https://youtu.be/ZOf7w9cs8rA?t=154" target="_blank" rel="noopener noreferrer">Gameplay Video</a>**  
  A YouTube video showing some of *Olly Power Play*’s gameplay. (I do not advise throwing with both hands if you want a high score.)   

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>
