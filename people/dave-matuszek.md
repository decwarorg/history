wrestled with esr’s file sst-doc.xml and here’s what can somewhat make sense of

# 1971 mike mayfield

The original Star Trek seems to have been written by Mike Mayfield at the beginning of the 1970s. His first version was in BASIC for a Sigma 7 in 1971; in 1972 he rewrote it in Hewlett Packard BASIC. The source is included in the SST2K repository. In January 1975 it became part of the DECUS library under the name SPACWR. While some people claim to have recollections of playing Trek games in the late 1960s, the earlier ones seem actually to have been variants of SPACEWAR, the earlier space-combat game on the PDP-1. Mayfield wrote in 2000 that he invented the Trek-style galactic grid, and the evidence seems to back that up. Some of the confusion probably stems from the fact that Mayfield's original and several early descendants were distributed under the name SPACWR. Many different versions radiated from Mayfield's original.

Most of the ones in BASIC are descended from a SPACWR version that David Ahl published in 101 BASIC Computer Games, July 1973\. This was a port of Mayfield's version obtained from the HP Contributed Programs library.

# 1973 grady hicks

Our SST2K is descended from a Taurus BASIC program by Grady Hicks dated 5 April 1973\. This does not appear to have been derived from Ahl's SPACWR. The header says "GENERAL IDEA STOLEN FROM PENN.U.", and the game has several features not present in SPACEWR: notably, the Death Ray, ramming, and the Klingon summons to surrender. And, of course, it predates Ahl's book. The source is included in the SST2K repository.

# 1973 dave matuszek, paul reynolds

Dave Matuszek, Paul Reynolds et. al. at UT Austin played the Hicks version on a CDC6600, but disliked the long load time and extreme slowness of the BASIC program. (David Matuszek notes that the Hicks version he played had a habit of throwing long quotes from Marcus Aurelius at the users, a feature he found intolerable on a TTY at 110 baud. It must, therefore, have been rather longer than the one we have.) The Austin crew proceeded to write their own Trek game, loosely based on the Hicks version, in CDC6600 FORTRAN.

Most of the code was written in 1973-1974. At that time, the game was just called "Star Trek"; the "Super" was added by later developers. In the rest of this history we'll call it the "UT FORTRAN" version. Dave Matuszek reports that the UT FORTRAN codebase he worked on in 1973-1974 was like Mayfield's original and most later versions in BASIC, in that it used used polar coordinates (a clockface angle and a distance) for manual navigation.

Tom Almy writes: "I've received further information that the black holes, Tholian web, Super Commander, and Emeritus mode were added by Marc Newman." At the time the UT FORTRAN source was last translated to C it emitted the message "Latest update-21 Sept 78". Thus, it actually predated (and may have influenced) the best-known BASIC version, the "Super Star Trek" published by David Ahl in his November 1978 sequel BASIC Computer Games. This 1978 "Super Star Trek" had been reworked by Robert Leedom and friends from (according to Leedom) Mayfield's HP port. There is internal evidence to suggest that at least some features of Leedom's SST may have derived from the UT FORTRAN version.

In particular, Dave Matuszek recalls implementing command words to replace the original numeric command codes during 1973-1974, a feature Leedom's SST also had but the 1973 and 1975 SPACWRs did not. One signature trait of the UT FORTRAN game and its descendants is that the sectors are 10x10 (rather than the 8x8 in Mike Mayfield's 1972 original and its BASIC descendants). The UT FORTRAN version also preserves the original numbered quadrants rather than the astronomically-named quadrants introduced in Ahl's SST and its descendants. Eric Allman's BSD Trek game is one of these, also descended from the UT FORTRAN version via translation to C. However, the mainline version (now SST2K) has had a lot more stuff folded into it over the years — deep space probes, dilithium mining, the Tholian Web, and so forth.

# 1977 tom almy

Tom Almy's story

Back in (about) 1977 I got a copy of the Super Star Trek game for the CDC 6600 mainframe computer. Someone had converted it to PDP-11 Fortran but couldn't get it to run because of its size. I modified the program to use overlays and managed to shoehorn it in on the 56k byte machine.

I liked the game so much I put some time into fixing bugs, mainly what could be called continuity errors and loopholes in the game's logic. We even played a couple tournaments. In 1979, I lost access to that PDP-11. I did save the source code listing.

