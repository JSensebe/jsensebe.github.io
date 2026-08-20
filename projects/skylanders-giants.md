---
layout: default  
title: "Skylanders: Giants"  
---
# **Skylanders: Giants**
### **Platform(s):** Nintendo 3DS  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** Toys for Bob engine, proprietary scripting tools  
### **Year:** 2012  

---

## **Overview**
*Skylanders: Giants* is a “toys‑to‑life” game where physical figures store character progress and abilities. Players place the toys on a reader (the “portal”), and the game reads the character’s packed data directly from the figure through an RFID chip. Because the 3DS is a portable device, the RFID reader was not connected during gameplay. Instead of keeping the toy on the reader continuously, the player had to visit a designated location in the hub to read and write Skylander data.

Due to system constraints, the engine could only store **two Skylanders at a time**, and each character’s animations, abilities, and toy metadata consumed a significant portion of available memory. Combined with expanded hat assets and handheld‑specific limitations, memory pressure shaped much of the engineering work on the project.

The 3DS version was a fast‑turnaround adaptation built on Toys for Bob’s engine and an undocumented proprietary scripting system. Most of the team’s work involved rapidly implementing gameplay behaviors using the existing toolset, but several technically challenging tasks required deeper engine understanding. My standout contributions included rewriting RFID logic, expanding memory allocations for hats and character data, implementing new camera modes, supporting localization through font‑atlas updates, and reverse‑engineering the engine to learn how to implement new Skylanders.

---

## **My Responsibilities**
- Modified RFID read/write routines to support expanded packed data formats  
- Restructured memory allocations to support new Skylanders and hat assets  
- Adapted quickly to the Toys for Bob engine and scripting tools despite a complete lack of documentation  
- Added localized characters to the font atlas (coordination with artists)  
- Supported designers by implementing new camera behaviors and instructing them in their use  
- Worked with artists to ensure art assets met system requirements  
- Delivered stable systems under a compressed production schedule  

---

## **Technical Highlights**

### **1. RFID Read/Write Code for Packed Data**
Skylanders toys store character data on RFID chips in packed formats. The Toys for Bob scripting engine lacked binary and shift operations, which would normally be used to pack and unpack data into bytes. I altered the read/write logic to support new fields in the Skylanders data. This required:

- unpacking and repacking data using only basic arithmetic operators  
- correctly interpreting toy RFID data on the 3DS  
- maintaining compatibility with engine constraints, console versions, and all versions of the previous Skylanders title  

This demanded careful manipulation of data structures and a deep understanding of how the toys encoded information.

---

### **2. New Camera System**
The original camera code only supported a simple linear follow mode. Designers needed more flexibility, so I implemented:

- **Circular follow mode** — camera orbits a fixed point, keeping the player center‑screen (useful for spiral staircases)  
- **Two‑target follow mode** — camera dollies forward and back to keep two specific entities on‑screen at all times (ideal for one‑on‑one arena combat)  

These additions improved readability, supported level‑specific needs, and expanded the engine’s camera capabilities.

---

### **3. Memory Allocation Overhaul**
The number of collectible hats nearly doubled for *Giants*, since it had to include all hats from the previous title for compatibility. The hat‑selection menu had to be broken out into its own “level” (similar to a Unity scene) or the hub would be too large to fit in memory. I modified memory allocations so:

- the expanded asset set could load without crashing  
- the hat‑selection level remained stable  
- new Skylanders with larger data footprints could still load two at a time  
- the game stayed within strict handheld memory constraints  

This required “leaching” RAM from other systems and carefully balancing character, UI, and level data.

---

### **4. Reverse‑Engineering the Toys for Bob Engine**
The scripting system was one of the most unusual parts of the project.

The engine and scripting system had **no documentation**. To work effectively, I had to learn the system by:

- studying scripts from the original Skylanders game  
- reading engine source code  
- experimenting with behaviors  
- inferring conventions from existing content  

The scripting workflow was unusual: commands were selected from dropdown menus, conceptually like a primitive version of Scratch. Script files were stored in an XML format that directly represented syntax trees, making them extremely difficult for a human to read. Source control was nearly useless. Despite these constraints, I learned the system quickly and used it to support designers and implement required behaviors. I even learned how to trace commands in the XML files in Windows Notepad to track down differences from older versions.

---

### **5. Implementing New Skylanders**
New Skylanders were implemented by finding the closest matching character from the previous game, cloning its script, and modifying behaviors as needed. This workflow required:

- a deep understanding of gameplay behavior  
- adapting existing logic to new characters  
- working within restrictive scripting tools  
- ensuring stability despite limited iteration features  

This was the core production methodology for character implementation on the handheld version.

---

### **6. Localization & Font Atlas Work**
The font atlas used to display Skylander names only supported characters used in the original game. To support localized names for new Skylanders, I coordinated with artists to add new glyphs to the atlas. This required:

- understanding the asset pipeline  
- finding the exact font and size used in the previous title and reproducing it  
- finding space in the atlas for new glyphs, sometimes requiring creative placement  
- updating the glyph bounding‑box file by hand (there must have been a tool originally, but I never saw it)  
- validating that localized text rendered properly in‑game  

This was a small but important cross‑discipline responsibility.

---

## **Engineering Challenges**

### **Compressed Schedule**
The handheld version had a very short production window. All systems had to be implemented quickly and reliably.

### **Undocumented Engine**
With no documentation for the engine or scripting language, all learning came from reverse‑engineering existing content.

### **Restrictive Scripting Workflow**
The dropdown‑based scripting tool slowed iteration and required a different mental model than text‑based scripting.

### **Memory Constraints**
Expanded hats and new Skylanders pushed the 3DS memory limits, requiring careful restructuring of the hub level.

---

## **Collaboration**
I worked closely with designers who needed specific camera behaviors and gameplay interactions. I coordinated with artists on font‑atlas updates for localization, and collaborated with QA to ensure stability after modifying core systems like RFID logic and memory allocations.

---

## **Outcome**
*Skylanders: Giants* shipped on Nintendo 3DS in 2012. My contributions strengthened the engine’s capabilities, enabled expanded content, supported localization, and ensured compatibility with Skylanders toy data — all under a compressed schedule and within the constraints of an undocumented engine and restrictive scripting environment.

---

## **Links**
- **<a href="https://www.youtube.com/watch?v=yrkz282g0TE&t=143" target="_blank" rel="noopener noreferrer">Gameplay Video</a>**  
  A YouTube video showing some of *Skylanders: Giants*’ gameplay.

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>
