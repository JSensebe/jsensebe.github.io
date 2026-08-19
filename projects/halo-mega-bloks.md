---
layout: default  
title: Halo Mega Bloks  
---
# **Halo Mega Bloks**
### **Platform(s):** Xbox 360 (Canceled)  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** Unreal Engine 3, Xbox 360  
### **Year:** 2013  

---

## **Overview**
*Halo Mega Bloks* was an unpublished Xbox 360 project developed by n‑Space. Despite never reaching release, it featured a surprising amount of functional gameplay, enemy AI, physics, and level interaction. I joined the project during active development and contributed improvements to core AI systems and enemy behavior.

The project was technically interesting, and its abrupt cancellation marked the beginning of n‑Space’s final period before the studio closed. Years later, gameplay footage — and eventually code for a vertical slice — leaked online and received high praise for its polish and potential, even though the build was unfinished.

---

## **My Contributions**
- Overhauled the **enemy cover system** to make it performant  
- Improved **enemy recovery from ragdoll** states  
- Supported gameplay stability and responsiveness during vertical slice development  

---

## **Technical Highlights**

### **1. Real‑Time Cover System Overhaul**
The original cover system was extremely inefficient. It rebuilt a list of **every cover location for every enemy on every frame**, which was computationally expensive and unsuitable for real‑time gameplay.

I redesigned the system to:

- maintain a **global cover list**  
- update it only when level segments were loaded or unloaded  
- use **messages** to add or remove cover locations dynamically  

This significantly reduced CPU usage and memory overhead, and later supported **destructible cover**, which required real‑time updates without heavy performance cost. I integrated this logic into the third‑party AI system n‑Space used on the project.

---

### **2. Ragdoll Recovery Improvements**
Enemies could be knocked into ragdoll states, but the system for standing them back up was unreliable and visually awkward.

I implemented a simple but non‑obvious fix:

- determine the orientation of the enemy’s **hips**  
- select an appropriate **stand‑up animation** based on that orientation  

This ensured enemies recovered smoothly and consistently, improving both gameplay readability and animation quality.

---

## **Outcome**
Although *Halo Mega Bloks* was ultimately canceled, the engineering work was meaningful. The project’s termination led to major layoffs at n‑Space, and the studio completed only one more large project before closing its doors.

My contributions strengthened the project’s AI behavior and performance, and the work remains a technically interesting part of my career despite never shipping.

---

## **Links**
- **<a href="https://www.youtube.com/watch?v=iRFWAHZy1vY" target="_blank" rel="noopener noreferrer">Gameplay Video</a>**  
  A YouTube video showing some of Halo Mega Bloks’ gameplay from an older build. The code was leaked several years ago.  

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>
