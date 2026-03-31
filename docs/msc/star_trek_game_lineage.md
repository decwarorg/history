# THE LINEAGE OF STAR TREK COMPUTER GAMES
### A Source-Driven Historical Investigation

---

# 1. Executive Summary

The story of Star Trek computer games is not a single clean line of descent. It is a story of convergent conditions — technological, cultural, and social — that produced a small explosion of independently developed but relationally connected games across roughly two decades, from 1971 to the early 1990s. To understand this history properly, one must resist the common narrative that flattens it into the sequence "Mayfield invented it, Ahl published it, Leedom improved it, and the personal computer spread it." That account is not wrong, but it omits crucial branches, overstates single authorship, and misses the sociological richness of what actually happened.

**The origin:** The earliest confirmed Star Trek computer game in the tradition that matters most — text-based, turn-based, single-player, quadrant-and-sector strategy — was created by Mike Mayfield in 1971, during his senior year of high school, using illicitly borrowed access to an SDS Sigma 7 mainframe at the University of California, Irvine. He was eighteen years old. He had seen Spacewar!, a 1962 graphical two-player combat game created at MIT for the DEC PDP-1, running on a vector-display terminal at the UCI lab, and wanted to make something like it for the only interface he had access to: a Teletype Model 33 ASR, a printer terminal incapable of graphics. He solved the problem elegantly: instead of simulating the physics of two ships in real-time graphical space, he abstracted the entire Star Trek universe into an 8×8 grid of quadrants, each containing an 8×8 sector grid, navigated by command and explored by scan. The result was completed in its first form in the summer of 1971 and rewritten from scratch for HP Time-Shared BASIC on an HP 2000C minicomputer, with the final version dated October 20, 1972, in the program's own REM header.

**David Ahl's role — disseminator, not originator:** David Ahl was not the creator of this game. He was its most important early distributor and the architect of its mass spread. A DEC employee in the education division, Ahl ran the EDU newsletter, which collected user-submitted games. In the summer of 1973, he and DEC colleague Mary Cole ported Mayfield's HP BASIC version to DEC BASIC-PLUS, made modest additions, and published it in the newsletter under the name "SPACWR" (an acknowledged misnaming). That same year he collected many such games, including the Trek program, into *101 BASIC Computer Games*, published by DEC in July 1973. This 10,000-copy publication was already highly influential. But the game's world-historic scale came later: in 1978, Ahl published the second edition as *BASIC Computer Games* — now in Microsoft BASIC, now containing Bob Leedom's much-enhanced Super Star Trek rather than the original Mayfield version — and it became the first computer book to sell more than one million copies. Ahl was the publishing infrastructure through which a high school student's game reached the world.

**Bob Leedom and Super Star Trek:** The version most people actually played was not Mayfield's original but Bob Leedom's 1974 expansion, Super Star Trek. Leedom, a professional programmer at Westinghouse Electric Corporation working on a Data General Nova 800 minicomputer, encountered the game through Ahl's *101 BASIC Computer Games* book, ported it to Data General BASIC, and, with input from engineering colleagues, expanded and polished it substantially. He replaced numeric commands with three-letter mnemonics (NAV, PHA, LRS, COM), added movement to Klingon ships, introduced quadrant names, added crew voice messages from canonical characters, and expanded the library computer. He wrote a letter describing his version to the People's Computer Company newsletter in September 1974. Ahl, who had by then left DEC to found Creative Computing magazine, saw the letter, contacted Leedom, and published Super Star Trek in Creative Computing (May/June 1975). Its inclusion in *BASIC Computer Games* (1978) gave it mass distribution just as the Apple II, TRS-80, and Commodore PET were entering the market. Leedom's version became the de facto standard.

**The broader lineage is a forest, not a tree.** Running in parallel with the Mayfield-Ahl-Leedom single-player BASIC tradition was a completely separate multiplayer tradition rooted in two places. On the PLATO network at the University of Illinois, Empire (1973, John Daleske) pioneered real-time, multi-player space combat with Star Trek-themed ships, inspiring the separate trek82/trek83/Xtrek/Netrek lineage that has no direct code connection to Mayfield's game. Separately, a two-player game called WAR (authors unknown, CDC 6600) evolved into DECWAR (1978, University of Texas at Austin, PDP-10), which was adapted without its Star Trek-specific IP into MegaWars for CompuServe (1983) and Stellar Warrior for GEnie (1986). These are not children of Super Star Trek; they are parallel cousins sharing a common cultural grandparent — the Star Trek franchise itself.

**Why Star Trek?** Star Trek was in syndication across 125+ American TV stations by 1972, drawing a larger audience after cancellation than during its original run. It had a passionate and organized fandom producing over 100 fanzines by the time of the first major convention in January 1972. More importantly for game design, its structure was uniquely gameable: a hierarchical command setting, episodic missions, a crew of specialized roles, alien adversaries with defined attributes, resource systems (shields, energy, torpedoes), and exploration of an explicitly mapped universe. The captain role was a natural player-character. The quadrant-and-sector map — explicitly referenced in the show — gave Mayfield his grid structure directly. No prior IP had offered this combination of cultural saturation and structural correspondence to turn-based tactical game systems.

**The enduring appeal** is not purely nostalgic. These games exemplify a principle that has been re-proven by roguelikes, text adventures, and minimalist indie games ever since: procedural drama generated from systematic abstractions is cognitively engaging in ways that visually rich games are not always able to replicate. The player of Super Star Trek is not watching a simulation; they are commanding one, using imagination to populate the sparse ASCII grid with a vivid mental model of space, threat, and urgency. The time limit is a genuine pressure system. Damaged sensors create real information deprivation. Running out of energy with one Klingon left is a genuine crisis. These are emergent dramas, not scripted ones — and they hold up.