In 1995, missing that old friend, I started converting the program into portable ANSI C. It's been slow, tedious work that took over a year to accomplish. In early 1997, I got the bright idea to look for references to Super Star Trek on the World Wide Web. There weren't many hits, but there was one that came up with 1979 Fortran sources\!

This version had a few additional features that mine didn't have, however mine had some feature it didn't have. So I merged its features that I liked. I also took a peek at the DECUS version (a port, less sources, to the PDP-10), and some other variations. Modifications I made: Compared to original version, I've changed the help command to call and the terminate command to quit to better match user expectations.

The DECUS version apparently made those changes as well as changing freeze to save. However I like freeze. I added EMEXIT from the 1979 version. That later version also mentions srscan and lrscan working when docked (using the starbase's scanners), so I made some changes here to do this (and indicating that fact to the player), and then realized the base would have a subspace radio as well — doing a Chart when docked updates the star chart, and all radio reports will be heard.

The Dock command will also give a report if a base is under attack. It also had some added logic to spread the initial positioning of bases. That made sense to add because most people abort games with bad base placement. The experimental deathray originally had only a 5% chance of success, but could be used repeatedly.

I guess after a couple years of use, it was less experimental because the 1979 version had a 70% success rate. However it was prone to breaking after use. I upgraded the deathray, but kept the original set of failure modes (great humor\!). I put in the Tholian Web code from the 1979 version.

I added code so that Romulans and regular Klingons could move in advanced games. I re-enabled the code which allows enemy ships to ram the Enterprise; it had never worked right. The 1979 version seems to have it all fixed up, but I'm still not overly happy with the algorithm. The DECUS version had a Deep Space Probe.

Looked like a good idea so I implemented it based on its description. I imported CAPTURE from BSD Trek. 

# 2004

Stas Sergeev's story 

I started from an older Tom Almy version and added features I had seen in other mainframe variants of the game, I wrote a screen-oriented interface for it based on the curses library. The Space Thingy can be shoved, if you ram it, and can fire back if fired upon.

The Tholian can be hit with phasers. When you are docked, base covers you with an almost invincible shields (a commander can still ram you, or a Romulan can destroy the base, or a SCom can even succeed with direct attack IIRC, but this rarely happens). SCom can't escape from you if no more enemies remain (without this, chasing SCom can take an eternity). Probe target you enter is now the destination quadrant.

Before I don't remember what it was, but it was something I had difficulty using. Secret password is now autogenerated. Victory plaque is adjusted for A4 paper rather than 132-column greenbar :-) Phasers now tells you how much energy needed, but only if the computer is alive. Planets are auto-scanned when you enter the quadrant.

Mining or using crystals in the presence of the enemy now yields an attack. There are other minor adjustments to what yields an attack and what does not. Ramming a black hole is no longer instant death. There is a chance you might get timewarped instead.

"freeze" command reverts to "save", most people will understand this better anyway. Screen-oriented interface, with sensor scans always up. My changes got merged into SST2K in 2005\. Eric Raymond's story I played the FORTRAN version of this game in the late 1970s on a DEC minicomputer.

In the late 1980s Dave Matuszek and I became friends; I was vaguely aware that he had had something to do with the original Star Trek game. In October 2004, sitting in Dave's living room, we got to talking about the game and I realized it would make a great exhibit for the Retrocomputing Museum. A few quick web searches later we found Tom Almy's page. We downloaded his code and Dave verified that that it was a direct descendent of UT Super Star Trek — even though it had been translated to C, he was able to recognize names and techniques from the FORTRAN version he co-wrote.

# esr notes

This game became an open-source project; see the project site. After I launched the Berlios project, Stas Sergeev contacted me. We worked together to merge in his changes. Modifications I've made: I converted the flat-text SST.DOC file to XML-Docbook so it can be webbed.

(That's what you're reading now.) The command-help code needed a rewrite because the flat-text form of the documentation is now generated from XML and doesn't have the easily recognizable section delimiters it used to. I wrote a script to filter that flat-text form into an sst.doc that's easy to parse for command descriptions, and changed some logic in sst.c to match. I've cleaned up a lot of grubby FORTRANisms in the code internals — used sizeof(), replaced magic numeric constants with \#defines, that sort of thing. Later I translated the code from C to Python.

I fixed a surprising number of typos in the code and documentation. All the game state now lives in one big structure that can be written to and read from disk as one blob. The write gives it an an identifiable magic number and the thaw logic checks for same. I made the internal pager work, and in the process got rid of a number of platform dependencies in the code.

The HELP/CALL/SOS command is now MAYDAY. Status report now indicates if dilithium crystals are on board. At Dave's prompting, restored the Space Thingy's original elusive behavior. Clean separation of game engine from the UI code, improving Stas Sergeev's excellent work on the curses interface.

Here are some good pages on the history of Star Trek games: http://www.dunnington.u-net.com/public/startrek/ http://www3.sympatico.ca/maury/games/space/star\_trek.html http://www.cactus.org/%7Enystrom/startrek.html Authors' Acknowledgments These are the original acknowledgments by Dave Matuszek and Paul Reynolds: The authors would like to thank Professor Michael Duggan for his encouragement and administrative assistance with the development of the Star Trek game, without which it might never have been completed. Much credit is due to Patrick McGehearty and Rich Cohen, who assisted with the original design of the game and contributed greatly to its conceptual development. Thanks are also due to Carl Strange, Hardy Tichenor and Steven Bruell for their assistance with certain coding problems. This game was inspired by and rather loosely based on an earlier game, programmed in the BASIC language, by Jim Korp and Grady Hicks.

It is the authors' understanding that the BASIC game was in turn derived from a still earlier version in use at Penn State University. References These are the original references by Dave Matuszek and Paul Reynolds: Star Trek (the original television series), produced and directed by Gene Rodenberry. Star Trek (the animated television series), produced by Gene Rodenberry and directed by Hal Sutherland. Also excellent, and not just kiddie fare.

If you enjoyed the original series you should enjoy this one (unless you have some sort of a hangup about watching cartoons). The Making of Star Trek, by Steven E. Whitfield and Gene Rodenberry. The best and most complete readily available book about Star Trek.

(Ballantine Books) The World of Star Trek, by David Gerrold. Similiar in scope to the above book. (Bantam) The Star Trek Guide, third revision 4/17/67, by Gene Roddenberry. The original writer's guide for the television series, but less comprehensive than (3) above.

(Norway Productions) The Trouble With Tribbles, by David Gerrold. Includes the complete script of this popular show. (Ballantine Books) Star Trek, Star Trek 2, ..., Star Trek 9, by James Blish. The original shows in short story form.

(Bantam) Spock Must Die, by James Blish. An original novel, but rather similar to the show The Enemy Within. (Bantam) Model kits of the Enterprise and a Klingon Battle-Cruiser by AMT Corporation are available at most hobby shops. Setting the Wayback Machine SST2K and its ancestors have a long history.

One of the objectives of this project is to make that history available. Accordingly, here is a timeline of the development of SST2K and its ancestors, as closely as we can reconstruct it. Someday this may become the basis for a "wayback machine" switch that enables feature sets by year. 1971 — Mike Mayfield's original BASIC Star Trek.

# timeline

5 April 1973 — Grady Hicks's BASIC version fot the Taurus. Summer 

1973 — Dave Matuszek, Paul Reynolds, and the Austin crew begin work on the UT FORTRAN version.

1974 — Dave Matuszek gets distracted by other things, notably a job change and the birth of his first child. 

21 September 1978 — This was the date on the first FORTRAN version Tom Almy saw, on which he based his later C translation.

1979 — Marc Newman adds Tholians, super-commanders, and Emeritus mode. 1995-1996 — Tom Almy translates his FORTRAN port to ANSI C. 1997 — Tom Almy finds the sources for UT FORTRAN on the Web and merges in features new since the 1978 version: EMEXIT, Tholian Web, improved death ray. He adds deep-space probes from the DECUS version.

10 October 2004 — ESR starts hacking on Almy's C translation, de-FORTRANIZING the code. HELP/CALL/SOS becomes MAYDAY. 30 October 2004 — SST2K project started on Berlios. 18 January 2005 — First changes merged in from Stas Sergeev.

The curses interface is added. September 2006 — BSD features merged in. Inhabited-worlds features and weighted critical hits date from this time. 9 October 2006 — Translation to Python.

1 March 2017 — Color added. Cloaking device and capture command added from BSD (via Almy's 2013 version) 25 March 2019 — At long last, chart entries are uniformly dot-filled. (Suppressed in the plain and almy interface styles.) 25 August 2023 — Coordinates optionally in alphameric mode, e.g "b3" rather than "2 \- 3". (Suppressed in the plain and almy interface styles.) One as-yet unanswered question is when the code changed from distance/direction navigation to coordinate offsets.

Dave Matuszek believes it must have been after he stopped working on the game in 1974\.

