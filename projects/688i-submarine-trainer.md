---
layout: default  
title: 688i Weapons Launch Console Trainer  
---
# **688i Weapons Launch Console Trainer**
### **Platform(s):** Desktop (Windows)  
### **Role:** Lead Engineer  
### **Engine / Tech:** Unity (hybrid 2D/3D), .NET serialization, custom trainer framework  
### **Years:** 2016–2017  

---

## **Overview**
The 688i Weapons Launch Console (WLC) trainer was a modernization effort to convert an existing 2D WinForms‑based submarine trainer into a hybrid 2D/3D Unity application. I was initially assigned as lead engineer and ultimately became the sole engineer on the project. The Navy was not ready to fund a full 3D rewrite, so the goal was to update the weapons launch console itself while replicating the original 2D interface for other parts of the submarine needed for training.

One of the core challenges was that the original server and the new Unity client used different versions of .NET, each with slightly different serialization behavior. By carefully analyzing and translating the serialized data, I enabled the legacy server and the new Unity client to communicate seamlessly. This avoided a major rewrite of the server and helped keep the project well within budget.

The result was a fully functional hybrid trainer that preserved the original logic, modernized the interface, and provided a foundation for future submarine trainers.

---

## **My Responsibilities**
- Lead engineer for the entire client rewrite  
- Reverse‑engineered .NET serialization differences to maintain server compatibility  
- Built tools to map and visualize existing WinForms UI controls  
- Recreated the entire 2D interface in Unity using a **data‑driven UI system**  
- Integrated the new 3D Weapons Launch Console with the legacy 2D logic  
- Implemented touchscreen projection for auxiliary screens not physically present on the console  
- Created new graphics assets (LED displays, Navy seal)  
- Added sound effects and visual polish (transparency, fade‑in/out)  
- Collaborated with SMEs and visited the **U.S.S. Pasadena** for reference photography  
- Delivered a working prototype far ahead of schedule  
- Provided a codebase that junior engineers later extended without needing assistance  

---

## **Technical Highlights**

### **1. Serialization Compatibility Layer**
The original trainer relied on .NET serialization to communicate between server and client. The new Unity client used a different .NET version, causing subtle incompatibilities in serialized data formats. I engineered a translation layer that:

- interpreted the legacy serialized data,  
- adapted it to the newer .NET format,  
- and preserved full compatibility with the existing server, which only required minor modifications.

This allowed the legacy server to remain nearly untouched and enabled old WinForms clients and new Unity clients to run side‑by‑side during development — a major advantage for testing and verification.

---

### **2. Data‑Driven UI Reconstruction**
To understand the original interface, I wrote a tool that read the WinForms control definitions and drew bounding boxes for each control type. After enhancing the tool to overlay these boxes on the original background images, I realized the entire interface — control positions, images, and logic — was fully data‑driven and could be moved wholesale to the new system, simplifying development immensely.

By implementing a small set of equivalent controls in Unity and feeding them the original data, I reproduced the entire WinForms interface with minimal manual work. This approach produced a complete working 2D port very early in development, allowing the team to focus on the 3D WLC integration. Another engineer tested the port against the written procedures and the old system to ensure the logic was correctly imported and that the new Unity controls behaved identically to the legacy WinForms ones.

---

### **3. Hybrid 2D/3D Interface Integration**
The Navy provided reference photos from the original 2D trainer, but these omitted parts of the console that trainees did not interact with. For the 3D trainer, the entire console had to be represented, at least visually. I visited the **U.S.S. Pasadena** with the lead artist — who was gathering information for another project elsewhere in the sub — to capture the missing details.

Once the 3D WLC assets were complete, I created 3D control components that replicated the corresponding 2D controls and their original logic internally, but presented a modern 3D interface integrated into a fully accurate representation of the weapons launch console. For screens not physically present on the console but still required by the operator, I created side‑mounted quads and wrote algorithms to project touchscreen input onto them, preserving full functionality.

---

### **4. Visual and Audio Enhancements**
With time remaining after the core work was complete, I added several polish features:

- object transparency and fade effects  
- custom LED alphanumeric display graphics  
- a new high‑resolution Department of the Navy seal  
- sound effects for all console interactions  

These enhancements improved clarity, usability, and overall presentation.

---

## **Engineering Challenges**

### **Legacy Server Compatibility**
Maintaining communication with the original server required careful handling of .NET serialization differences.

### **Incomplete Reference Material**
The Navy’s original photos omitted parts of the console; visiting the submarine was essential for accuracy.

### **Hybrid Architecture**
The trainer needed to preserve the original 2D logic while presenting a modernized 3D interface.

### **Touchscreen Projection**
Auxiliary screens required custom projection logic to map trainee input correctly.

---

## **Collaboration**
I worked closely with SMEs and visited the **U.S.S. Pasadena** to gather reference data. I collaborated with the lead artist to ensure the 3D console matched real‑world equipment and integrated smoothly with the data‑driven UI system. I also coordinated with management to align prototype delivery with formal review milestones.

---

## **Outcome**
The 688i trainer was deployed successfully and exceeded expectations. The modernization effort preserved the original logic, delivered a significantly improved interface, and avoided a costly server rewrite. The Navy later commissioned a **688 2<sup>nd</sup> Flight Weapons Launch Console Trainer** built on top of my codebase, which junior engineers extended without needing assistance — a testament to the clarity and maintainability of the architecture.

---

## **Links**
- **<a href="https://www.navair.navy.mil/nawctsd/688i-Weapons-Launch-Console-WLC" target="_blank" rel="noopener noreferrer">NAWCTSD’s 688i WLC Page</a>**  
  Includes a video demo, mostly of the 2D direct copy of the old trainer. From 1:07, the 3D console is displayed. There is no interaction shown, but nearly all of the buttons, dials, and switches — over five hundred interactable controls, everything needed for training — are fully functional.  

- **<a href="https://www.navair.navy.mil/nawctsd/688-2nd-Flight-Weapons-Launch-Console-WLC" target="_blank" rel="noopener noreferrer">NAWCTSD’s 2<sup>nd</sup> Flight WLC Page</a>**  
  I had no direct involvement in this project, but it is based on my 688i code. The 3D consoles at the start of the video show many analog gauges that are not present on the all‑digital 688i console. The team modified a copy of my existing gauge code to quickly produce these new controls.  

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>