---

# 2. Key Findings

- **Mike Mayfield created the foundational Star Trek text game in 1971** (Sigma 7) and completed the canonical HP BASIC version on October 20, 1972. He was a high school student at the time.
- **David Ahl was not the game's creator.** He was its most important early publisher and the agent of its mass dissemination, through *101 BASIC Computer Games* (1973) and *BASIC Computer Games* (1978). His contribution was infrastructural and editorial, not creative.
- **Mary Cole was Ahl's co-porter** at DEC in summer 1973, adapting Mayfield's code to BASIC-PLUS. Her contribution is acknowledged by Ahl but insufficiently documented in secondary literature.
- **Bob Leedom's Super Star Trek (1974)** is the version most people actually encountered. It is a significant creative expansion of Mayfield's work, not merely a port. It added player-facing polish, mechanical depth, and thematic richness.
- **BASIC Computer Games (1978)** was the first million-selling computer book and the primary mechanism by which Super Star Trek became ubiquitous across early home computing platforms.
- **The single-player BASIC strategy tradition** (Mayfield → Ahl/Cole → Leedom → BASIC Computer Games → microcomputer ports) is a distinct lineage from the multiplayer combat tradition.
- **The multiplayer tradition has two main branches:** (a) PLATO Empire (1973) → trek82/trek83 → Xtrek (1986) → Netrek (1988), and (b) WAR → DECWAR (1978) → MegaWars (1983) → Stellar Warrior (1986).
- **TREK73** (William K. Char, Perry Lee, Dan Gee; begun January 1973, first external publication January 1974 in PCC) was a parallel tactical combat variant on the same HP 2000 platform as Mayfield's game, not a descendant of it.
- **Spacewar! (1962)** was Mayfield's explicit stated inspiration, but was a graphical vector game; his key creative decision was how to redesign a space game for teletype output. It is a causal influence but not a direct ancestor in code or system.
- **Ahl's own claim** to have played Star Trek text games on campuses in 1967–68 remains unverified and is likely a confusion with Spacewar! variants.
- **The game's structural elegance under constraint** — not just nostalgia — explains its enduring appeal and continued porting, rewriting, and study today.

---

# 3. Genealogy Map

```
DIRECT LINEAGE (code-to-code descent):
═══════════════════════════════════════

[Spacewar!, 1962, MIT/DEC PDP-1]
  │ [INSPIRATION/INFLUENCE, not code descent]
  ▼
[Mike Mayfield Star Trek, SDS Sigma 7, summer 1971]
  │ [Rewrite from scratch, not port]
  ▼
[STTR1 / HP BASIC version, HP 2000C, Oct 20 1972]
  │ [entered HP public domain library Feb 1973]
  ├──→ [People's Computer Company newsletter pub, 1973]
  │
  ▼
[Ahl/Cole port to BASIC-PLUS, DEC, summer 1973]
  │ [published as "SPACWR" in DEC EDU newsletter]
  ▼
[101 BASIC Computer Games, DEC, July 1973]
  │ [10,000+ copies; Leedom reads this]
  ▼
[Bob Leedom Super Star Trek, Data General Nova 800, 1974]
  │ [letter to PCC, Sept 1974; Ahl sees it]
  ├──→ [Creative Computing magazine, May/June 1975]
  ▼
[BASIC Computer Games, 1978, Microsoft BASIC edition]
  │ [~1,000,000+ copies; first million-selling computer book]
  ├──→ Apple Trek (Apple II+, 1979, W. Sander / Apple Inc.)
  ├──→ Space Trek (TRS-80, Tandy)
  ├──→ Galaxy (BBC Micro, Acornsoft)
  ├──→ Stellar Track (Atari 2600, 1980)
  ├──→ Video Trek 88 / BASICA (IBM PC, 1982)
  ├──→ DOS Super Star Trek (Matuszek/Reynolds, 1982; Smith/Almy revisions, 2014)
  ├──→ EGA Trek (IBM PC, graphical screens)
  └──→ [hundreds of other BASIC platform ports, 1978–1990]


PARALLEL BRANCH A — TACTICAL COMBAT (HP 2000C)
══════════════════════════════════════════════
[TREK73 / $SPACE, William K. Char, Perry Lee, Dan Gee]
  [Wilson High School HP 2000C, began Jan 1973, published Jan 1974 PCC]
  │
  ├──→ [Roderick Perkins port, Lawrence Hall of Science, UC Berkeley, 1974]
  ├──→ [Dave Pare/Chris Williams C port, UC Berkeley, 1984]
  ├──→ [Jeff Okamoto/Peter Yee consolidated version, April 1985]
  ├──→ [Howard Chu Turbo Pascal / DOS port, U Michigan, 1985]
  ├──→ Begin: A Tactical Starship Simulation (Nelson/Higgins, MS-DOS, 1984)
  └──→ [Fred Fish Disk 10 Amiga version]


PARALLEL BRANCH B — MULTIPLAYER REAL-TIME (PLATO)
══════════════════════════════════════════════════
[Empire I, PLATO, John Daleske / Silas Warner, Spring 1973, UIUC]
  │ [Star Trek-themed ships; first 8-player multi-terminal game]
  ├──→ Empire II–IV (PLATO, larger scale, real-time combat)
  │
  ├──→ [trek82, David Davis, UC Berkeley UNIX, 1982]
  │     └──→ [trek83, Guthrie/Davis/Poskanzer/Leres, UC Berkeley]
  │           └──→ [Xtrek, Chris Guthrie, X Window System, 1986]
  │                 └──→ [Netrek, Silvey/Smith/Chang, 1988]
  │                       └──→ [Internet Netrek League, 1992; still played]
  │
  └──→ [Conquest, Jef Poskanzer, VAX/VMS, 1982]


PARALLEL BRANCH C — MULTIPLAYER REAL-TIME (CDC / DEC)
══════════════════════════════════════════════════════
[WAR, unknown authors, CDC 6600, ~pre-1978]
  │ [2-player version of Star Trek mechanics]
  ▼
[DECWAR, Robert Schneider et al., UT Austin PDP-10, 1978]
  │ [1–18 players; shared memory architecture; Star Trek IP intact]
  │
  ├──→ [MegaWars, Kesmai/CompuServe, 1983–1998]
  │     [Star Trek IP stripped; Bill Louden purchased DECWAR for $50]
  │     └──→ [MegaWars III, Kesmai/CompuServe, 1984–1999]
  │           [massively multiplayer 4X; up to 100 players]
  │
  └──→ [Stellar Warrior, Kesmai/GEnie, 1986–1999]
        [MegaWars reskinned for GEnie; IP further genericized]
        └──→ [Stellar Emperor, MegaWars III equivalent on GEnie]

[MTrek / Multi-Trek, UC Santa Cruz, 1986, C/PDP; 3D persistent world]


ADJACENT INFLUENCES (not direct code descent):
══════════════════════════════════════════════
- Spacewar! → influenced Mayfield's goal, not his code
- Star Fleet Battles (tabletop, 1979) → influenced some Trek73 later versions
- PLATO Empire → influenced trek82 via David Davis's memory; not code-related to DECWAR
- Star Raiders (Atari, 1979) → independently inspired; cited as influencing Elite and Wing Commander
- MegaWars III (via Kesmai's "S" prototype, 1979) → partially independent from DECWAR lineage


DISPUTED / UNCERTAIN CONNECTIONS:
═══════════════════════════════
? Pre-Mayfield Star Trek text games (Ahl's recollection, 1967–68) — unconfirmed, likely Spacewar! variants
? Exact relationship between WAR and DECWAR in terms of code — original WAR authors unknown
? Whether Char knew of STTR1 before developing TREK73
? Whether any Homebrew Computer Club members directly used Mayfield's code before HP library release
```

