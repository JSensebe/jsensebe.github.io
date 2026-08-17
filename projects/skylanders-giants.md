---
layout: default
title: Skylanders Giants
---
# **Skylanders: Giants**
### **Platform(s):** Nintendo 3DS  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** Toys for Bob engine, proprietary scripting tools  
### **Year:** 2012  

---

## **Overview**
*Skylanders: Giants* for Nintendo 3DS was developed under a very tight schedule, with nSpace adapting Toys for Bob’s engine and proprietary scripting system. My work focused on several technically meaningful systems: rewriting RFID read/write logic to support packed data, building a new camera system, and restructuring memory allocations to support expanded asset sets. The project required learning an unfamiliar engine quickly and working within a restrictive scripting environment that resembled Garry Kitchen’s *GameMaker* more than any conventional text‑based workflow.

---

## **My Responsibilities**
- Modified RFID read/write routines to support packed data formats  
- Built a new camera system with additional follow modes  
- Restructured memory allocations to support expanded hat assets  
- Adapted quickly to the Toys for Bob engine and scripting tools  
- Supported designers by implementing required camera behaviors  
- Ensured stability under a compressed production timeline  

---

## **Technical Highlights**

### **1. RFID Read/Write Code for Packed Data**
The Skylanders toys store character data in packed formats. The Toys for Bob engine lacked binary operations, so the existing RFID routines couldn’t interpret the data correctly. I rewrote the read/write logic to:

- unpack and repack data without bitwise operators  
- correctly interpret toy data on the 3DS  
- maintain compatibility with the engine’s constraints  

This required careful manipulation of data structures and a deep understanding of how the toys encoded information.

---

### **2. New Camera System**
The original camera code only supported a simple linear follow mode. Designers needed more flexibility, so I implemented:

- **Circular follow mode** — camera orbits the player  
- **Limited‑space follow mode** — camera moves within a constrained region  

These additions improved readability, supported level‑specific needs, and expanded the engine’s camera capabilities.

---

### **3. Memory Allocation Overhaul**
The number of collectible hats doubled for *Giants*. The hat‑selection “level” (similar to a Unity scene) became too large to fit in memory. I modified memory allocations so:

- the expanded asset set could load  
- the selection level remained stable  
- the game stayed within 3DS memory limits  

This prevented crashes and ensured the expanded content could ship.

---

### **4. Learning the Toys for Bob Engine and Scripting Tools**
The scripting system was one of the most unusual parts of the project:

- scripts were **not text files**  
- commands were selected from **dropdown menus**  
- no copy/paste, no search/replace, no diffing  
- no editing in Visual Studio  
- workflow resembled **Garry Kitchen’s GameMaker**

Despite the restrictive environment, I learned the system quickly and used it to support designers and implement required behaviors.

---

## **Engineering Challenges**

### **Compressed Schedule**
The handheld version had a very short production window. All systems had to be implemented quickly and reliably.

### **Engine Limitations**
Lack of binary operations required creative solutions for packed data.

### **Scripting Workflow Constraints**
The dropdown‑based scripting tool slowed iteration and required a different mental model than text‑based scripting.

### **Memory Constraints**
The expanded hat assets pushed the 3DS memory limits, requiring careful restructuring.

---

## **Collaboration**
I worked closely with designers who needed specific camera behaviors and gameplay interactions. I also collaborated with QA to ensure stability after modifying core systems like RFID logic and memory allocations.

---

## **Outcome**
*Skylanders: Giants* shipped on Nintendo 3DS in 2012. My contributions strengthened the engine’s capabilities, enabled expanded content, and ensured compatibility with Skylanders toy data — all under a compressed schedule and within the constraints of an unfamiliar engine and scripting environment.

---

## **Video**
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe 
    src="https://www.youtube-nocookie.com/embed/yrkz282g0TE" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
    frameborder="0" 
    allowfullscreen>
  </iframe>
</div>
