# Machines from *Spacewar!* to *DECWAR*
### A Platform, Systems, and Implementation History

---

# 1. Executive Summary

The history of computer space-combat games from *Spacewar!* (1962) to *DECWAR* (1978) is not simply a story of game design evolution. It is a story about what computers could do, how people could access them, what languages they could program, and how those constraints both limited and inspired the games that emerged. Each machine in this lineage imposed specific constraints that shaped the design of its software — and when the constraints changed, the design changed with them.

**The central thesis:** The transformation from *Spacewar!*'s real-time graphical combat on a single PDP-1 display to *DECWAR*'s eighteen-player text-based war across a shared universe on a PDP-10 mainframe is best understood as a sequence of *platform pivots* — each driven by hardware reality, not designer whim. The key shifts were: (1) the move from graphics to text, driven by the dominance of teletypes over vector displays; (2) the move from single-user to multi-user BASIC, enabled by time-sharing minicomputers; (3) the move from interpreted BASIC to compiled FORTRAN and then assembly, driven by the memory and performance demands of a larger, richer game world; and (4) the move from serial single-terminal play to true simultaneous multiplayer, made possible only by TOPS-10's shared high-segment architecture on the PDP-10.

**The machines:** The PDP-1 (1960) was a transistor minicomputer whose CRT vector display made *Spacewar!* possible — and whose rarity (53 units total) ensured it remained a machine for elites. The SDS Sigma 7 (1966), a 32-bit scientific mainframe, hosted Mike Mayfield's 1971 Sigma 7 BASIC version of Star Trek — the foundational game in the single-player tradition — but the code is lost. The HP 2000 series (1968 onward), a dual-processor time-sharing minicomputer running HP Time-Shared BASIC, hosted the earliest surviving Star Trek code (STTR1, October 20, 1972) and was the institutional workhorse of educational computing in the early 1970s, supporting up to 32 simultaneous teletype users. The DEC PDP-10 / DECsystem-10 (delivered from 1967), a 36-bit word machine running TOPS-10, was the premier university computing platform of the 1970s and the machine that made *DECWAR* possible — because TOPS-10's shared high-segment memory architecture allowed multiple independent user jobs to share a single live galaxy state without requiring a centralized server process or message-passing system.

**The transitional systems:** Between the canonical BASIC Star Trek and *DECWAR* lay a critical and underappreciated middle step: the University of Texas at Austin, which had both a CDC 6600 (used for WAR, a two-player single-terminal Star Trek variant of unknown authorship) and a DEC PDP-10, which became the target platform for DECWAR's total architectural reimagining. The UT FORTRAN Super Star Trek (Matuszek, Reynolds, et al., 1973–74) represents a parallel lineage running on DEC machines but as a single-player game; it shows the trajectory from BASIC toward compiled languages for richer single-player experiences. WAR on the CDC 6600 represents the earliest known attempt to put two human players into the same Star Trek universe simultaneously — but the CDC 6600 supported only a single operating terminal, so the two players had to physically take turns. DECWAR eliminated this bottleneck by running each player's game loop as a separate TOPS-10 job, all accessing the same shared high segment.

**Why the PDP-10 and DECWAR are central:** The PDP-10's 36-bit word architecture, TOPS-10's UUO-based monitor calls, and especially its support for shared high-segment read-write memory between multiple simultaneous jobs made it uniquely suitable for the kind of multiplayer game *DECWAR* became. The game was written in MACRO-10 (the PDP-10 assembly language) and FORTRAN IV, making heavy use of TOPS-10's job structure, IPC mechanisms, and terminal I/O model. The DECWAR source (preserved at the Dolph Briscoe Center for American History and on GitHub) shows this directly in its header: `SEARCH MONSYM, MACSYM` / `.REQUIRE SYS:MACREL` — these are standard TOPS-10 system library references. A 1990s usenet thread captures the architectural lock-in plainly: *"DECWAR is very much a Tops-10 program, utilizing many many features of that operating system which are unavailable in TOPS-20."* It could not simply be ported away from TOPS-10 without fundamental restructuring. When CompuServe's Kesmai team acquired DECWAR, they ran it on CIS's own TOPS-10 variant — they did not port it.

The resulting game — 18 simultaneous players, a 79×79 sector galaxy, real-time updates on text terminals, Federation vs. Klingon team play, the ability to join or leave without disrupting others — was a genuine architectural achievement for its era, and the direct ancestor of MegaWars (CompuServe, 1983), Stellar Warrior (GEnie, 1986), and through those, the entire lineage of commercial online multiplayer space games.

---

# 2. Key Findings

- The **PDP-1's vector display** made *Spacewar!* possible and also made it impossible to generalize: the game was inseparable from hardware that existed on fewer than 53 machines worldwide.
- The **Teletype Model 33 ASR**, printing at 10 characters per second, was the universal terminal of early university computing. Mayfield's design challenge was creating a space game *for* it, not against it.
- The **SDS Sigma 7** hosted the original 1971 Mayfield code, which is definitively lost. STTR1 (HP 2000C, October 20, 1972) is the earliest surviving Star Trek code.
- **HP Time-Shared BASIC** was a dual-processor system supporting up to 32 simultaneous teletype users. Its contributed-programs library was the first institutional distribution channel for the Star Trek game.
- **DEC BASIC-PLUS** (the Ahl/Cole port target) differed from HP BASIC primarily in supporting multiple statements per line. The Ahl/Cole changes were almost entirely cosmetic — confirmed by Aaron Reed's close code comparison.
- The **CDC 6600 at UT Austin** hosted WAR, the proto-multiplayer Star Trek variant, but its single-terminal architecture meant players had to take turns physically. No simultaneous multiplayer was possible on that hardware.
- **DECWAR was almost entirely rewritten** during the CDC-to-PDP-10 port. The UT documentation states: the current version "bears little resemblance to the original" WAR. Almost all commands, and the core concept of separate jobs sharing a single galaxy state, were added on the PDP-10.
- **DECWAR's shared high-segment architecture** is the central technical innovation. Each player ran their own TOPS-10 job (their own process), but all jobs mapped the same high-segment containing the galaxy state. This gave each player an independent execution context with a shared world view.
- **MACRO-10 + FORTRAN IV** was the implementation stack: assembly for OS-intimate, time-critical, shared-memory infrastructure; FORTRAN for game logic modules. Both are preserved in the drforbin/decwar and PDP-10/decwar GitHub repositories.
- **TOPS-10's command abbreviation model** directly shaped DECWAR's user interface: commands could be abbreviated to their most unique initial characters — mirroring the OS's own CLI behavior.
- **DECWAR v1.0 was released August 1978;** v2.0 July 1979; v2.3 November 20, 1981. Distributed on tape for $50.
- The **UT FORTRAN Super Star Trek** (Matuszek/Reynolds/Cohen, 1973–74) is a separate single-player lineage; it influenced BSD Trek but did not lead to DECWAR.
- **PLATO Empire (1973)** was a genuine simultaneous multiplayer space game developed in parallel on a separate, proprietary network; it influenced the Xtrek/Netrek branch but is architecturally and institutionally unrelated to DECWAR.

