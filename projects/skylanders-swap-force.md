---
layout: default  
title: Skylanders SWAP Force  
---
# **Skylanders: SWAP Force**
### **Platform(s):** Nintendo 3DS  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** Toys for Bob engine, proprietary scripting tools  
### **Year:** 2013  

---

## **Overview**
*Skylanders: SWAP Force* was the most ambitious handheld entry in the franchise. Unlike previous 3DS titles, which could only load two Skylanders at a time, *SWAP Force* needed to store the player’s **entire Skylander collection** in save data and load **any** of them on demand during gameplay. This was a major shift:  

- *Spyro’s Adventure* supported **32** characters  
- *Giants* supported **56**  
- *SWAP Force* added **40 more**, for a total of **96**  
- SWAP Force characters were split into top and bottom halves, bringing the real total to **112**  

Supporting this required a complete overhaul of memory allocations, save‑data structures, UI design, and loading strategy. The scripting language also needed new capabilities to handle more complex logic and more efficient RFID operations.

The team had prior experience with the engine and a longer schedule than Giants, which allowed for deeper systems work. My contributions included building a virtual machine and toolchain for the scripting language, modifying the scripting language itself, redesigning memory architecture, generating dynamic UI assets, and writing the AI for the game’s final boss — a level that earned praise from Activision as the best in the franchise.

---

## **My Responsibilities**
- Built a stack‑based virtual machine, compiler, linker, and XML‑to‑text converter for Toys for Bob scripts  
- Modified the Toys for Bob scripting language to support binary operations and advanced math  
- Redesigned memory allocations and save‑data structures to support 96–112 Skylanders  
- Created Python tools to generate dynamic UI “level” files for Skylander selection buttons  
- Implemented a dynamic loading menu with animation‑hidden load times  
- Wrote the AI for the final boss, including flanking, weapon switching, and reactive behaviors  
- Supported designers and artists by improving scripting workflows and debugging tools  
- Delivered stable systems under a significantly expanded content load  

---

## **Technical Highlights**

### **1. Virtual Machine, Compiler, and Linker**
I was initially tasked with removing reliance on Toys for Bob’s external scripting tools by building an internal runtime. I developed:

- a **stack‑based virtual machine**  
- a **compiler** for text‑converted scripts  
- a **linker**  
- a **Python XML‑to‑text converter** for the proprietary syntax‑tree XML files  

The VM was ultimately abandoned due to the complexity of the scripting language and the time required for proper testing. However, the **XML‑to‑text converter became essential**: the XML files were extremely difficult for humans to read, and source control could not diff them properly. My converter made debugging and tracking changes feasible throughout development.

---

### **2. Extending the Toys for Bob Scripting Language**
Having learned the internals of the scripting language while building the VM, I directly modified the shipped scripting system to support:

- **binary operations**  
- **square roots**  
- **trigonometry functions**  

These additions enabled more efficient RFID access, more expressive gameplay logic, and improved performance across multiple systems. This was deep engine‑level work that expanded the capabilities of the scripting language itself.

---

### **3. Memory Architecture Overhaul**
Supporting 96–112 Skylanders required a radical redesign of memory usage.

Problems:
- Even the menu assets for the Skylander selection screen could not fit in memory at once.  
- The old model of storing two Skylanders in RAM was obsolete.  
- The game needed to load **any** Skylander on demand during gameplay.  

Solutions:
- Repurposed the second Skylander memory slot for the new loading UI.  
- Created **“level” files** containing assets for each Skylander selection button.  
- Wrote a **Python script** to automatically generate these level files from the assets.  
- Implemented a **dynamic loading menu** with:
  - four visible buttons,  
  - four off‑screen preloaded buttons (top and bottom),  
  - animations to hide load times.  

This redesign allowed the game to remain responsive while loading assets for up to 112 characters.

---

### **4. Save‑Data Expansion**
The save‑data format was expanded to store the player’s entire Skylander library, including SWAP Force’s top/bottom halves. This required restructuring how character data was stored, accessed, and updated.

---

### **5. Final Boss AI**
I wrote the AI for the final boss, which included:

- strategic flanking behavior  
- weapon switching based on player position  
- reactive logic based on player actions  

Some of this logic was reused for earlier bosses. Activision praised this boss level as **the best in the franchise**, making it one of the standout achievements of the project.

---

## **Engineering Challenges**

### **Expanded Content Load**
SWAP Force pushed the 3DS harder than any previous entry:
- more characters  
- more animations  
- more levels  
- more hats  
- more UI assets  

### **Undocumented Engine**
As with Giants, the scripting system was undocumented and stored in XML syntax‑tree files. My tools and language modifications were essential for navigating and extending it.

### **Dynamic Loading Requirements**
The need to load any Skylander on demand required careful memory juggling and UI design.

### **Complex Scripting Logic**
RFID operations and gameplay logic needed more advanced math and binary operations, prompting direct modifications to the scripting language.

---

## **Collaboration**
I worked closely with designers to support gameplay behaviors and menu interactions, collaborated with artists to ensure UI assets met system requirements, and partnered with QA to validate memory behavior and dynamic loading across the full Skylander library.

---

## **Outcome**
*Skylanders: SWAP Force* shipped on Nintendo 3DS in 2013. My contributions expanded the scripting language, redesigned memory architecture, improved debugging workflows, enabled dynamic loading of over 100 characters, and delivered one of the franchise’s most praised boss encounters.

---

## **Video**
Here is a sample of the gameplay in *Skylanders: SWAP Force*  
*(You can replace this with a preferred clip later.)*

<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe 
    src="https://www.youtube-nocookie.com/embed/yrkz282g0TE" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
    frameborder="0" 
    allowfullscreen>
  </iframe>
</div>
