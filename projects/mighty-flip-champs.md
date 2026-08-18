---
layout: default  
title: Mighty Flip Champs!  
---
# **Mighty Flip Champs!**
### **Platform(s):** Nintendo DS  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** WayForward internal engine, Nintendo DS hardware  
### **Year:** 2009  

---

## **Overview**
*Mighty Flip Champs!* is a puzzle‑platformer built around a unique screen‑flipping mechanic that required extremely tight, deterministic gameplay behavior. I wrote the **majority of the gameplay code** and designed the game’s **horizontal blanking (H‑blank) effects**, which defined the look and feel of the flip transitions.

Although I didn’t design most of the puzzles, I worked closely with the designer because puzzle games demand pixel‑perfect consistency — players can’t be punished for being “one pixel too far to the right.” My work ensured the flip mechanic was readable, responsive, and visually distinctive.

The game performed well enough that it was later **ported to the PlayStation Portable**. I didn’t work on the port, but I was credited on it, likely because some of my gameplay logic or timing code was reused or referenced. The DS‑specific H‑blank raster effects obviously couldn’t be reused directly on PSP hardware, and the PSP version reimagined the transitions using GPU‑friendly 3D effects while matching the timing and feel of the original.

*Mighty Flip Champs!* was the first entry in WayForward’s “Mighty” series, which later included *Mighty Milky Way*, *Mighty Switch Force!*, and *Mighty Switch Force! 2*.

---

## **My Responsibilities**
- Wrote the majority of the gameplay code  
- Designed and implemented all H‑blank visual effects  
- Integrated raster effects into WayForward’s engine  
- Worked closely with the designer to ensure pixel‑perfect puzzle behavior  
- Shaped the visual feel of the flip mechanic  
- Provided technical foundations later referenced in the PSP port  

---

## **Technical Highlights**

### **1. Horizontal Blanking (H‑Blank) Effects**
The DS’s H‑blank interrupt fires once per scanline, allowing per‑line manipulation of display registers. I used this to create:

- **Vertical scaling** during the flip transition  
- **A wavy distortion** on the bottom screen  

These effects were based on earlier Game Boy Advance hobby work I had done, where I implemented more complex rotation and scaling effects. The DS version was simpler by comparison, but still required careful integration into WayForward’s engine.

I pitched the wavy effect because the H‑blank integration was already solved — it was a natural extension of the technique and added visual flair without additional overhead.

---

### **2. Majority of Gameplay Programming**
I implemented most of the core gameplay systems:

- player movement  
- collision logic  
- flip‑plane transitions  
- puzzle interactions  
- timing and state management  

Puzzle games require deterministic behavior, so the gameplay code had to be extremely precise. Movement, collision, and flip timing all needed to be consistent down to the pixel.

---

### **3. Designing the Flip Transition**
Even though I didn’t design most of the puzzles, I *did* design the visual behavior of the flip mechanic:

- the vertical scaling effect  
- the timing of the transition  
- the bottom‑screen wavy distortion  

This was a blend of technical and aesthetic design — shaping how the core mechanic *felt* to the player.

---

### **4. Tight Collaboration With the Designer**
Because puzzle games demand clarity and fairness, I worked closely with the designer to ensure:

- transitions didn’t obscure gameplay  
- movement was predictable  
- collision was pixel‑accurate  
- players were never penalized for tiny positional differences  

This collaboration ensured the game felt responsive and readable despite its unusual mechanic.

---

### **5. Technical Background: GBA → DS**
My H‑blank work originated from earlier Game Boy Advance hobby projects. The GBA version included rotation and scaling effects, so adapting the technique to the DS was straightforward — but integrating it into WayForward’s engine required careful engineering.

This background gave me a strong foundation in raster effects and scanline timing, which directly benefited the project.

---

## **Series Impact**
*Mighty Flip Champs!* was the first game in WayForward’s “Mighty” series. Although I didn’t work on the PSP port, I was credited on it, likely because some of my gameplay logic or timing code was reused or referenced. The PSP version reimagined the flip effects using its 3D hardware, but retained the timing and feel established in the DS original.

---

## **Outcome**
*Mighty Flip Champs!* shipped on Nintendo DS in 2009 and became the foundation for a multi‑game series. My contributions included writing most of the gameplay code, designing the H‑blank effects that defined the flip mechanic, integrating raster effects into the engine, and ensuring the puzzle gameplay behaved with pixel‑perfect consistency.

---

## **Video**
Here is a sample of the gameplay in *Mighty Flip Champs!*  
*(You can replace this with a preferred clip later.)*

<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe 
    src="https://www.youtube-nocookie.com/embed/6m2v2wY8VtE" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
    frameborder="0" 
    allowfullscreen>
  </iframe>
</div>