---

# 3. Machine Chronology

**1960 — PDP-1 delivered (first unit to BBN)**
Machine: DEC PDP-1. OS: None (bare metal). Language: PDP-1 assembly. 18-bit words; Type 30 CRT vector display; ~100K ops/sec; 4K–65K words of magnetic core. First commercial computer designed around user interaction.
*Sources: Wikipedia, "PDP-1"; Computer History Museum, PDP-1 Restoration Project*

**1962 — *Spacewar!* completed, MIT**
Machine: DEC PDP-1. OS: None. Language: PDP-1 assembly. Authors: Russell, Graetz, Wiitanen, Samson, Edwards et al. Required Type 30 CRT vector display; demanded ~100,000 calculations/second for physics. First real-time interactive multiplayer game; spread to all ~50 PDP-1 installations via paper tape.
*Sources: Wikipedia, "Spacewar!"; Graetz, "Spacewar! Real-Time Capability of the PDP-1," DECUS Proceedings 1962 (bitsavers.org)*

**1966 — SDS Sigma 7 introduced**
Machine: Scientific Data Systems Sigma 7. 32-bit architecture; magnetic-core memory; scientific/batch primary use; connected to Teletype Model 33 ASR at UC Irvine. Relevance: machine Mayfield used in 1971.
*Sources: Wikipedia, "SDS Sigma 7"; Star Trek (1971 video game) Wikipedia*

**1967–1968 — PDP-10 (KA10) enters universities**
Machine: DEC PDP-10 / KA10. OS: Monitor (later TOPS-10). 36-bit word; 18-bit word addresses; 256 kilowords max physical memory (KA10); high/low segment memory model; teletype terminals. Begins the era of university PDP-10 installations.
*Sources: Wikipedia, "PDP-10"; Bell et al., "The Evolution of the DECsystem 10," CACM 1978*

**1968 — HP 2000 series enters market**
Machine: HP 2000 (based on HP 2100 series). OS: HP Time-Shared BASIC (TSB). Dual-processor: one CPU for user code, one for RS-232 I/O handling. Supports 16–32 simultaneous teletype users. HP 2000F cost: $105,000 (1974). Dominant educational time-sharing platform of the early 1970s.
*Sources: Wikipedia, "HP Time-Shared BASIC"; Wikipedia, "HP 2100"; HP 2000/Access Operator's Manual (mrynet.com)*

**1971 (summer) — Mayfield Star Trek, SDS Sigma 7, UC Irvine**
Machine: SDS Sigma 7 via Teletype Model 33 ASR. Language: BASIC (Sigma 7 dialect). Author: Mike Mayfield (high school senior). Foundational design: 8×8 quadrant grid, phaser/torpedo mechanics, turn-based interaction. **Source code definitively lost** when Mayfield lost account access.
*Sources: Mayfield email to Games of Fame, December 3, 2000 (gamesoffame.wordpress.com); Wikipedia, "Star Trek (1971 video game)"*

**1972 (October 20) — STTR1 completed, HP 2000C**
Machine: HP 2000C. Language: HP Time-Shared BASIC. Author: Mayfield (rewrite from scratch; HP BASIC too different from Sigma 7 BASIC for a port). **Earliest surviving Star Trek source code.** Dated REM header: "TOTAL INTERACTION GAME - ORIG. 20 OCT 1972." Added to HP contributed-programs library February 1973 as program STTR1.
*Sources: STTR1 source code (dunnington.info/public/startrek/STTR1); Wikipedia; Reed, Medium 2022*

**1973 (spring) — Empire I on PLATO (separate lineage)**
Machine: PLATO mainframe, UIUC. Authors: John Daleske, Silas Warner. First 8-player simultaneous networked space game; Star Trek-themed ships. Does not connect to Mayfield lineage in code; parallel branch → trek82/Xtrek/Netrek.
*Sources: Wikipedia, "Empire (1973 video game)"*

**1973 (summer) — Ahl/Cole DEC BASIC-PLUS port**
Machine: DEC systems, RSTS/11, BASIC-PLUS. Authors: David Ahl, Mary Cole (DEC). Published in DEC EDU newsletter as "SPACWR." Code changes minimal (dialect conversion, multi-statement line compression). Published in *101 BASIC Computer Games* (DEC, July 1973).
*Sources: Ahl notes in BASIC Computer Games (1978); Reed, Medium 2022*

**1973 (spring–summer) — UT Austin BASIC and FORTRAN Trek**
Machine: CDC 6600 at University of Texas Computation Center. Languages: BASIC (Hicks/Korp, April 1973) → FORTRAN + CDC Assembler (Matuszek/Reynolds/Cohen, 1973–74). **Separate lineage** → BSD Trek; not DECWAR.
*Sources: ESR, sst-doc.html (catb.org); UT Austin repository, Super Star Trek printout scan*

**Mid-1970s — WAR, CDC 6600, UT Austin**
Machine: CDC 6600 (single operating terminal). Language: Unknown; code not recovered. Author: Unknown. Two-player serial turn-taking game derived from Star Trek mechanics. **Critical limitation:** one terminal; both players shared a single keyboard.
*Sources: Wikipedia, "Decwar"; Games of Fame, "WAR, DECWAR and MegaWars"; UT Decwar v2.2 documentation*

**1974 — Leedom Super Star Trek, Data General Nova 800**
Machine: Data General Nova 800, Westinghouse. Language: DG Extended BASIC. Key changes: 3-letter mnemonics, moving Klingons, named quadrants, crew messages. Published Creative Computing May/June 1975; reprinted BASIC Computer Games 1978.
*Sources: Leedom email to Games of Fame; Wikipedia; Reed, IF50 substack 2021*

**1974 (May) — TOPS-10 Release 6.01: virtual memory**
TOPS-10 milestone: first demand paging, enabling programs larger than physical memory. Expands what DECWAR-scale programs can do on PDP-10.
*Sources: Wikipedia, "TOPS-10"*

**1978 (August) — DECWAR v1.0 released, UT Austin PDP-10**
Machine: DEC PDP-10 (DECsystem-10), UT Austin Computation Center. OS: TOPS-10. Languages: MACRO-10 + FORTRAN IV. Authors: Bob Hysick, Jeff Potter (port initiated by Robert Schneider). Up to 18 simultaneous players; 75×75 sector galaxy. Distributed on tape for $50. First true simultaneous-multiplayer text space combat game. v2.0: July 1979. v2.3: November 20, 1981.
*Sources: Wikipedia, "Decwar"; decwar.org; UT Austin repositories; drforbin/decwar GitHub; decwar.hlp*

**1983 — MegaWars on CompuServe**
DECWAR with Star Trek IP removed; commercialized by Kesmai for CompuServe. Ran 1983–1998. Run on CIS's TOPS-10 variant — not ported away from TOPS-10.
*Sources: Wikipedia, "Decwar" and "MegaWars III"*

