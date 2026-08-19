---
layout: default  
title: Jillian Michaels Fitness Adventure  
---
# **Jillian Michaels Fitness Adventure**
### **Platform(s):** Xbox 360  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** n‑Space internal engine, Xbox 360, Kinect  
### **Year:** 2011  

---

## **Overview**
*Jillian Michaels Fitness Adventure* was my first project at n‑Space, my first Xbox 360 title, and my first Kinect game. n‑Space had never shipped a Kinect game before and had only released one Xbox 360 title, so I had to learn the engine, the console, and the Kinect hardware all at once. Despite that, I had the first Kinect gameplay working in under a week.

I wrote **all foundational Kinect gameplay code** and a large percentage of the overall gameplay systems. The design included exercises that Kinect’s skeletal tracking couldn’t handle, so I built a custom depth‑map comparison system that matched the player’s silhouette against Jillian Michaels’ motion‑capture data. This allowed the game to support poses and movements that were impossible to detect using skeletal tracking alone.

The Kinect was still new at the time, and the documentation was incomplete — especially for a project this ambitious. Much of the work required experimentation, reverse‑engineering behavior, and building systems that went beyond what the SDK officially supported.

---

## **My Responsibilities**
- Wrote **all foundational Kinect gameplay code**  
- Implemented a large percentage of the game’s overall gameplay  
- Learned n‑Space’s engine, Xbox 360 hardware, and Kinect SDK simultaneously  
- Built a custom depth‑map comparison system for exercises skeletal tracking couldn’t detect  
- Integrated Kinect input into n‑Space’s engine  
- Implemented early Xbox Avatar support (later cut due to design changes)  
- Implemented a 2.5D display of the player using the Kinect’s depth map and a custom shader that flashed green, yellow, or red based on exercise performance  
- Delivered working Kinect gameplay in under a week  

---

## **Technical Highlights**

### **1. Full Kinect Gameplay Implementation**
Because n‑Space had no prior Kinect experience, I owned the entire Kinect gameplay pipeline:

- sensor initialization  
- skeletal tracking integration  
- depth‑map processing  
- pose evaluation  
- exercise correctness logic  
- gameplay feedback systems  

This required deep understanding of Kinect’s quirks, noise patterns, and latency characteristics.

---

### **2. Custom Depth‑Map Comparison System**
Many exercises in the design were **not compatible with skeletal tracking**, which struggled with:

- occlusion  
- non‑standard poses  
- floor‑level movements  
- exercises requiring precise limb alignment  

To solve this, I built a system that:

- captured the player’s **depth map**  
- compared it against Jillian Michaels’ **motion‑capture skeletal animations**  
- evaluated pose correctness based on shape and depth rather than joints  
- bypassed skeletal tracking entirely for certain exercises  

This was advanced Kinect work, especially given the SDK’s early state.

---

### **3. Rapid Ramp‑Up on New Technology**
This project required learning three unfamiliar systems at once:

- n‑Space’s internal engine  
- Xbox 360 hardware and development environment  
- Kinect hardware and SDK  

Despite that, I delivered working Kinect gameplay in **under a week**, allowing the team to begin prototyping exercises immediately.

---

### **4. Early Xbox Avatar Integration**
The original design included Xbox Avatar support. I implemented early versions of:

- Avatar rendering  
- Avatar animation hooks  
- Avatar integration with Kinect gameplay  

The feature was later cut due to a shift toward using the Jillian Michaels model (and mocap data) from the previous game and adopting a first‑person perspective for the player. Even so, the work demonstrates familiarity with multiple Xbox subsystems.

---

### **5. Working With Early Kinect Documentation**
The Kinect SDK was still new, and documentation was:

- incomplete  
- inconsistent  
- missing examples for advanced use cases  
- unclear about skeletal tracking limitations 
- insufficient for exercises outside skeletal tracking’s capabilities  

Much of the project required experimentation, testing edge cases, and building systems that went beyond what the SDK officially supported.

---

## **Engineering Challenges**
- Learning three new systems simultaneously  
- Working with immature Kinect documentation  
- Handling exercises skeletal tracking couldn’t detect  
- Designing depth‑map comparison algorithms  
- Managing noisy sensor data  
- Ensuring responsive gameplay despite Kinect latency  
- Integrating Kinect input into n‑Space’s engine  
- Supporting early Avatar features before they were cut  
- Converting a depth map into a “lit” representation of the player using a fragment shader  

---

## **Outcome**
I delivered the Kinect gameplay system for the entire project and implemented a large portion of the overall gameplay. I built custom depth‑map comparison technology to support exercises the Kinect SDK couldn’t handle, and I ramped up on new hardware and engine tech extremely quickly. The project was a major technical milestone and established n‑Space’s Kinect development capabilities.

---

## **Links**
- **<a href="https://www.youtube.com/watch?v=jkP3bjh4gd0" target="_blank" rel="noopener noreferrer">Game Trailer</a>**  
  A YouTube Video of the official trailer for *Jillian Michaels Fitness Adventure*.  
- **<a href="https://www.youtube.com/watch?v=tSMQRSN9aro&t=256s" target="_blank" rel="noopener noreferrer">Gameplay Video</a>**  
  A YouTube video showing some of *Jillian Michaels Fitness Adventure*’s gameplay.  

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>