---

# 4. Annotated Chronology

**1962 — Spacewar!**
Steve Russell, Martin Graetz, Wayne Wiitanen, et al. DEC PDP-1, MIT. Assembly language. The first widely distributed graphical computer game; requires vector CRT display. Spreads to every PDP-1 installation. Directly inspires Mayfield's ambition nine years later.
*Sources: Computer History Museum, Spacewar! documentation; Wikipedia, "Spacewar!"*

**1966–1969 — Star Trek: The Original Series**
NBC television, 79 episodes. Establishes universe, characters, and structural elements (starship command hierarchy, exploration mission, alien adversaries, quadrant navigation, resource systems) that will prove directly gameifiable.
*Sources: Wikipedia, "Star Trek"*

**1969 (fall) — Star Trek enters syndication**
Reruns begin; audience grows. By 1972, 125+ domestic markets. The fan phenomenon intensifies during the show's off-air years, not during its run.
*Sources: Wikipedia, "Star Trek"; Wikipedia, "Trekkie"*

**1971 (summer) — Mike Mayfield's Star Trek, SDS Sigma 7, UC Irvine**
Mayfield, then a high-school senior, programs a text-based Star Trek game on borrowed (unauthorized) account access. Uses punched paper tape for persistence. Inspiration explicitly cited as Spacewar!, seen on the PDP-10 at the UCI lab.
*Sources: Mayfield's email to Games of Fame, December 3, 2000; Wikipedia, "Star Trek (1971 video game)"*

**1972 (January) — First International Star Trek Convention, NYC**
Expected 500 attendees; 3,000+ come. Demonstrates scale of fandom and its organizing capacity.
*Sources: Wikipedia, "Trekkie"*

**1972 (October 20) — STTR1 completed — HP BASIC version**
Mayfield rewrites game from scratch for HP 2000C. The REM header in the source code reads "TOTAL INTERACTION GAME - ORIG. 20 OCT 1972." Attribution to "Centerline Engineering" (a fictional company Mayfield coined).
*Sources: STTR1 source code, extracted by Pete Turnbull from HP tape image; frankrefischer/STTR GitHub repository*

**1973 (February) — STTR1 added to HP Contributed Program Library**
HP places game in public domain software catalog, distributed on tape. This is the first broad institutional distribution. Later also published in People's Computer Company newsletter and in the 1975 PCC book *What to Do After You Hit Return*.
*Sources: Wikipedia, "Star Trek (1971 video game)"*

**1973 (January–October) — TREK73 created**
William K. Char begins $SPACE in January 1973 at Wilson High School, San Francisco, on HP 2000C; completes Trek73 in October with Perry Lee and Dan Gee. Published in People's Computer Company newsletter, January 1974. A distinct, parallel tactical combat game, not descended from Mayfield's code.
*Sources: Wargaming Scribe; Codex Gamicus; Trek73 Codex entry*

**1973 (spring) — Empire I, PLATO system**
John Daleske (Iowa State University, CERL) creates the first multi-terminal multiplayer space game on PLATO, with Silas Warner providing disk space. Inspired by but not derived from Mayfield's game. Uses Star Trek-themed ship designs. Eight simultaneous players. This is the earliest confirmed multiplayer networked space game.
*Sources: Wikipedia, "Empire (1973 video game)"*