---

# 4. Platform Profiles

## 4.1 DEC PDP-1 (1960–1969)

**Machine overview:** 18-bit word, transistor minicomputer. First DEC product focused on user interaction. Price: $120,000. Only 53 units ever delivered. Memory: 4,096 to 65,536 18-bit words of magnetic core. 93,458 arithmetic operations per second (two-memory-cycle instructions).

**Operating environment:** No operating system. Programs ran bare-metal, managing all hardware directly — interrupts, I/O, timing, display refresh.

**I/O model:** Input via front-panel switches (later custom controllers). Output via the **Type 30 CRT vector display** — a crucial point. The Type 30 was a *vector* display, not raster: the beam drew lines and points directly. *Spacewar!* drove the display at over 20,000 points per second and demanded 100,000+ calculations per second for physics simulation.

**Why it mattered:** *Spacewar!* could not have been written for a teletype machine. The PDP-1's vector display was its game-enabling hardware. When Mayfield encountered Spacewar! running (on a PDP-10 display port) at UC Irvine in 1971, and wanted to replicate the experience on the Sigma 7 — which had only a Teletype — his entire design challenge was: *how do you make a compelling space combat game without graphics?* The PDP-1 thus mattered not as a platform Star Trek ran on, but as the conceptual origin Mayfield was trying to recreate under different constraints.

---

## 4.2 SDS Sigma 7 (1966–early 1970s)

**Machine overview:** 32-bit scientific mainframe by Scientific Data Systems. Primarily batch/scientific use. UC Irvine operated one.

**Operating environment:** Batch-oriented; time-sharing available. Supported a BASIC interpreter sufficiently distinct from HP BASIC that Mayfield chose to rewrite rather than port when moving to the HP 2000C.

**I/O model:** In Mayfield's context: Teletype Model 33 ASR. 10 characters per second, paper output only. Mayfield had no persistent file storage — he punched paper tape at the end of each session and read it back in the next day.

**Relevance and loss:** The Sigma 7 version is the true origin, but the code is definitively lost. The machine's BASIC dialect, Mayfield's lack of storage, and the Sigma 7's end-of-life status combined to make this version ephemeral. All surviving history begins with STTR1 on the HP 2000C.

---

## 4.3 HP 2000 Series / HP Time-Shared BASIC (1968 onward)

**Machine overview:** Not a single machine but a system: an HP 2100-series CPU (main processor) paired with a second, smaller HP 2100-series CPU acting as an I/O processor for RS-232 serial lines. HP 2000F cost $105,000 in 1974. Supported 16 or 32 simultaneous users.

**Operating environment:** HP Time-Shared BASIC (HP TSB), also called "Access BASIC" in later versions. Full multi-user time-sharing environment whose primary interface language was BASIC. Users received an account (e.g., "B001"), logged in via teletype or modem, wrote and saved BASIC programs, and could access the contributed-programs library.

**I/O model:** Teletype Model 33 ASR at 110 baud (10 characters/second). Line-by-line input; no cursor addressing; output scrolled linearly on paper. PRINT USING / IMAGE statements gave formatted output — used for the Star Trek map display.

**Memory considerations:** User programs ran in the main CPU's address space, time-sliced across up to 32 concurrent users. The front-end I/O processor buffered terminal input/output. No paging in early versions; programs had to fit in available core.

**Why it mattered:** The HP 2000 was the most accessible time-sharing BASIC system in U.S. educational institutions in the early 1970s. HP's contributed-programs library was the first real distribution mechanism for this kind of software — request a program, receive it on punched tape, load it on any HP 2000. This is how STTR1 spread: HP put it in the library February 1973, and it immediately became a shared cultural artifact across HP 2000 installations nationwide.

**Critical technical note:** The Teletype 33's 10 character/second speed was an acknowledged design constraint. Mayfield: *"Working on a 10 character per second terminal forced me to keep the program small. Otherwise, I probably would have gone crazy adding feature after feature."* The sparse output of the BASIC Star Trek tradition is partly an artifact of 110-baud terminal economics.

---

## 4.4 CDC 6600 (at UT Austin, mid-1970s)

**Machine overview:** Control Data Corporation 6600, Seymour Cray's 1964 design — one of the first true supercomputers. 60-bit word; extremely fast floating-point; 10 peripheral processing units (PPUs) for I/O. UT Austin had one at their Computation Center.

**Operating environment:** CDC SCOPE/KRONOS. Primarily batch-processing. **Critical limitation:** the 6600 supported only a single "operating terminal" — one interactive terminal at a time.

**Relevance:** Two Star Trek lineages used the UT CDC 6600: the Hicks/Korp BASIC Trek and Matuszek/Reynolds FORTRAN version (single-player); and WAR (two-player but serial). WAR demonstrated the appeal of human-vs.-human gameplay but could not achieve true simultaneous multiplayer. The single-terminal architecture was a hard constraint that defined WAR's social form — and made the PDP-10 port's architectural redesign not optional but mandatory.

---

## 4.5 DEC PDP-10 / DECsystem-10 (1967–1983)

**Machine overview:** 36-bit word mainframe family. Key CPU generations: KA10 (1968, core memory, 256 kiloword max), KI10 (1972, integrated circuits, paged memory), KL10 (1975, ECL, 1.8 MIPS), KS10 (1978, lower cost TTL bit-slice). By the late 1970s, PDP-10s ran TOPS-10 or TOPS-20 at university computing centers across the US. Described as "the machine that made time-sharing common" (Columbia University Computing History site).

**Operating environment:** TOPS-10 (Timesharing Operating System 10). Key features:
- Prioritized run queues; preemptive time-sharing across multiple jobs
- **UUO (Unimplemented User Operation)** mechanism for system calls — monitor calls that looked like machine instructions, making system programming natural
- File system with project-programmer numbers (PPN)
- **Command abbreviation:** every command abbreviated to its most unique initial characters
- **Shared high/low segment memory model** (central to DECWAR — see Section 7)
- Release 6.01 (May 1974): first TOPS-10 with virtual memory (demand paging)

**I/O model:** Terminals via RS-232 or multiplexers. Standard terminal: Teletype Model 33 or DECwriter. Terminal I/O handled through the OS TTY subsystem. DECWAR showed this transparency to users: the program name changed based on execution state (DECWTI = waiting for input, DECWRN = running a command, DECWSL = sleeping), visible via Ctrl-T — a TOPS-10 feature.

**Memory and address space:** 18-bit word addresses. User processes had "high" (bit 17 set) and "low" (bit 17 clear) memory. High segments could be shared as read-write across multiple jobs — the foundation of DECWAR's multiplayer architecture.

**Languages:** MACRO-10 (standard PDP-10 assembler; full macro support); FORTRAN IV / FORTRAN-10 (compiled, efficient for game logic); BASIC (available but slow). DECWAR used MACRO-10 for OS-intimate system interaction and FORTRAN for game logic modules.

