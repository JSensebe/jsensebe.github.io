---
layout: default  
title: Space Chimps  
---
# **Space Chimps**
### **Platform(s):** Nintendo DS  
### **Role:** Gameplay / Systems Engineer  
### **Engine / Tech:** WayForward internal engine, Nintendo DS hardware  
### **Year:** 2008  

---

## **Overview**
*Space Chimps* on Nintendo DS was a mix of minigames and level‑based gameplay built under tight constraints and minimal documentation. Many of the sections I owned had only a **single paragraph** of design description, requiring me to invent the gameplay, visual effects, and technical approach myself.

Several of my levels required the DS to do something it was not designed to do: **render 3D on both screens simultaneously**. Achieving this required engine‑level modifications, custom rendering tricks, and close collaboration with the art team to ensure assets matched the gameplay and technical requirements.

---

## **My Responsibilities**
- Designed and implemented multiple gameplay sections from minimal documentation  
- Modified the engine to support dual‑screen 3D rendering  
- Implemented DS‑specific rendering tricks and visual effects  
- Collaborated heavily with artists to shape gameplay and visuals  
- Created simple art assets to support custom effects  
- Delivered complete minigame experiences under tight constraints  

---

## **Technical Highlights**

### **1. Dual‑Screen 3D Rendering**
The Nintendo DS cannot natively render 3D to both screens at once. To support my levels, I engineered a custom pipeline:

- Render **one screen per frame**  
- Use the DS’s **screen capture hardware** to store the rendered frame  
- Render the other screen on the next frame  
- Display both screens simultaneously using captured buffers  

Because of DS memory layout:

- one screen must be captured into **screen memory**,  
- the other into **sprite memory**.

This required:

- **pre‑empting the engine’s sprite handler**,  
- modifying engine internals to support alternating 3D renders,  
- ensuring smooth updates despite the DS’s strict memory and timing constraints.

This was deep engine work and one of the most technically demanding parts of the project.

---

### **2. Designing Gameplay From Minimal Documentation**
Most of my sections had only a short paragraph of design text. I created:

- gameplay mechanics  
- pacing and flow  
- interactions  
- visual effects  
- moment‑to‑moment feel  

This required both engineering and design thinking, since the gameplay had to be invented, implemented, and visually supported from scratch.

---

### **3. Heavy Collaboration With Artists**
Because I was inventing much of the gameplay myself, the art team needed assets tailored to **my** requirements rather than predefined designs. This meant:

- more collaboration than usual  
- constant iteration between gameplay and visuals  
- ensuring art matched the technical constraints of DS hardware  
- providing my own simple assets when needed to unblock production

I created small but essential assets such as:

- smoke  
- dirt  
- debris  
- warp tube textures  

These supported the custom rendering effects and gameplay I designed.

---

### **4. Custom Rendering Tricks and Effects**
To achieve the look and feel of my levels within DS hardware limits, I implemented several clever effects:

#### **Billboarding distant asteroids**
Used billboards for far asteroids to reduce geometry load while maintaining depth.

#### **Smoke effects using fog + transparency without a framebuffer**
The DS has **no framebuffer**, so normal blending isn’t possible.  
I simulated smoke using fog and transparency tricks that worked within hardware constraints.

#### **Space warp sequence using texture modulation**
By stretching and modulating a few abstract textures, I created many variations for the warp effect without additional memory cost.

These techniques allowed visually rich scenes on extremely limited hardware.

---

## **Engineering Challenges**

### **Dual‑Screen Rendering**
Supporting 3D on both screens required engine modifications and careful memory management.

### **Minimal Documentation**
Gameplay had to be invented from scratch, requiring both design and engineering work.

### **Hardware Constraints**
The DS’s lack of a framebuffer, limited VRAM, and strict memory layout required creative solutions.

### **Art Integration**
Gameplay‑driven art requirements meant tight collaboration and occasional asset creation on my part.

---

## **Collaboration**
I worked closely with artists to ensure assets matched the gameplay and technical constraints. Because I was designing much of the gameplay myself, this collaboration was more intensive than usual. I also coordinated with other engineers to integrate the dual‑screen rendering pipeline into the engine.

---

## **Outcome**
*Space Chimps* shipped on Nintendo DS in 2008. My contributions included designing and implementing multiple gameplay sections, modifying the engine to support dual‑screen 3D rendering, creating custom visual effects, and collaborating closely with artists to deliver polished experiences under tight constraints.

---

## **Video**
Here is a sample of the gameplay in *Space Chimps*  
*(You can replace this with a preferred clip later.)*

<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe 
    src="https://www.youtube-nocookie.com/embed/0t8Jt8gY8uE" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
    frameborder="0" 
    allowfullscreen>
  </iframe>
</div>
