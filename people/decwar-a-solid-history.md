## **DECWAR: A Solid History**

### **Origins at UT Austin (Late 1970s)**

DECWAR was created at **The University of Texas at Austin** in 1978 for the **PDP-10** mainframe running **TOPS-10**. It evolved out of a simpler two-player game called **WAR**, itself inspired by earlier Star Trek–style text simulations.

Where WAR was essentially a two-player duel, DECWAR’s leap was radical for the time:

* many players instead of two  
* real-time shared state  
* running on a university mainframe across multiple terminals

UT students **Jeff Potter** and **Bob Hysick** led this transformation, turning WAR into DECWAR: one of the earliest large-scale, real-time multiplayer strategy games.

The **first version of DECWAR** was released in **August 1978**.

---

### **Feature Growth and Campus Culture (1979–1981)**

Between 1979 and 1981, DECWAR was refined into a sophisticated multiplayer system. Notable innovations included:

* Support for **up to 18 simultaneous players**  
* **Drop-in/drop-out play**: players could join and leave without stopping the game  
* A neutral **AI-controlled Romulan ship** to help balance underpopulated games  
* A much larger universe, eventually a **75×75 sector grid**  
* Extensive **command abbreviations** and multiple text output modes  
* Use of **shared memory** and interprocess communication for real-time concurrency

Major releases:

* **DECWAR 2.0 – July 1979**  
* **DECWAR 2.3 – November 1981**

DECWAR was even sold on **magnetic tape for $50**, which helped it spread to other PDP-10 installations and academic sites—a kind of early, semi-commercial distribution within the academic computing world.

On campus, DECWAR became part of UT’s computing culture, played from terminals across the system and remembered as a formative social and technical experience for many students.

---

### **Gameplay in Brief**

Players join either the **Federation** or the **Klingon Empire** (mechanically symmetric teams) and command a starship in a shared universe filled with:

* planets  
* starbases  
* black holes and other hazards  
* enemy and allied ships

Key mechanics include:

* **Scans** and sensors to read the strategic situation  
* **Phasers** and **torpedoes** for combat  
* **Energy and shield** management  
* **Subsystem damage** tracking (engines, weapons, etc.)  
* **Planet capture** and use of bases for repair and resupply

Because everything happens via **text commands and text output**, the game foregrounds system literacy, quick interpretation, and social interaction. Alliances, betrayals, diplomacy, and coordinated strikes all play out through text—no graphics, no voice, just mechanics and chat.

---

### **Influence on Early Online Gaming (1980s–1990s)**

DECWAR’s design and popularity helped shape the early commercial online game space. Its ideas and structure influenced:

* **MegaWars** on CompuServe (1983–1998), adapted and expanded from DECWAR-like gameplay  
* **Stellar Warrior** on GEnie (1985–1999), another large-scale online space combat game

These titles were among the earliest persistent online strategy games, making DECWAR part of the **ancestral lineage of modern MMOs and online strategy games**.

---

### **Preservation and Source Release (2010s)**

In **2011**, the **Dolph Briscoe Center for American History** at UT Austin released the original **DECWAR source code**, making it available for study and revival. The code—Fortran plus MACRO-10 assembler—was later mirrored on GitHub and other platforms.

This opened the door for three kinds of modern work:

1. **New implementations from the original design**  
2. **Restoration of the original codebase**  
3. **Cloud-native hosting for large-scale multiplayer**

---

### **Modern Work:**

#### **Eric Freeman, PhD (UT Austin Faculty)**

**Eric Freeman**, a current UT Austin faculty member, has worked from the **original Fortran and assembler sources** to build a **modern implementation of DECWAR** that:

* preserves the original game’s structure and mechanics  
* runs on contemporary systems  
* keeps gameplay as authentic as possible while shedding hardware-era constraints

Freeman’s work provides a bridge between historical software and modern development environments, making DECWAR easier to integrate into teaching and research.

---

#### **Noah Smith, PhD (UT Austin Aerospace Engineering Alumni)  — Restoration of the Original Code**

**Noah Smith** focuses on **restoring the original DECWAR codebase** itself rather than writing a new implementation.

His work includes:

* working directly with the historical Fortran and assembler sources  
* stabilizing the build process  
* getting authentic DECWAR binaries running again in historically faithful environments

This is crucial for **software archaeology and preservation**: it keeps the original artifact alive and runnable, rather than only surviving in ported or rewritten form.

---

#### **Harris Newman — decwars.com Cloud Clone**

**Harris Newman** is responsible for the **Go-based cloud clone of DECWAR at `decwars.com`**.

His work:

* reimplements DECWAR’s gameplay in **Go**  
* hosts it as a **cloud service**, allowing **large-scale multiplayer sessions** in a browser-accessible environment  
* preserves the feel and flow of the original, while leveraging modern networking and deployment tools

This Go-based clone makes DECWAR widely playable today, without requiring users to understand or maintain PDP-10 emulators.

---

### **Emulation and Community Contributions**

Beyond those three, the broader community has helped keep DECWAR alive:

* **SIMH-based PDP-10 emulation**, allowing DECWAR to run essentially as it did in 1978  
* a **reverse-engineered version by Merlyn Cousins**, aiding understanding of internal behaviors and code structure

Together with decwars.com and Freeman’s implementation, these efforts make DECWAR:

* historically grounded  
* practically playable  
* and richly analyzable for research and teaching

---

### **Why This History Matters**

Because DECWAR:

* was **born at UT Austin**,  
* influenced early commercial online games,  
* has **surviving original source**, and  
* now has **active restoration, ports, and a cloud clone**,

it stands out as one of the **best-preserved and most research-ready early multiplayer games in existence**.

It is not just a curiosity from the past—it’s a living system that allows us to study:

* multiplayer dynamics before modern graphics  
* command-line UX and system literacy  
* early networked play and real-time shared systems  
* the long-term preservation of complex, interactive software

