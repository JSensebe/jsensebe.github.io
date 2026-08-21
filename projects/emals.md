---
layout: default  
title: Electromagnetic Aircraft Launch System (EMALS) Trainer  
---
# **Electromagnetic Aircraft Launch System (EMALS) Ops and Maintenance Trainer**
### **Platform(s):** Desktop (Windows)  
### **Role:** Lead Engineer (Operations → Full Project Lead)  
### **Engine / Tech:** Unity, Animator Controllers, Nav Meshes, Microsoft Speech API (Unity wrapper), custom trainer framework  
### **Years:** 2017–2019  

---

## **Overview**
The Electromagnetic Aircraft Launch System (EMALS) trainer was one of the most ambitious simulation projects ever undertaken at ProActive Technologies. EMALS consists of two distinct sub‑trainers — **Operations** and **Maintenance** — each with its own procedures, constraints, and user workflows. I was initially assigned as co‑lead of Operations, responsible for the launch‑deck portion of the system, while another engineer led Maintenance. As development progressed, I became the sole lead for the entire EMALS project.

Operations required capabilities ProActive had never implemented before: animated human personnel, speech recognition, audible call‑outs, multi‑trainee coordination (up to five trainees at once), and complex abort/recovery logic that had to behave deterministically under all conditions. The project began with a heavy R&D phase, during which I built prototypes to validate animation systems, navigation logic, and speech recognition workflows before full production began.

I also visited the **USS Gerald R. Ford** with the lead artist to gather reference photos for flight‑deck assets and equipment. EMALS demanded a level of accuracy and procedural fidelity beyond previous trainers, and the final system became one of ProActive’s most advanced simulation products.

---

## **My Responsibilities**
- Lead engineer for EMALS Operations; later lead for the entire EMALS project  
- Designed and implemented personnel animation and movement systems  
- Built prototype characters using primitive shapes to test animation logic  
- Created animator controllers for walking, turning, strafing, and idle states  
- Implemented nav mesh–based movement and obstacle avoidance  
- Integrated speech recognition using Unity’s Microsoft Speech API wrapper  
- Implemented audible speech and call‑out logic for launch procedures  
- Designed deterministic abort/recovery logic for launch operations  
- Coordinated Operations and Maintenance asset usage to avoid conflicts  
- Mentored junior engineers in animation, UI techniques, and Unity workflows  
- Visited the **USS Gerald R. Ford** with the lead artist to gather reference photos  
- Delivered R&D prototypes that formed the foundation of the final trainer  

---

## **Technical Highlights**

### **1. Personnel Animation & Movement System**
EMALS Operations required animated human personnel moving around the flight deck — something ProActive had never built before. I began by creating prototype characters out of simple primitives (spheres and cylinders) to test animation logic without art‑asset dependencies.

I implemented:

- walking, strafing, turning, and idle animations  
- animator controllers governing state transitions  
- nav mesh navigation for pathfinding  
- dynamic obstacle avoidance  
- multi‑character coordination logic  
- deterministic movement behavior across multiple trainee stations  

Once the prototype was validated, the system was scaled to full human characters and integrated into the flight‑deck environment.

---

### **2. Speech Recognition Integration**
Trainees were required to call out specific EMALS status phrases as part of the launch procedure. Unity provided a wrapper for Microsoft’s Speech API, but the wrapper only returned the single most probable phrase. The full API supported probability lists, which would have allowed contextual weighting, but direct integration was non‑trivial.

I implemented speech recognition using the Unity wrapper and built procedural logic around its constraints, ensuring:

- reliable recognition of required call‑outs  
- integration with launch‑sequence state machines  
- audible speech feedback  
- deterministic behavior across multi‑station setups  

This was ProActive’s first trainer with speech recognition. I also recorded coworkers to provide voices for synthetic personnel, providing the audible call‑outs used during launch procedure, and cleaned up the recordings, as ProActive did not have a proper studio environment and background noise and reverberation were issues.

---

### **3. Abort & Recovery Logic**
EMALS launch procedures require the ability to abort at any moment. Some aborts are recoverable; others are not. I designed deterministic state machines that handled:

- immediate animation resets  
- safe repositioning of personnel  
- rollback of procedural steps  
- branching logic for recoverable vs. non‑recoverable aborts  
- trainee decision points following an abort  