**1973 (summer) — Ahl and Cole port to BASIC-PLUS**
David Ahl (DEC education division) and Mary Cole adapt STTR1 to DEC BASIC-PLUS dialect for RSTS-11 compiler. Published in DEC's EDU newsletter as "SPACWR." Ahl later acknowledges this was an incorrect name.
*Sources: Ahl's notes in BASIC Computer Games (1978 edition); Games of Fame blog; Wikipedia*

**1973 (July) — 101 BASIC Computer Games published**
Published by DEC. Contains "SPACWR" (the Ahl/Cole Trek port). First printing sells out; two further print runs (April 1974, March 1975); total ~10,000 copies.
*Sources: Wikipedia, "BASIC Computer Games"; Smithsonian NMAH collection nmah_1465425; Museum of Play blog on Ahl*

**1974 (early) — Bob Leedom encounters SPACWR in 101 BASIC Computer Games**
Working at Westinghouse on Data General Nova 800. Ports the game, then expands it throughout 1974 with suggestions from engineering colleagues. Key additions: 3-letter command mnemonics, moving Klingons, quadrant names, crew voice messages, expanded library computer.
*Sources: Leedom's email to Games of Fame, gamesoffame.wordpress.com*

**1974 (October) — Creative Computing magazine founded**
David Ahl, after leaving DEC. Launched as educational/hobby computing magazine, publishes BASIC source code, becomes primary distribution channel for hobby games through early 1980s.
*Sources: Wikipedia, "Creative Computing"; Museum of Play blog*

**1974 (September) — Bob Leedom writes to People's Computer Company newsletter**
Describes his enhanced Star Trek game. This letter is seen by Ahl.
*Sources: Games of Fame blog; IF50 substack; Wargaming Scribe*

**1975 (May/June) — Super Star Trek published in Creative Computing**
Ahl publishes Leedom's version, ported to Microsoft BASIC, under the name "Super Star Trek." First major commercial-adjacent publication of the superior version.
*Sources: Creative Computing magazine, May/June 1975; Wikipedia; Wargaming Scribe*

**1976 — The Best of Creative Computing anthology**
Includes Super Star Trek. Further distribution.
*Sources: Wikipedia*

**1978 — BASIC Computer Games published**
Microsoft BASIC edition. Contains Super Star Trek as longest program (c. 500 lines). Sells 1,000,000+ copies — the first million-selling computer book. Released just as Apple II, TRS-80, and Commodore PET enter market.
*Sources: Wikipedia, "BASIC Computer Games"; Creative Computing Wikipedia; Museum of Play*

**1978 (August) — DECWAR written**
University of Texas at Austin, Robert Schneider and others, for PDP-10. Derived from WAR (2-player CDC 6600 version, earlier, authors unknown). Supports 1–18 simultaneous players via shared memory architecture.
*Sources: Wikipedia, "Decwar"; Massively Overpowered retrospective*

**1979 — Apple Trek**
Apple II+, Wendell Sander / Apple Inc. Commercial release derived from Ahl's BASIC lineage. Renamed to avoid trademark issues.
*Sources: Wikipedia; The Register*

**1980 — Stellar Track (Atari 2600)**
Commercial port of Super Star Trek lineage for home console.
*Sources: Wikipedia; Atari Archive YouTube channel*

**1982 — trek82, UC Berkeley**
David Davis, UNIX; based on his memory of PLATO Empire. First step in the Unix/X-window multiplayer lineage.
*Sources: Netrek Nexus history; Wikipedia, "Netrek"*

**1983 — MegaWars launched on CompuServe**
Kesmai adapt DECWAR for Bill Louden at CompuServe, stripping Star Trek IP. Real-time multiplayer space combat, available via modem. Runs 1983–1998.
*Sources: Wikipedia, "Decwar" and "MegaWars III"; Games of Fame blog; Massively Overpowered*

**1984 — MegaWars III launched on CompuServe**
Massively multiplayer (up to 100 players), 1000-system galaxy, month-long campaigns. Precursor to MMO 4X design.
*Sources: Wikipedia, "MegaWars III"*

**1986 — Xtrek released, UC Berkeley XCF**
Chris Guthrie et al. Star Trek-themed real-time multiplayer game using X Window System.
*Sources: Wikipedia, "Netrek"; Netrek Nexus*

**1986 — Stellar Warrior launched on GEnie**
MegaWars reskinned for GEnie service by Kesmai; runs until GEnie shutdown 1999.
*Sources: Wikipedia, "MegaWars III"; Games of Fame blog*

**1988 — Netrek**
Scott Silvey, Kevin Smith, Terence Chang. Client-server architecture; own protocol independent of X. Posted to Usenet 1989. Probably first Internet game using both TCP and UDP. First Internet team game.
*Sources: Wikipedia, "Netrek"; Netrek Nexus history*

**1992 — International Netrek League founded**
Teams compete across universities. Inter-scholastic play begins between UC Berkeley and Carnegie Mellon.
*Sources: Netrek Nexus history*

---

# 5. Origins Analysis

## The Mayfield Question

Mike Mayfield's authorship of the foundational game is well established by multiple independent sources: his own first-person account (emailed to Games of Fame, December 3, 2000), David Ahl's attribution in his book prefaces, Bob Leedom's written account, the dated source code header in the surviving STTR1 tape image, and the consistent secondary literature. The date of the Sigma 7 version is 1971 (summer, Mayfield's senior year of high school). The date of the HP BASIC version is October 20, 1972, per the source code. These are, in all essential respects, confirmed facts.

