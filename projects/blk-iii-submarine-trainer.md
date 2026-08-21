---
layout: default  
title: Virginia Torpedo Room Block III Trainer  
---
# **Virginia Torpedo Room Block III Trainer**
### **Platform(s):** Desktop (Windows)  
### **Role:** Interaction Design / Systems Engineer  
### **Engine / Tech:** Unity (legacy version), custom trainer framework  
### **Year:** 2016  

---

## **Overview**
The Virginia Torpedo Room Block III trainer was my introduction to Unity and my first project at Proactive Technologies. The trainer was originally built on top of the Block I/II system, which had been written by outside contractors, and the inherited codebase was widely considered difficult to maintain. Because the project was already deep into development, rewriting the entire system wasn’t feasible — instead, I was tasked with stabilizing, extending, and modernizing the trainer while working within the constraints of an outdated Unity version and inconsistent legacy code.

Despite joining late, I delivered several foundational improvements that made the trainer more maintainable, more consistent, and easier to extend. Many of the engineering patterns I developed here became the basis for my later work on the 688i and EMALS trainers.

---

## **My Responsibilities**
- Cleaned up and modernized inherited UI code  
- Implemented a proper **radio‑button group control** to replace duplicated ad‑hoc logic  
- Rewrote the **valve interaction system**, replacing physics‑based torque/friction controls with a clean UI‑driven model  
- Added new valves and improved the workflow for configuring them  
- Reproduced in‑world touchscreen interfaces for the weapons launch console  
- Improved maintainability and consistency across multiple legacy systems  

---

## **Technical Highlights**

### **1. Rebuilding the UI Interaction Framework**
The inherited UI code relied heavily on one‑off solutions and duplicated logic. Radio buttons, in particular, were implemented differently in multiple places. I replaced all of these with a unified **radio‑button group component**, where:

- individual buttons were children of the group GameObject,  
- the group managed selection state,  
- and all UI logic became consistent and predictable.

This eliminated a large amount of duplicated code and made future UI work significantly easier.

---

### **2. Redesigning the Valve System**
The original valve implementation attempted to simulate physical torque, friction, and resistance — an approach that made sense for physics‑based gameplay but was completely inappropriate for a touchscreen trainer. The result was a system that was:

- difficult to configure,  
- inconsistent across valves,  
- and frustrating for developers.

I reframed the problem as a **UI interaction**, not a physics simulation. The new valve system used:

- start and stop angles,  
- a simple multiplier mapping finger rotation to valve rotation,  
- and deterministic behavior that felt correct on a touchscreen.

This redesign made adding and tuning new valves trivial and dramatically improved usability. I later extended this system to support locking pins and other locking devices.

---

### **3. Stabilizing and Extending Legacy Systems**
Because the project was already deep into development, I had to work within:

- an outdated Unity version,  
- legacy .NET constraints,  
- and code written by multiple contractors with inconsistent styles.

I cleaned up numerous ad‑hoc systems while preserving compatibility, ensuring the trainer could ship without a full rewrite. I also added a sortable, searchable dropdown property drawer for managing the growing list of messages supported by the system.

---

## **Engineering Challenges**

### **Inherited Codebase**
The trainer was built on top of older Block I/II work, and the code quality varied widely. My job was to stabilize and extend it without breaking existing functionality.

### **Outdated Unity Version**
To avoid compatibility issues with legacy code, the project used an older version of Unity. This limited available features and required careful engineering.

### **UI/UX Consistency**
The trainer relied heavily on touchscreen interactions, but the inherited UI systems were inconsistent. I unified them and made them maintainable.

---

## **Collaboration**
I coordinated with other engineers to integrate my rewritten systems without disrupting existing work.

---

## **Outcome**
The Block III trainer was deployed successfully, and the project established my engineering approach at ProActive and set the stage for my later leadership roles on the [688i](./688i-submarine-trainer.html) and [EMALS](./emals.html) trainers.

---

## **Links**
- **<a href="https://www.navair.navy.mil/nawctsd/VIRGINIA-Torpedo-Room-Block-III-VA-Torp-Rm-BLK-III-or-VA-BLKIII-0" target="_blank" rel="noopener noreferrer">NAWCTSD's Virginia Torpedo Room Block III Trainer Page</a>**  
  Includes a video demo which unfortunately does not feature my work, but gives an idea of what the trainer is about.  

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>
