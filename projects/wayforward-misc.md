---
layout: default  
title: WayForward Nintendo DS Projects  
---
# **WayForward Nintendo DS Projects**
### **Platform(s):** Nintendo DS  
### **Role:** Gameplay Programmer  
### **Engine / Tech:** WayForward internal engine, Nintendo DS SDK  
### **Years:** 2006–2008  

---

## **Overview**
These three titles represent my earliest professional game development work. They were my introduction to WayForward’s internal engine, the Nintendo DS hardware, and the realities of commercial game production. Each project taught me something different — rapid iteration under shifting design goals, direct hardware‑level programming, and the constraints of handheld 3D.

Although these games were small in scope compared to later projects, they formed the foundation of my career and proved I could deliver real, shippable gameplay under tight deadlines.

---

# **SpongeBob SquarePants: Creature from the Krusty Krab (NDS)** {#spongebob}

## **Overview**
This was my first commercial game project and my introduction to both WayForward’s engine and the Nintendo DS. The game underwent massive design changes during development, shifting from a traditional platformer with touch‑screen enhancements to a game built almost entirely around touch‑screen gestures.

Despite the upheaval, I contributed a significant amount of gameplay code, enemy behavior, animation logic, and special effects.

## **My Contributions**
- Built the **touch‑screen gesture system** using the NDS SDK  
- Implemented most of the **player gameplay mechanics**, including special moves  
- Wrote a **complex helicopter boss battle** (later cut during redesign)  
- Implemented **enemy AI** and animation behavior across multiple levels  
- Added numerous **visual effects**, including:
  - Plankton’s giant transformation (pitched‑down laugh, bullet hit effects)  
  - Player‑squash effects when heavy objects fell  
- Adapted gameplay repeatedly as the design changed  

## **Notes**
One highlight was the level where Plankton grows to giant size and fights off the military. I used his laugh as the transformation sound and pitched it down as he grew. Because giant Plankton was invulnerable, I added bullet‑hit effects on his body as planes flew past, giving the level a Godzilla/King Kong tone. I also added squash effects when heavy objects fell on the player characters — earning a reputation as “the guy who added violence to the game.”

---

# **Looney Tunes: Duck Amuck (NDS)** {#duck-amuck}

## **Overview**
Duck Amuck was based loosely on the classic cartoon short, with many minigames inspired by modern concepts rather than the original film. I wrote two of the minigames, each requiring very different technical approaches — one involving direct polygon manipulation, the other involving text input, localization, and drawing compression.

## **My Contributions**
- Wrote two full minigames:
  - **The Bleeding Black**  
  - **Chat Splat**  
- Programmed DS polygon hardware directly for dynamic effects  
- Implemented localized text‑chat gameplay  
- Added player drawing and **compressed drawings** for later quiz use  

## **Notes**
**The Bleeding Black** recreated the moment in the cartoon where the top of the frame collapses on Daffy’s head. To simulate this, I accessed the DS’s polygon hardware directly and created a dynamic “blackness” that behaved like a fabric sim dropping onto Daffy.

**Chat Splat** simulated a text chat with Daffy. The player typed phrases to push chat bubbles upward and smash Daffy into the top of the screen. Because the minigame relied heavily on text, I worked with localized versions to ensure the gameplay still functioned when the chat wasn’t in English. When designers wanted player drawings added, I wrote code to compress the drawings so they could be stored and reused in a later quiz — preventing players from scribbling nonsense.

---

# **Shrek: Ogres & Dronkeys (NDS)** {#shrek}

## **Overview**
This project was smaller in scope, and my work focused on a single minigame involving collecting fireflies. Despite its simplicity, it required careful handling of DS transparency and animation timing.

## **My Contributions**
- Wrote the **firefly collection minigame**  
- Implemented hovering and “sucked‑in” firefly behavior  
- Worked around DS transparency limitations  

## **Notes**
The minigame involved one of the babies collecting fireflies as quickly as possible. I wrote the logic for fireflies to hover and then be pulled into the baby when grabbed — convincing enough at DS resolution when paired with the grab animation. The main challenge was handling the glow transparency on the fireflies, since the DS lacked a frame buffer and transparency had to be managed carefully.

---

## **Outcome**
These early DS projects were my introduction to professional game development. They taught me how to work within strict hardware limitations, adapt quickly to changing designs, and write gameplay code that shipped. The experience I gained here — from touch‑screen gesture systems to direct polygon manipulation — became the technical foundation for the handheld and console projects that followed.

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>