One point of minor uncertainty: Mayfield's recollection of using an HP-35 calculator as his initial link to HP staff has been questioned by knowledgeable observers, since the HP-35 was not programmable (that was the HP-65, released 1974). This is a minor detail likely involving memory conflation; it does not affect the core history.

The game is not the first "Star Trek" branded item in the universe — there were board games by the late 1960s — but it is, by all available evidence, the first text-based, turn-based, computer Star Trek strategy game of the quadrant-hunting type that defines the tradition.

## The Ahl Question

Ahl's remark that he "recalled playing Star Trek games at Carnegie Mellon in 1967 or 1968, and a very different one at Berkeley" is intriguing but weak evidence. He makes this claim in a preface note added years after the events. He does not identify the specific games, their authors, or their gameplay in detail. Multiple commentators have suggested he was likely seeing Spacewar! variants, not true Star Trek text games. **This claim should be treated as plausible but unverified, and should not be used to establish a pre-Mayfield Star Trek text game tradition.** No corroborating source exists; no code or documentation from any such game has surfaced.

Ahl's actual contribution was threefold: (1) porting and publishing Mayfield's game through DEC channels in 1973, with Mary Cole; (2) founding Creative Computing magazine (1974); (3) editing and publishing *BASIC Computer Games* (1978), which put Super Star Trek in front of a million readers just as home computers arrived. He was the most consequential distributor in the history of the game, but not its creator or its most important enhancer.

## Mary Cole's Role

Mary Cole's role is acknowledged by Ahl ("Mary Cole at DEC contributed enormously to this task too") but is not detailed in any primary source. She was a DEC employee who co-worked the summer 1973 BASIC-PLUS port. The specific nature of her contribution — whether primarily technical, editorial, or both — is not documented beyond Ahl's brief acknowledgment. **Her contribution is real but insufficiently recorded.** This is a genuine archival gap.

## Bob Leedom's Role

Leedom's contribution is the most underappreciated by popular accounts. His changes were not trivial polishing: moving Klingons fundamentally altered the tactical situation; named quadrants added narrative texture; three-letter command mnemonics added thematic authenticity; crew voice messages created genuine emotional immersion. He worked on this throughout 1974 as a personal project, without any expectation of publication, sharing improvements with engineering colleagues. His willingness to write a letter to PCC, and Ahl's ability to recognize its quality, completed the chain.

## How the Early Versions Relate

The relationship is **inspiration → port → expansion**, not a single continuous development. Mayfield's Sigma 7 version was not ported to HP BASIC; it was rewritten from scratch. The HP version was ported (with modifications) by Ahl and Cole to DEC BASIC-PLUS. Leedom's version began as a port of the Ahl/Cole version to Data General BASIC, then became a substantial expansion. Ahl then ported Leedom's version to Microsoft BASIC for *BASIC Computer Games*. Each step involved human creative decisions, not mechanical translation. The code at each stage is related but not identical.

---

# 6. Cultural and Media Context

## What Star Trek Was

Star Trek: The Original Series (1966–69) was a network science fiction television series created by Gene Roddenberry for NBC. It ran for 79 episodes across three seasons before cancellation. During its original run it was a modest success: culturally literate, progressively cast, thematically ambitious, but not a ratings blockbuster.

What transformed it into a phenomenon was syndication. When Paramount licensed the reruns in 1969, the show began appearing on local TV stations across the country and world. By 1974 it was airing on 140+ domestic stations and 54 international markets. The fandom was strikingly organized: over 100 fanzines by January 1972, 250+ Star Trek clubs by 1976. The first major New York convention in January 1972 drew 3,000 people when 500 were expected; by 1974 the New York convention drew 15,000. Fan campaigns demonstrated real political leverage: letter-writing kept the show on for a third season in 1968–69, and a later campaign caused NASA to name its first Space Shuttle orbiter *Enterprise* in 1976.

## Why It Translated So Well Into Games

Star Trek's structure anticipated game design principles in ways that seem almost prescient in retrospect:

1. **Clear player role:** The player is the captain. Command authority is total and unambiguous.
2. **Explicit spatial system:** The Galaxy is divided into quadrants; quadrants into sectors. The show literally gave game designers a grid.
3. **Resource management:** Fuel, weapons (phaser power, torpedo supply), shields, and crew capacity are finite and manageable — natural game systems.
4. **Defined adversaries with attributes:** Klingons, Romulans, and starbases each had consistent behavioral profiles, mapping directly onto game AI categories.
5. **Mission framing:** Each episode had a setup, complications, and resolution. The game replicated this exactly.
6. **Social legitimacy:** Star Trek fandom gave the game cultural credibility that a generic space game could not have.

The cultural conditions of 1971–1978 also matter. The Apollo program had given the culture an appetite for space as genuine future possibility. University computing labs were sites of exploration and experimentation. BASIC was readable and modifiable by amateurs. The hacker ethic — that software should be shared, modified, and improved — was not yet in tension with commerce.

---

# 7. Design Character of Early Star Trek Games

## The Interface and Its Consequences

The Teletype Model 33 ASR printed at 10 characters per second. It had no cursor, no screen refresh, no backspace over previous output — only a scrolling paper roll. Programming for this terminal meant accepting that every output was permanent and sequential; the program could only add more text, never erase or redraw.

Mayfield's solution was elegant and foundational. Instead of attempting real-time display, he created a turn-based system with two map outputs: a long-range scan showing the 8×8 quadrant grid with Klingon, starbase, and star counts; and a short-range scan of the 8×8 sector grid, using ASCII characters (+K+ for Klingon, <\*> for Enterprise, >\!< for starbase, \* for star). Between turns, the player typed a command and received a paragraph of output. The pacing was naturally thoughtful — there was time between turns to consider options.