This system ensured that Operations behaved correctly under all conditions, even with multiple trainees interacting simultaneously.

---

### **4. Multi‑Trainee Coordination**
Operations supported up to **five trainees** at once, each at a different station. This required:

- deterministic synchronization across all client machines  
  - strict synchronization was not necessary  
  - clients moved personnel when instructed and reported when they reached their destination  
  - the deterministic nature of the system ensured any differences were insignificant  
- consistent personnel animation states  
- shared procedural logic  
- real‑time updates across multiple consoles  

The multi‑trainee architecture was significantly more complex than previous trainers and required careful design to ensure reliability.

---

### **5. R&D Prototyping**
Before full production began, I built several prototypes to validate key systems:

- **Pac‑Man maze terrain for nav mesh testing**  
  - multiple routes to any location  
  - readily available reference image  
  - saved time by avoiding custom environment creation  

- **Primitive characters for animation testing**  
  - custom movement algorithms  
  - characters could combine walking, running, turning, and strafing  
  - produced a wide variety of natural‑looking movements  

- **Obstacle placement for dynamic pathing**  
- **Multi‑character movement for collision avoidance**

These prototypes demonstrated feasibility to the team and became the foundation of the final trainer, providing a roadmap for animators and automated pathing for engineers.

---

### **6. Mentoring & Team Support**
I mentored junior engineers throughout the project, teaching:

- animation controller workflows  
- nav mesh usage  
- UI texture modulation techniques (white → tinted)  
- Unity best practices for deterministic behavior  

I also demonstrated the R&D prototypes to ensure the team was confident using the systems I built.

---

## **Engineering Challenges**

### **First‑of‑Its‑Kind Systems**
EMALS was the first ProActive trainer with:

- animated human personnel  
- speech recognition  
- audible call‑outs  
- multi‑trainee coordination  
- complex abort/recovery logic  

### **Operations vs. Maintenance Asset Conflicts**
Maintenance procedures sometimes occurred on the flight deck, requiring careful coordination to avoid asset conflicts between the two sub‑trainers.

### **Strict Procedural Accuracy**
EMALS procedures are highly detailed and safety‑critical. I worked closely with SMEs and written documentation to ensure accuracy.

### **Limited Documentation**
The EMALS system was new and the procedures were evolving. Much of the system relied on SME knowledge, requiring deep familiarity with EMALS procedures. In some cases, written maintenance procedures were rendered impossible by physical reconfigurations on the ship.

### **Day/Night Conditions**
Operations required adjustments for day and night lighting conditions on the flight deck. Day and night operations required separate signaling systems: hand signals during the day and lighted batons at night, effectively doubling the number of signaling animations.

---

## **Collaboration**
I worked closely with SMEs throughout development and became deeply familiar with EMALS procedures — sometimes more familiar with specific subtopics than the SMEs themselves, who relied on memory while I worked from written procedures and reference photos.

I visited the **USS Gerald R. Ford** with the lead artist to gather reference photos for flight‑deck and maintenance‑specific assets. Our methodology was simple: the lead artist used a video camera while I took copious still photos. Naval personnel assisted us and even performed mock launches. Between us, we captured a substantial amount of reference material. I also coordinated with the Maintenance team to ensure asset consistency and avoid conflicts.

---

## **Outcome**
The EMALS trainer was deployed successfully and became one of ProActive’s most advanced trainers. The project introduced animation systems, speech recognition, multi‑trainee coordination, and complex abort/recovery logic to the company’s simulation framework. The R&D prototypes I built early in development became the backbone of the final trainer, and the systems I created were reused and extended by other engineers.

I began the project as co‑lead of Operations and ultimately became the sole lead for the entire EMALS project — a reflection of the trust placed in my engineering judgment and the reliability of the systems I delivered.

---

## **Links**
- **<a href="https://www.navair.navy.mil/nawctsd/Electromagnetic-Aircraft-Launch-System-EMALS-Operations-Ops-and-Maintenance-Maint" target="_blank" rel="noopener noreferrer">NAWCTSD's EMALS Trainer Page</a>**  
  Includes a video demo showing a couple of clips of operational procedures on the flight deck of the U.S.S. Gerald Ford at night. This video does not include audio, unfortunately.  

---

[← Back to Projects](./)

---

<p style="font-size: 0.75em;">© 2026 John Sensebe — Gameplay & Simulation Engineer</p>