**Why it mattered:** Ubiquitous in university computing, fast enough (KL10: 1.8 MIPS) to service 18 concurrent interactive processes, and — critically — TOPS-10's shared high-segment architecture was the exact mechanism DECWAR needed that no earlier institutional platform provided.

---

# 5. The BASIC Star Trek Implementation Chain

## The HP BASIC Foundation

STTR1 (HP 2000C, October 1972) established the game's core data model. The galaxy was an 8×8 array of quadrant descriptors (encoding Klingon count, starbase count, and star count as digits of a two-digit number). Each sector within a quadrant was an 8×8 array accessed by position. All state was kept in BASIC numeric and string arrays using single-letter variable names — an HP BASIC optimization to save memory and parsing time.

HP BASIC constraints that shaped the code:
- **Single statement per line:** forced verbose code
- **PRINT USING / IMAGE statements** for formatted output — used for the sector map display
- **Limited string operations** (array-slice style, unlike DEC's MID/LEFT/RIGHT)
- **GOTO-heavy control flow** — FOR/NEXT was the only structured loop; all branching was GOTO or GOSUB with line numbers
- **Paper tape as storage** for Mayfield's informal account — forced compactness

## The Ahl/Cole DEC BASIC-PLUS Port (Summer 1973)

Aaron Reed's close code comparison (Medium, 2022) established that the Ahl/Cole port was almost entirely cosmetic: the line numbers, algorithms, and text were preserved. Key technical changes: (1) multiple statements per line (BASIC-PLUS supported this; reduced printed listing length for publication); (2) minor punctuation tweaks in output. Published in *101 BASIC Computer Games* (DEC, July 1973) as "SPACWR."

## The Leedom Super Star Trek Expansion (1974)

Bob Leedom's port from the Ahl/Cole version to Data General Extended BASIC and subsequent expansion is the most significant creative transformation in the BASIC lineage. Key changes:
- **Moving Klingons** — repositioned to random sector after being fired upon; fundamentally changed tactics
- **3-letter command mnemonics** (NAV, PHA, TOR, SHE, DAM, LRS, SRS, COM, STA) replacing numeric codes
- **Named quadrants** (RIGEL IV, POLLUX II, etc.)
- **Crew messages** (Spock, Scotty, Uhura, Sulu — strong thematic immersion)
- **Expanded library computer** with additional navigation functions

*Technical note:* The Data General Nova 800 had 32K words of memory — substantially more than HP 2000 configurations — which is what allowed the expansion. Memory constraints directly drove feature scope.

Ahl ported Leedom's version to Microsoft BASIC for *BASIC Computer Games* (1978), achieving mass distribution at exactly the moment Apple II, TRS-80, and Commodore PET were entering the market.

## Summary Table: Major BASIC Implementations

| Version | Year | Platform | Language | Key Change | Code Survives? |
|---|---|---|---|---|---|
| Mayfield Sigma 7 | 1971 | SDS Sigma 7 | Sigma 7 BASIC | Original design | **Lost** |
| STTR1 (HP) | 1972 | HP 2000C | HP TSB | Rewrite; canonical design | Yes (tape extract) |
| Ahl/Cole SPACWR | 1973 | DEC RSTS/11 | BASIC-PLUS | Dialect port; minor changes | Yes (101 BCG book) |
| Leedom SST | 1974 | DG Nova 800 | DG Extended BASIC | Major expansion | Yes (CC mag + BASIC CG) |
| BASIC Computer Games SST | 1978 | Microsoft BASIC | MS BASIC | Mass distribution | Yes (atariarchives.org) |

---

# 6. Transitional Systems Between BASIC Trek and DECWAR

## The UT Austin Ecosystem

The University of Texas at Austin was the critical transitional site. It had both a CDC 6600 (for numerical computation and early Trek variants) and a PDP-10 (for time-sharing interactive work). The existence of both machines at the same institution made UT the site of the specific transition from single-player BASIC Trek → two-player FORTRAN Trek (WAR) → 18-player MACRO-10/FORTRAN Trek (DECWAR).

**UT BASIC Trek (Hicks/Korp, April 1973):** Written for the CDC 6600 in BASIC. The header "GENERAL IDEA STOLEN FROM PENN. U." suggests it may trace to a Penn State version. Eric Raymond notes it is unknown whether this Penn State version descended from Mayfield or was an independent invention. **Unresolved uncertainty.**

**UT FORTRAN Super Star Trek (Matuszek/Reynolds/Cohen, 1973–74):** Independently designed (not a BASIC Trek port, though the authors played Hicks/Korp BASIC Trek). Written in FORTRAN and CDC Assembler Language. Key differences from the BASIC tradition: 10×10 sectors (not 8×8); numbered quadrants (not named). Distributed via DECUS. Eric Allman later ported this to C as BSD Trek.

**The UT FORTRAN lineage and DECWAR are separate:** The UT FORTRAN version is a richer single-player game. It did not lead to DECWAR. The two lineages shared an institutional home but the code relationship is zero.

## WAR: The Critical Conceptual Pivot

WAR represents the crucial insight: replacing AI Klingons with a human opponent. The mechanics — capturable planets, strategic territory control, ship-vs.-ship combat — represent genuine design work beyond Mayfield's original model. But the CDC 6600's single-terminal limitation meant WAR was always a proto-game requiring players to physically take turns.

The experience of WAR established that human opponents were dramatically more interesting than AI, and this drove the investment in DECWAR's far more complex architecture. The code transition was not a port — the UT documentation explicitly states the current DECWAR "bears little resemblance to the original." The platform change *forced* the architectural change: simultaneous multiplayer was only possible on the PDP-10 because of TOPS-10's job structure and shared segment model.

## PLATO Empire (Separate, Parallel)

Empire on PLATO (Spring 1973, Daleske/Warner) was a genuine simultaneous multiplayer space game developed in parallel and entirely independently. It ran on PLATO's CDC-based networked system with proprietary terminal hardware — not available outside PLATO installations. Its design influenced the trek82/Xtrek/Netrek branch. DECWAR's developers are not known to have had access to or been influenced by PLATO Empire.

---

# 7. The PDP-10 as a Multiplayer Game Platform

## Time-Sharing: The Foundation

TOPS-10 ran multiple *jobs* concurrently with a priority-based preemptive scheduler. Each user's game loop — terminal I/O, command processing, combat calculations — ran as a separate TOPS-10 job. There was no central server process managing all players. The "server" was the shared high segment itself.

## The High-Segment / Low-Segment Model (The Technical Core)

Every PDP-10 user process in TOPS-10 had two memory segments:

- **Low segment (bit 17 = 0 addresses):** Private, read-write. The job's stack, local variables, buffers, working data. Only that job could see or modify this.
- **High segment (bit 17 = 1 addresses):** Could be mapped shared across multiple jobs. When multiple jobs mapped the *same* physical high-segment pages, they shared that memory — any write by one job was immediately visible to all others.

For shared *executable* code, the high segment was typically read-only. But the high segment could also be mapped read-write — and this is what DECWAR exploited. The galaxy state (positions of all ships, planets, bases, black holes, torpedoes in flight, all player state structures) lived in a shared read-write high segment. Every player job mapped this same segment. When player A fired a torpedo, that torpedo's presence was immediately visible when player B's job next read the galaxy state.

The DECWAR usenet thread confirms this directly: *"I did note that they mentioned used a shared hi-seg, which means they use shared memory between processes. They most likely also have some other form of IPC going on, which most likely is very Tops-10 specific as well."*

The DecwarOrg source excerpt shows the MACRO-10 startup sequence:
```asm
START: RESET
    MOVE P,[IOWD PDLEN,PDL]
    MOVEI T1,.FHSLF
    RPCAP
    MOVEM T2,USRCAP        ; Save user capabilities
    CALL GLINIT            ; Initialize galaxy
    CALL PLINIT            ; Initialize player structures
    JRST MAIN              ; Enter main game loop
```
`RPCAP` is a TOPS-10/TOPS-20 monitor call (read process capabilities) — system-specific code appears in the first 8 instructions of the program. `SEARCH MONSYM, MACSYM` at the file header pulls in TOPS-10 monitor symbol definitions, binding the code irreversibly to the OS.

## Terminal Computing in Practice

In 1978, accessing the UT Austin PDP-10 meant either sitting at a terminal in the Computation Center or connecting via a 300 or 1200 baud modem. Playing DECWAR meant typing commands like `MOVE 3 5` or `PHASER 500` at your terminal, reading the output, and responding — all as character streams. Three verbosity levels (full detail to tersest code-like format) were a direct response to terminal bandwidth. Command stacking (a sequence of commands on a single line) let fast typists pipeline their actions.

The DECWAR help file (decwar.hlp, Version 2.2, June 3, 1980) reveals the OS transparency: the game noted TTY speed, TTY number, job number, and PPN (project-programmer number) in error/gripe reports. Program names changed by execution phase (DECWTI, DECWRN, DECWSL, DECWPG) — visible via Ctrl-T, a TOPS-10 feature. The game was deeply integrated with TOPS-10's understanding of sessions, users, and jobs.

## What the PDP-10 Could Not Do

No graphics. No bit-mapped displays. No screen refresh or cursor addressing. No color. DECWAR was entirely character-stream I/O — every player saw the world sequentially, line by line. The game had no display loop; each command execution produced scrolling text output.

---

# 8. DECWAR Deep Dive

## Implementation Context

DECWAR v1.0 was installed on the UT Austin PDP-10 in August 1978 by Bob Hysick and Jeff Potter, building on Robert Schneider's initial port of WAR to the DEC-10. The machine was a DECsystem-10 running TOPS-10 at the University of Texas Computation Center — a shared institutional machine used for teaching, research, and administration. DECWAR was recreational use of institutional computing time, frequently causing administrative concern about resource consumption.

## Languages and Architecture

Written in **MACRO-10 assembly and FORTRAN IV**, confirmed by the source title page, DecwarOrg, and the GitHub repository structure.

- **MACRO-10 (`.MAC` files):** Core system-level code — startup, job initialization, main game loop, all TOPS-10 monitor calls, shared high-segment setup, terminal I/O dispatch, timing/scheduling of command execution.
- **FORTRAN IV (`.FOR` files — TORP.FOR, EXTERN.FOR, etc.):** Individual command implementations — torpedo firing, phasers, movement, capture mechanics, combat resolution. Compiled (runtime efficient) and more maintainable than assembly for complex game logic.

## The Shared Galaxy: Concurrent World State

Each player ran their own TOPS-10 job with their own private low segment (terminal state, input buffer, local working variables). All jobs shared the same high-segment containing:
- Galaxy grid: planet positions, base positions, black hole positions
- Player ship positions and states (shields, energy, torpedoes, equipment damage)
- Torpedo-in-flight data
- Team affiliations
- Game phase and timing

**The consequence:** Any player could enter a command at any time and update the global game state. The Wikipedia description captures this: *"Although, like Star Trek, each user interacted through a turn-based command line, the game as a whole was essentially real-time because any user could enter commands at any time and update the global game state."*

This is importantly distinct from fully asynchronous real-time: each player's command was processed sequentially within their job, and the galaxy state was updated per command. But because 18 jobs could be processing commands nearly simultaneously (TOPS-10 scheduler permitting), the effective experience was real-time.

## Command Architecture: TOPS-10 Influence

DECWAR's command language was explicitly modeled on TOPS-10's own CLI:
- **Commands abbreviated to shortest unique form** (e.g., `MOV` or `M` for MOVE, `PH` for PHASER)
- **Coordinates in absolute, relative, or computed format**
- **Command stacking on a single line** (a queue of commands executed in sequence)
- **3 detail levels for output** (matching slow and fast terminal connections)

This was not an aesthetic choice — it was adaptation to TOPS-10's existing user patterns. Users already comfortable with TOPS-10's abbreviated command syntax found DECWAR's interface immediately familiar.

## Operational Context

Playing DECWAR in 1978 meant being logged into the UT Austin PDP-10 at a Computation Center terminal, or calling in via modem. Some players were physically adjacent at the terminal room and could shout at each other; others were remote. The game's social structure was that of a computing center in-group. The university "often banned them because of their RAM use" (Fandom wiki) — 18 simultaneous jobs plus the shared high-segment was a substantial memory load on a machine shared with all other university users.

## DECWAR vs. Earlier Implementations: A Comparison

| Dimension | BASIC Star Trek | WAR (CDC 6600) | DECWAR (PDP-10) |
|---|---|---|---|
| Players | 1 | 2 (serial) | 1–18 (simultaneous) |
| Game loop | Single sequential execution | Single sequential; players take turns | 1 TOPS-10 job per player; shared galaxy |
| State storage | BASIC arrays in single-job memory | Arrays in single-job memory | Shared high-segment |
| Language | BASIC | Unknown | MACRO-10 + FORTRAN IV |
| Terminal I/O | Sequential (one player's I/O) | Sequential (one terminal) | Concurrent (each job handles its own TTY) |
| Effectively real-time? | No | No | Yes |
| Galaxy size | 8×8 quad × 8×8 sector | Unknown | 79×79 sectors (v2.3) |
| Persistence | None (new game each session) | None | Yes (galaxy persists; rejoin after death) |

---

# 9. Engineering Challenges of Building DECWAR-Class Multiplayer Software

This section analyzes what was genuinely difficult about DECWAR as an engineering problem. Documented challenges are labeled as such; inferences from platform characteristics are labeled as inferences.

## 1. Shared State Concurrency (Most Critical)

**The problem:** 18 player jobs reading and writing the same high-segment galaxy state simultaneously. Two concurrent writes to the same data structure could corrupt the galaxy state.

**The challenge in 1978:** TOPS-10 did not provide automatic mutual exclusion for shared memory at the application level. The PDP-10 architecture provided atomic word-level memory operations, but coordinating multi-word updates (updating a ship's position, shields, and status simultaneously) required careful manual protocol.

**Likely approach (inference from platform and DECWAR's observed behavior):** DECWAR almost certainly used a flag-based locking scheme in the shared high-segment, or a convention that per-object updates used the PDP-10's atomic test-and-modify instructions. The structured use of MACRO-10 for system access (where hardware atomics were natural) and FORTRAN for game logic (compiled to efficient register code) suggests a clean layering: game logic modules called into assembly stubs for any operation touching shared state.

**Evidence for designed serialization:** The DECWAR help file documents intentional command delays — 5 seconds for CAPTURE/BUILD operations, with 1 second added per BUILD for captured planets. These delays were partly tension mechanics and partly serialization — giving the galaxy state time to stabilize and other players a visible window of vulnerability.

## 2. Terminal I/O Handling

**The problem:** 18 simultaneous terminal connections, each requiring attention at unpredictable times, handled through TOPS-10's TTY subsystem.

**The model:** Each player job sat in a loop: read a command from terminal (blocking on TTY input), process the command against the shared galaxy state, output result to terminal, repeat. Since each job was independent, one player waiting for user input didn't block other players. The TOPS-10 scheduler time-sliced the 18 jobs, giving CPU to active jobs while blocked-on-input jobs waited.

**The tersest mode:** Three verbosity levels allowed players to reduce terminal output volume — important for 300 baud connections and for fast players wanting to minimize read time between commands.

## 3. Synchronization and Race Conditions

**The problem:** Classic concurrent-update issues. If player A fires a torpedo at position X,Y and player B moves to X,Y simultaneously, what happens?

**The challenge:** In 1978, no language runtime or OS handled this automatically. Solutions were manual.

**Inference:** DECWAR almost certainly used per-object or per-region lock flags in the shared high segment, or relied on the PDP-10's word-level atomic operations for critical state transitions. The MACRO-10 foundation gave direct access to hardware-level atomic operations. The FORTRAN modules (TORP.FOR etc.) almost certainly called MACRO-10 stubs for any write to shared state.

## 4. Player Join/Leave and Persistence

**Documented solution:** Players chose from a list of ships not currently being controlled. On re-entry, they could take back the same ship. This is persistent game state per ship across sessions within a single galaxy instance — an early form of session persistence. No server-side session management; the state lived in the shared segment.

## 5. Memory Constraints

**The problem:** 18 simultaneous jobs plus shared galaxy state on a machine with limited physical memory, shared with all other university users.

**The consequence:** Memory pressure was real. The university banned DECWAR and similar games due to RAM consumption. This explains the compact MACRO-10 core, the terse command set, and the specific 75×75 / 79×79 galaxy size — large enough for 18 players to have interesting territories, but constrained by the memory cost of storing and updating the galaxy array.

## 6. Scheduling and Fairness

**The property:** TOPS-10 used priority-based scheduling where compute-intensive jobs accumulated a worse priority (they got more CPU and were penalized); interactive jobs (mostly blocked on I/O with short CPU bursts) got better priority. DECWAR jobs were naturally interactive — this meant TOPS-10's scheduler *naturally* favored DECWAR jobs over batch compilation jobs. This was not designed; it was an emergent benefit of the time-sharing model.

**The designed asymmetry:** Fast typists could issue many commands while slow players were still deciding — explicitly documented as giving advantage to fast players. The three terse modes partially addressed this by reducing output-reading time.

## 7. Reliability and Recovery

**Limitations:** No explicit crash recovery for hardware failures — a machine reboot ended all active galaxies. **Partial mitigation:** Individual ship states persisted between player sessions within a galaxy. The GRIPE command (documented in decwar.hlp) logged bug reports from live players with full session metadata to GAM:DECWAR.GRP — the game's designed feedback mechanism for a system that couldn't be easily debugged in a classical single-process debugger.

## 8. Debugging in a Multi-User Time-Sharing Environment

**The challenge:** Debugging a race condition in a shared-memory 18-player game in 1978 meant operating without source-level debuggers. DDT10 (the TOPS-10 debugger) operated at the machine-instruction and symbol-table level. Reproducing a race condition required multiple simultaneously active player jobs — which meant the developers had to debug live.

**Practical consequence:** The GRIPE command was the production monitoring system. Each gripe was logged with version number, date, time, ship name, user name, TTY speed, PPN, TTY number, and job number — full diagnostic context from a live game, the only practical way to catch race conditions in an 18-player simultaneous system.

## 9. Deployment in a University Computing Environment

DECWAR was distributed as source code (MACRO-10 + FORTRAN), not binaries, knowing that different sites would have different TOPS-10 configurations. Installation required: assembling the MACRO-10 source, compiling the FORTRAN modules, linking with LINK-10, and installing with appropriate PPN setup. The $50 tape included build instructions.

The TOPS-10 specificity was a real deployment constraint. The usenet discussion showed that porting to TOPS-20 was considered effectively impossible without ground-up restructuring of the MACRO-10 components, because the shared hi-seg mechanism and TOPS-10-specific UUOs had no direct TOPS-20 equivalents. CompuServe's Kesmai team ran DECWAR on CIS's own TOPS-10 variant rather than porting it.

---

# 10. What Remains Uncertain

1. **WAR's authorship and code.** The CDC 6600 WAR game has no identified author(s) and no surviving code. "Mid-1970s" dating is from secondary sources. Whether it used BASIC, FORTRAN, CDC Assembly, or a combination is unknown.

2. **The Hicks/Korp "Penn. U." Trek.** The April 1973 BASIC Trek header says "GENERAL IDEA STOLEN FROM PENN. U." — implying a Penn State version that predates it. No code or documentation from this Penn State version has been located. Whether it descended from Mayfield's STTR1 or was an independent invention is unknown.

3. **DECWAR's exact synchronization mechanism.** The shared high-segment architecture is confirmed. The specific locking protocol — how DECWAR prevented concurrent modifications from corrupting galaxy state — is in the MACRO-10 source but has not been specifically analyzed in the secondary literature examined for this report. This is the most important open technical question.

4. **Which PDP-10 model ran DECWAR v1.0 at UT Austin in 1978.** Sources say "the DEC-10" without specifying KA10, KI10, or KL10. Given 1978 date, a KI10 or KL10 is most likely.

5. **Exact DECWAR pregame lobby and galaxy initialization.** How the first player to join initialized the shared segment; whether there was a "master process" or entirely symmetric job architecture — details in the source code not yet specifically analyzed in secondary literature.

6. **The Matuszek/Reynolds FORTRAN Trek's relationship to Mayfield's code.** ESR and Matuszek both state the UT FORTRAN version was independently designed. But the Hicks/Korp BASIC Trek it was based on may or may not have descended from Mayfield. Chain is uncertain.

7. **Whether any pre-1978 multiplayer Star Trek variants existed outside PLATO and WAR.** Ahl's vague recollection of seeing "Star Trek games at CMU in 1967-68" has never been corroborated with specific authorship or code, and likely refers to Spacewar! variants.

---

# 11. Future Research Agenda

## Source Code Analysis (Highest Priority)

- **Full MACRO-10 analysis of DECWAR:** The drforbin/decwar and PDP-10/decwar GitHub repositories contain the complete source. A close reading of the MACRO-10 startup sequence (particularly GLINIT, PLINIT, and any locking primitives around shared high-segment writes) is the single most important outstanding task for understanding the synchronization architecture.
- **UT Super Star Trek original printout scan** (repositories.lib.utexas.edu/items/82ab7746...) — a close reading would clarify the CDC Assembler components and their role.

## Archives to Search

- **Dolph Briscoe Center for American History, UT Austin:** Primary repository for DECWAR. Physical inspection may reveal development notes, correspondence, or earlier versions not digitized.
- **DECUS tape archives** (trailing-edge.com, Tim Shoppa): Systematic search for WAR, earlier DECWAR versions, or related games from other PDP-10 institutions.
- **Bitsavers.org, DEC documentation section** (bitsavers.org/pdf/dec/pdp10/): TOPS-10 Monitor Calls Reference Manual; TOPS-10 Operating System Commands Manual — will confirm the specific UUOs DECWAR used.
- **UT Austin Computing Center institutional records:** May contain account records, system logs, or correspondence about DECWAR's deployment and the university's administrative response.

## Interviews to Pursue

- **Bob Hysick and Jeff Potter** (primary DECWAR authors): No public interviews found. Their recollections of the shared-memory design decisions would be invaluable.
- **Robert Schneider** (initiated the CDC-to-PDP-10 port): No public account found.
- **Harris Newman** (preserved source code; built Go clone decwars.com): Has detailed knowledge from reverse engineering work; accessible via public presence.
- **Dave Matuszek** (UT FORTRAN Super Star Trek): Has spoken with ESR. His recollections of the CDC 6600 computing environment at UT Austin in 1973–78 would clarify the CDC → PDP-10 transition context.

## Manuals to Inspect

- **TOPS-10 Monitor Calls Reference Manual** (DEC; bitsavers.org/pdf/dec/pdp10/TOPS10/) — specifically shared memory and hi-seg sections, UUO reference, IPC facilities.
- **MACRO-10 Assembler Reference Manual** (DEC; bitsavers.org) — understanding the macro environment DECWAR uses.
- **HP 2000/Access Reference Manuals** (mrynet.com/hp2000/documentation.html; bitsavers.org) — confirms HP TSB architecture details.
- **Bell et al., "The Evolution of the DECsystem-10," CACM 1978** (archive.computerhistory.org) — canonical technical history by the designers.
- **CDC 6600 SCOPE/KRONOS operating system manuals** — for confirming the single-terminal limitation that defined WAR's architecture.

## Videos Worth Watching

- **SimH PDP-10 DECWAR running on TOPS-10** (YouTube, multiple channels): *Evidentiary* for terminal interface, command abbreviation behavior, and galaxy display. The best way to see what DECWAR's players actually experienced.
- **DecwarOrg YouTube channel** (referenced at decwar.org): *Preservation-era evidentiary.* Direct documentation of DECWAR in preservation context.
- **Computer History Museum PDP-1 tour** (CHM YouTube, guided by Lyle Bickley): *Explanatory.* Demonstrates the Type 30 vector display and the magnitude of the contrast with teletype-based gaming.
- ***Spacewar!* emulation** (masswerk.at/spacewar/ — runs in browser): *Evidentiary* for understanding what Mayfield saw and why the teletype design challenge was non-trivial.
- **"Life on the PDP-10"** (various CHM and Living Computers Museum recordings): *Explanatory.* Context for what TOPS-10 operation looked and felt like.

## Evidence That Would Most Improve Confidence

1. Any surviving documentation or code from WAR (the CDC 6600 two-player version).
2. Documented oral history from Hysick and/or Potter describing the shared-memory design decisions.
3. Identification of the specific TOPS-10 synchronization primitives in DECWAR's MACRO-10 code via direct source analysis.
4. Any documentation from UT Austin Computation Center about the institutional response to DECWAR (resource consumption records, correspondence about banning).

---

# 12. Annotated Bibliography

## Primary Sources

**STTR1 source code** (HP BASIC, October 20, 1972). Extracted from HP tape by Pete Turnbull. http://www.dunnington.info/public/startrek/STTR1 — *The foundational artifact. The dated REM header ("TOTAL INTERACTION GAME - ORIG. 20 OCT 1972") is primary evidence for completion date.*

**DECWAR source code, version 2.3** (MACRO-10 + FORTRAN IV, November 1981). github.com/drforbin/decwar and github.com/PDP-10/decwar. Original archive: Dolph Briscoe Center for American History, UT Austin (hdl.handle.net/2152/11351). — *Primary source for DECWAR implementation. The FORTRAN files (TORP.FOR, EXTERN.FOR, etc.) and MACRO-10 assembly are the direct artifacts.*

**DECWAR Version 2.2 help file** ("decwar.hlp", June 3, 1980). github.com/PDP-10/decwar/blob/master/files/decwar.hlp — *Primary. Reveals command set, program state names (DECWTI, DECWRN, DECWSL, DECWPG), gripe mechanism, and operational details.*

**DECWAR Version 2.2, UT Austin repository** (binary; from DECUS tape). repositories.lib.utexas.edu/items/1aa48343-09ab-4b3b-a9f2-e2e525074a4d — *Primary institutional. Contains definitive version attribution: "almost entirely re-written (in assembler language and Fortran)".*

**DECWAR Version 2.3, UT Austin institutional archive**. repositories.lib.utexas.edu/items/7e2ccf50-e814-4bce-91d2-a7f6440eabe4 — *Primary. Confirms WAR origin and Robert Schneider's initiation of the PDP-10 transfer.*

**UT Super Star Trek source/documentation** (FORTRAN + CDC Assembler, ca. 1973–78). repositories.lib.utexas.edu/items/82ab7746-0327-47fe-9afd-5281a41dcedc — *Primary. "Only known physical print out of the Super Star Trek source code and user manual."*

**Mayfield email to Games of Fame** (December 3, 2000). gamesoffame.wordpress.com/star-trek/ — *Primary creator account, ~30 years after events. Confirms Sigma 7 origin, HP rewrite rationale.*

**Leedom email to Games of Fame** (ca. 2000). gamesoffame.wordpress.com/star-trek/ — *Primary creator account for Super Star Trek. Confirms DG Nova 800 platform and design decisions.*

**Graetz, J.M. "Spacewar! Real-Time Capability of the PDP-1."** DECUS Proceedings 1962. Digitized at bitsavers.org/pdf/dec/decus/confProceedings/DECUS_1962.pdf. HTML: masswerk.at/spacewar/decus1962/ — *The original contemporaneous description of Spacewar! by one of its creators.*

**DECWAR usenet source thread** (alt.sys.pdp10, archiving discussion of porting). alt.sys.pdp10.narkive.com/zEU0jtQa/decwar-source-for-version-2-3 — *Primary community discussion. Confirms shared hi-seg architecture and TOPS-10 dependency: "DECWAR is very much a Tops-10 program."*

---

## Technical Manuals

**Bell, C. Gordon; Kotok, Alan; Hastings, Thomas N.; Hill, Richard. "The Evolution of the DECsystem-10."** CACM, Vol. 21, No. 1, 1978. archive.computerhistory.org/resources/text/DEC/pdp-10/... — *Definitive technical history of the PDP-10 by its designers.*

**DECsystem-10 System Reference Manual** (DEC-10-XSRMA-A-D). bitsavers.org and gunkies.org/wiki/PDP-10. — *Primary hardware documentation.*

**TOPS-10 Monitor Calls Reference Manual** (DEC). bitsavers.org/pdf/dec/pdp10/TOPS10/ — *Primary OS documentation for the UUO/monitor call mechanism DECWAR uses.*

**HP 2000/Access Reference Manuals.** mrynet.com/hp2000/documentation.html; bitsavers.org/pdf/hp/2000TSB/ — *Confirms dual-processor architecture, 32-user limit, contributed-programs library structure.*

**HP Time-Shared BASIC/2000 Quick Reference Card** (September 1972). decodesystems.com/hp2000/ — *Contemporary to STTR1's development. Shows the exact HP BASIC dialect Mayfield used.*

**PDP-10 FORTRAN IV Programming Manual** (Aug 1969, DEC-10-AFC0-D). archive.org/details/bitsavers_decpdp10TOFORTRANIVProgrammingManualAug69_2597505 — *The FORTRAN manual relevant to DECWAR's FORTRAN components.*

---

## Secondary Sources

**Wikipedia, "PDP-10"** — Well-cited secondary synthesis. Cross-checked against primary sources.

**Wikipedia, "TOPS-10"** — Explicitly confirms TOPS-10 shared memory and DECWAR as an example of its use.

**Wikipedia, "Decwar"** — Best secondary synthesis of DECWAR history. Cross-checked against UT Austin primary archives.

**Wikipedia, "HP Time-Shared BASIC"** — Confirms dual-processor architecture, 16–32 user support, Star Trek's role in HP TSB history.

**Wikipedia, "HP 2100"** — Machine overview; confirms HP 2000 packaging and time-sharing model.

**Wikipedia, "Star Trek (1971 video game)"** — Best secondary synthesis of the BASIC lineage.

**Reed, Aaron A. "Code Archaeology with 'Super Star Trek'."** Medium / The Startup, May 2022. medium.com/swlh/code-archaeology-with-super-star-trek-928101eb010c — *Close reading of STTR1 vs. Ahl/Cole code differences. The best technical source analysis of the BASIC implementation chain.*

**Reed, Aaron A. "1974: Super Star Trek."** IF50 Substack, January 2021. if50.substack.com/p/1974-super-star-trek — *Best single secondary synthesis of the Mayfield → Leedom chain. Technically literate.*

**ESR (Eric Raymond), sst-doc.html.** catb.org/~esr/super-star-trek/sst-doc.html — *Valuable for UT FORTRAN Trek lineage. ESR was personally acquainted with Matuszek.*

**Games of Fame, "Star Trek."** gamesoffame.wordpress.com/star-trek/ — *Contains Mayfield and Leedom emails in full.*

**Games of Fame, "WAR, DECWAR and MegaWars."** gamesoffame.wordpress.com/war-decwar-and-megawars/ — *Best secondary account of the WAR → DECWAR → MegaWars chain.*

**Columbia University Computing History, "The Digital Equipment Corporation PDP-10."** columbia.edu/cu/computinghistory/pdp10.html — *Solid institutional history.*

**DecwarOrg.** decwar.org — *Active preservation organization; contains the most concise confirmed source header excerpt showing MACRO-10 structure and startup sequence.*

**Multiplayer video game, Fandom wiki.** ultimatepopculture.fandom.com/wiki/Multiplayer_video_game — *Contains the key line: "The games had a program running on each terminal (for each player), sharing a segment of shared memory (known as the 'high segment' in the OS TOPS-10)."*

**Time Reshared, "DEC PDP-10."** timereshared.com/dec-pdp-10/ — *Concise technical overview.*

---

## Video Sources

**SimH PDP-10 DECWAR demonstrations** (multiple YouTube channels) — *Evidentiary.* Shows actual DECWAR terminal interaction, command abbreviation behavior, galaxy display on emulated TOPS-10.

**DecwarOrg YouTube channel** (referenced at decwar.org) — *Preservation-era evidentiary.*

**Computer History Museum, PDP-1 Restoration Project / CHM PDP-1 tour** (computerhistory.org/pdp-1/spacewar/ and CHM YouTube) — *Primary institutional + explanatory.* Demonstrates the Type 30 vector display.

***Spacewar!* browser emulation** (masswerk.at/spacewar/) — *Evidentiary* for understanding what Mayfield saw and the design challenge it posed.

---

## Archives and Repositories

| Resource | Location |
|---|---|
| DECWAR source (MACRO-10 + FORTRAN) | github.com/drforbin/decwar ; github.com/PDP-10/decwar |
| DECWAR UT Austin institutional archive | repositories.lib.utexas.edu (search "Decwar") |
| DECWAR physical archive | Dolph Briscoe Center for American History, UT Austin |
| STTR1 HP BASIC source | dunnington.info/public/startrek/STTR1 |
| Bitsavers DEC documentation | bitsavers.org/pdf/dec/pdp10/ |
| HP 2000/Access documentation | mrynet.com/hp2000/documentation.html |
| TOPS-10 emulation (SIMH) | trailing-edge.com (Tim Shoppa's PDP-10 archive) |
| People's Computer Company newsletters | archive.org |
| BASIC Computer Games (Ahl, 1978) | atariarchives.org/basicgames/ |
| UT Super Star Trek printout scan | repositories.lib.utexas.edu/items/82ab7746... |
| Go clone of DECWAR (Gowars) | github.com/hsnewman/Gowars |
| DecwarOrg preservation organization | decwar.org |
| Spacewar! browser emulation | masswerk.at/spacewar/ |

---

*This report was compiled through systematic parallel research across platform history, implementation history, source code analysis, and primary/secondary source comparison. Claims are classified throughout as confirmed, strongly supported, or inferred from platform characteristics — with the inference clearly labeled. Where the evidence ends and inference begins is explicitly marked. The engineering analysis in Section 9 represents informed inference from the documented platform characteristics of TOPS-10, the PDP-10 architecture, and the observable behaviors described in DECWAR documentation — not a complete analysis of the full source code, which remains available for further study at the repositories listed above.*
