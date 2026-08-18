---
layout: default  
title: Halo Mega Bloks  
---
# **Halo Mega Bloks**
### **Platform(s):** Xbox 360 (Unpublished Prototype)  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** n‑Space internal engine, Xbox 360  
### **Year:** 2015  

---

## **Overview**
*Halo Mega Bloks* was an unpublished Xbox 360 prototype developed by n‑Space. Despite never reaching release, it featured a surprising amount of functional gameplay, enemy AI, physics, and level interaction. I joined the project during active development and contributed improvements to core AI systems and enemy behavior.

The work was technically interesting, and the project’s abrupt cancellation marked the beginning of n‑Space’s final period before the studio closed.

---

## **My Contributions**
- Overhauled the **enemy cover system** to make it performant  
- Improved **enemy recovery from ragdoll** states  
- Supported gameplay stability and responsiveness during prototype development  

---

## **Technical Highlights**

### **1. Real‑Time Cover System Overhaul**
The original cover system was extremely inefficient. It rebuilt a list of **every cover location for every enemy on every frame**, which was computationally expensive and unsuitable for real‑time gameplay.

I redesigned the system to:

- maintain **global cover lists**  
- update them only when level segments were loaded or unloaded  
- use **messages** to add or remove cover locations dynamically  

This allowed the cover system to run efficiently and later supported **destructible cover**, which required real‑time updates without heavy CPU cost.

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

My contributions strengthened the prototype’s AI behavior and performance, and the project remains a technically interesting part of my career despite never shipping.