## The Core Game Systems

The following systems persist through all major versions:

- **8×8 quadrant grid, 8×8 sector grid** — the nested spatial system
- **Energy as primary resource** — all actions (movement, weapons, shields) consume energy
- **Photon torpedoes as secondary resource** — limited supply, replenished at starbases
- **Starbases as resupply and repair points** — creates territorial structure
- **Time limit (stardates)** — creates urgency, prevents grinding
- **Damage system** — random failures create information deprivation
- **Long-range scan** — information management; you can see into quadrants but must choose where to go
- **Phasers (distance-degraded) and torpedoes (fixed-path)** — two weapon types with distinct tactical profiles
- **Klingon attack tied to player turn** — enemy action is reactive, not independent

Leedom's key additions to Super Star Trek:

- **Moving Klingons** — enemy ships reposition after being fired upon; the most important tactical change
- **Three-letter command mnemonics** (NAV, PHA, TOR, SHE, DAM, COM, LRS, SRS, STA)
- **Named quadrants** (RIGEL IV, POLLUX II, etc.) — narrative immersion
- **Crew voice messages** (Spock, Scotty, Uhura, etc.) — thematic authenticity
- **Expanded library computer** (navigation assistance, star chart display)

## The Phenomenology of Play

Playing Super Star Trek circa 1978 meant sitting with a physical book open to a printout (or a screen showing typed-in code), entering commands at a prompt, and receiving several lines of output describing the situation. Combat was narrated rather than animated: "KLINGON AT SECTOR 7,3 ATTACKS — 200 UNITS ABSORBED BY SHIELDS." A damaged warp drive meant you couldn't navigate freely. Depleted shields meant each enemy attack was catastrophic.

The game created what game designers now call *emergent narrative* — stories arising from system interactions rather than authored scripts. No two games were identical (Mayfield built randomized starting conditions). The player constructed a mental model from sparse text, filling in visual and dramatic detail from imagination and knowledge of the show. The Enterprise felt like the Enterprise because the player already knew what the Enterprise was.

This was not a limitation being overcome; it was the game's primary mechanism. The sparseness of the interface forced active cognitive engagement. Players did not observe a story; they experienced themselves as commanding a ship.

---

# 8. Descendants and Related Systems

## TREK73 (1973, William K. Char, Perry Lee, Dan Gee)

TREK73 began in January 1973 when Char (then at Wilson High School, San Francisco) started programming $SPACE on a time-shared HP 2000C. The finished game was completed in October 1973 and published in PCC in January 1974. It is a parallel tactical combat game — not a descendant of Mayfield's code — with significantly greater complexity: 27 commands in the original version, wider enemy variety (Romulans, Gorns, and others from show canon), and more detailed crew interactions. Steve Dompier of the Homebrew Computer Club was sufficiently addicted to purchase a home teletype to play it.

TREK73 was more complex but less portable than Super Star Trek. It inspired later ports (C translation 1984; DOS version 1985; Amiga port) and the Begin family of tactical simulations, but never achieved the mass reach of the Leedom/Ahl lineage. Today it is largely forgotten outside retrogaming historiography.

## Empire (PLATO, 1973)

Empire on the PLATO system (spring 1973, John Daleske, Silas Warner) was arguably the most significant parallel development in the history of multiplayer gaming. It was the first game to support more than two simultaneous network-connected players. Between 1978 and 1985, PLATO users logged approximately 300,000 hours playing Empire. It directly influenced trek82 (David Davis's recreation at UC Berkeley) and through that chain the entire Netrek lineage. Empire had no code relationship to Mayfield's game; it was independently inspired by the same television franchise.

## WAR and DECWAR (CDC 6600 / UT Austin PDP-10, ~pre-1978 / 1978)

WAR was a two-player variant of Star Trek mechanics, created for the CDC 6600 by unknown authors. DECWAR (1978, Robert Schneider et al., University of Texas at Austin, PDP-10) expanded it to support 1–18 simultaneous players using shared memory to create a global game state. Players could join and leave without disrupting the game. The command structure was modeled on TOPS-10, the PDP-10 operating system. DECWAR spread significantly among university computing communities.

**Uncertain claim:** The original WAR authors and exact code ancestry are "lost to history" per available literature. The relationship between WAR and Mayfield's code is not documented.

## MegaWars and Stellar Warrior (CompuServe/GEnie, 1983/1986)

Bill Louden purchased DECWAR for $50 after hearing about it on CompuServe's CB Simulator. Kesmai (Kelton Flinn and John Taylor) discovered the copyright said nothing about commercial use, stripped Star Trek-specific IP, and launched MegaWars in 1983 — running until 1998. Stellar Warrior (GEnie, 1986–1999) was a reskin for GEnie. MegaWars III (1984) incorporated ideas from Kesmai's earlier game "S" (1979), supported up to 100 players, and ran month-long campaigns — making it a genuine proto-MMO.

## Xtrek and Netrek (1986/1988, UC Berkeley)

Xtrek (Chris Guthrie, 1986, UC Berkeley XCF) ported the trek83 multiplayer combat concept to the X Window System, introducing graphical display and mouse input. Netrek (Silvey/Smith/Chang, 1988) extended Xtrek into a fully independent client-server architecture — the first Internet-aware team game, probably first to use both TCP and UDP protocols. Source code posted to Usenet in 1989. The International Netrek League was founded in January 1992. Netrek is still played today, making it by some measures the oldest continuously-played Internet game. It derives from the PLATO Empire lineage, not from Mayfield's single-player BASIC game.

---

# 9. What Remains Uncertain

1. **Pre-Mayfield Star Trek text games.** David Ahl's claim to have played Star Trek text games at CMU in 1967–68 is unverified, lacks corroboration, and is likely a confusion with Spacewar! variants. No code, author name, or documentation from any pre-Mayfield Star Trek text game has surfaced. This should not be treated as established fact.

2. **The original WAR game.** The CDC 6600 two-player version that preceded DECWAR has unknown authors and no surviving code or documentation. Whether it descended from Mayfield's code or was independently designed is unknown.

3. **Mary Cole's specific contribution.** Ahl's acknowledgment is genuine but vague. What she specifically contributed to the summer 1973 port — debugging, code writing, testing, documentation — is unanswered in any primary source.

4. **The exact scope of Mayfield's Sigma 7 version.** The Sigma 7 version was never formally published. Whether the 1971 game differed substantially from the 1972 HP BASIC rewrite is uncertain; Mayfield says he rewrote from scratch.

5. **TREK73's awareness of STTR1.** Char began TREK73 in January 1973, before STTR1 was officially in the HP library (February 1973). Did Char know of Mayfield's game? The two games developed on the same platform type (HP 2000C) but the relationship requires further investigation.

6. **Dozens of lost variants.** Numerous mid-1970s variants were described in PCC and other newsletters with no surviving code. The Wargaming Scribe notes "ULTIMATE STAR TREK" variants in 1976 PCC issues that are otherwise undocumented.

---

# 10. Future Research Agenda

## Archives to Search

- **People's Computer Company newsletter archive (Internet Archive):** Full run should be systematically reviewed for Star Trek game listings, letters, and documentation. The January 1974 issue contains TREK73; what other Trek-related content appears 1972–1978?
- **DEC EDU Newsletter archive:** The original publication venue for Ahl/Cole's "SPACWR." Physical copies may be held at DEC-related collections or MIT.
- **HP Contributed Program Library documentation:** HP's original program catalog entries for STTR1 (Feb 1973) may contain Mayfield correspondence or metadata not yet examined.
- **Creative Computing magazine archive (complete):** AtariArchives.org hosts significant material; the complete run should be reviewed for Trek variants published 1974–1985.
- **Smithsonian NMAH collection:** Physical copy of 101 BASIC Computer Games (nmah_1465425) should be examined in person, along with any associated Ahl papers.
- **Dolph Briscoe Center for American History, UT Austin:** Holds DECWAR source code.

## People Worth Interviewing (if accessible)

- **Mike Mayfield** — the 2000 email to Games of Fame is his most detailed public account but now 25+ years old
- **Mary Cole** — her account of the 1973 port has never been publicly given; her contribution remains undocumented
- **Bob Leedom** — gave detailed email to Games of Fame ca. 2000; a more formal interview would be valuable
- **William K. Char** — creator of TREK73; his account of the parallel development and any awareness of Mayfield's game would resolve ambiguities
- **Harris Newman** — instrumental in DECWAR preservation; detailed knowledge of the WAR/DECWAR lineage

## Repositories and Code to Examine

- **dunnington.info/public/startrek/** — Pete Turnbull's original HP tape extraction; treat as primary
- **GitHub frankrefischer/STTR** — collects primary code and references
- **cyber1.org** — still-running PLATO emulation; Empire still playable here
- **netrek.org** — extensive Netrek history and source repositories
- **AtariArchives.org/basicgames/** — full BASIC Computer Games source; maintained by Kay Savetz with Ahl's permission

## Videos Worth Watching (in evidence quality order)

1. **Michael Sternberg's STTR1 playthrough** (YouTube, 2016) — plays original HP BASIC code; evidentiary
2. **"Stu" playing from 101 BASIC Computer Games code** (Twitch/YouTube) — evidentiary, demonstrates type-in process
3. **Data Driven Gamer** — systematic review of Mayfield/Ahl version; well-researched secondary
4. **Atari Archive (YouTube), Stellar Track episode** — covers Atari 2600 commercial port; retrospective
5. **Computer History Museum Spacewar! materials** (computerhistory.org/pdp-1/spacewar/) — primary institutional; essential for prehistory
6. **IF50 Substack (Aaron Reed), 1974 episode** — best single secondary synthesis of the Mayfield-Leedom chain

## Evidence That Would Most Improve Confidence

- Discovery of any pre-Mayfield text-based Star Trek game with identifiable authorship and system
- Mary Cole's own account of the 1973 DEC port
- Documentation of WAR's authorship and code origin
- Confirmation of whether Char knew STTR1 before developing TREK73

---

# 11. Annotated Bibliography

## Primary Sources

**STTR1 source code** (HP BASIC, dated Oct 20 1972 in REM header). Extracted from HP tape image by Pete Turnbull. Available: http://www.dunnington.info/public/startrek/STTR1 — The foundational artifact. The dated REM header is the key primary evidence for the game's completion date.

**Ahl, David H.** *101 BASIC Computer Games.* Digital Equipment Corporation, July 1973. First edition. Physical copy held: Smithsonian National Museum of American History, accession nmah_1465425 (second printing, April 1974).

**Ahl, David H.** *BASIC Computer Games: Microcomputer Edition.* Creative Computing Press, 1978. Contains Super Star Trek as longest program. Full text available at AtariArchives.org with Ahl's permission.

**Leedom, Bob.** Email to Maury Markowitz (Games of Fame blog), ca. 2000. Published at https://gamesoffame.wordpress.com/star-trek/ — Primary creator account, approximately 30 years after events; important but not infallible.

**Mayfield, Mike.** Email to Maury Markowitz (Games of Fame blog), December 3, 2000. Published at https://gamesoffame.wordpress.com/star-trek/ — Most detailed public statement by Mayfield about the game's origin.

**People's Computer Company Newsletter.** Volume 1 (October 1972) onward. Archive: https://archive.org/details/1972-10-peoples-computer-company — Primary distribution venue for early BASIC game culture.

**Creative Computing Magazine.** May/June 1975 issue. First publication of Super Star Trek under that name.

**Netrek Nexus overall history.** https://netrek.org/about/history_overall.php — Written by participants in the mid-1990s; primary/near-primary for Netrek lineage.

---

## Secondary Sources

**Reed, Aaron A.** "1974: Super Star Trek." *50 Years of Text Games* (IF50 Substack), January 28, 2021. https://if50.substack.com/p/1974-super-star-trek — Best single secondary synthesis of the Mayfield-Leedom chain. Carefully researched; distinguishes versions clearly.

**Wikipedia.** "Star Trek (1971 video game)." https://en.wikipedia.org/wiki/Star_Trek_(1971_video_game) — Well-cited secondary synthesis. Cross-checked against primary sources throughout this report.

**Wikipedia.** "Decwar." https://en.wikipedia.org/wiki/Decwar

**Wikipedia.** "Netrek." https://en.wikipedia.org/wiki/Netrek

**Wikipedia.** "Empire (1973 video game)." https://en.wikipedia.org/wiki/Empire_(1973_video_game) — Key source for PLATO parallel lineage.

**Wikipedia.** "BASIC Computer Games." https://en.wikipedia.org/wiki/BASIC_Computer_Games

**Wikipedia.** "MegaWars III." https://en.wikipedia.org/wiki/MegaWars_III

**Wargaming Scribe (zeitgame.net).** "Game #19: Star Trek (1971+)." https://zeitgame.net/archives/1770 — Excellent primary source synthesis; includes reproduction of key PCC newsletter excerpts.

**Wargaming Scribe (zeitgame.net).** "Game #32: Trek73 (1973)." https://zeitgame.net/archives/2775 — Best available account of TREK73's origins and lineage.

**Games of Fame (gamesoffame.wordpress.com).** "Star Trek." https://gamesoffame.wordpress.com/star-trek/ — Contains the Mayfield and Leedom emails in full; indispensable.

**Games of Fame (gamesoffame.wordpress.com).** "WAR, DECWAR and MegaWars." https://gamesoffame.wordpress.com/war-decwar-and-megawars/

**The Register.** "Star Trek: The original computer game." Tony Smith, May 2013. https://www.theregister.com/2013/05/03/antique_code_show_star_trek/

**Museum of Play (museumofplay.org).** "David Ahl: Getting Creative with Computers." January 2023.

**medieninitiative.wordpress.com.** "Super Star Trek and the Collective Serialization of the Digital." August 2013. — Academic analysis of type-in culture and Trekkie fandom overlap.

**Massively Overpowered.** "The Game Archaeologist: MegaWars." August 2022. https://massivelyop.com/2022/08/13/the-game-archaeologist-megawars-the-star-trek-online-sim-from-the-70s/

**Greenspun, Philip (blog).** "PLATO and early computer games." March 2018.

---

## Video Sources

**Sternberg, Michael.** Playthrough video of original STTR1. YouTube, 2016. Referenced at: https://github.com/frankrefischer/STTR — *Evidentiary.* Plays original HP BASIC code.

**"Stu."** *BASIC Computer Games* / Super Star Trek playthrough from book extraction. Twitch/YouTube. — *Evidentiary.* Demonstrates type-in process using actual 1978 book code.

**Data Driven Gamer.** Review of Mayfield/Ahl Star Trek. https://datadrivengamer.blogspot.com/2019/02/game-48-star-trek.html — *Explanatory/Retrospective.*

**Atari Archive (YouTube).** Stellar Track episode (Atari 2600 port). — *Retrospective.*

**Computer History Museum.** Spacewar! / PDP-1 materials. https://www.computerhistory.org/pdp-1/spacewar/ — *Primary institutional.* Essential for prehistory.

---

## Archives and Repositories

| Resource | URL / Location |
|---|---|
| People's Computer Company newsletters | https://archive.org/details/1972-10-peoples-computer-company |
| BASIC Computer Games full text | https://www.atariarchives.org/basicgames/ |
| Pete Turnbull's STTR1 extraction | http://www.dunnington.info/public/startrek/ |
| Mayfield STTR reference collection | https://github.com/frankrefischer/STTR |
| 1978 BASIC source code | https://github.com/philspil66/Super-Star-Trek |
| Working PLATO emulation (Empire) | https://cyber1.org |
| Netrek project history | https://netrek.org |
| Smithsonian NMAH (101 BASIC Computer Games) | accession nmah_1465425 |
| DECWAR source code | Dolph Briscoe Center, UT Austin |
| Ahl public domain release (2022) | https://blog.adafruit.com/2022/06/16/david-ahl-places-all-his-classic-computing-publications-into-the-public-domain/ |

---

*This report was compiled through systematic multi-track research. All major claims have been traced to at least one cited source. Where claims rest on single secondary sources, this has been noted. Where evidence is contradictory or absent, the uncertainty has been preserved rather than resolved artificially. The genealogy map reflects both documented lineage and explicit notation of disputed or uncertain connections. Researchers building on this document should treat the primary source appendix as the foundation and verify secondhand claims through the archives listed above.*
