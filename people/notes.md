
# 20251122

Noah — 16:32
and joel and me were saying during the game - too many planets, least for effectively a few players - twenty would have been fine
would like to get python robots compatible - then a simple test can be - do they reach victory conditions in thirty forty minutes 🙂 
Eric — 16:48
i'm matching the codebase on that one
const nplnet = 80; // to jibe with 2.2, start with 80, 20 of which will become bases
are your bots just using the text interface or built into the codebase?
Noah — 16:54
they are pure text interface - exactly like a human - they use telnet, start game, play🙂 
they are indistinguishable from a human telnetting in 👍
https://statespace.dev/decwar-game-length.html
statespace.dev
decwar game length
memory is that typical ‘all out’ decwar games, san marcos 83/84, were around thirty to forty minutes, and an ideal afternoon would be two or three intense games complete with ‘report to slave planet’ or ‘the galaxy is saved’ messages. then go swimming/tubing in the san marcos river. as project utexas and robots have gotten smoother o...
nutshell - it's a 'control knob' on the game - can be changed for different environments 
Eric — 16:59
ah should be easy to get those working
just have to make sure i'm totally in sync with original
Noah — 16:59
source code has commented out - 20 min, 80 max
understood - am just giving some context
Eric — 17:02
yea 20 min would be bases only
well maybe
Noah — 17:02
it's a control knob - not a canonical truth 
Eric — 17:03
question is, is 80 max what i have, or is that really 80 neutrals
Noah — 17:04
we're discussing number of planets at game start - in addition to the twenty bases at startup
Eric — 17:05
Good question for Bob
if he remembers
Noah — 17:06
for me the source code is very clear - and excellent topic for bob🙂 
jakydude — 17:06
yeah i recall you could choose short, medium, or long game.  or provide a hash code of sorts.  if you chose to generate a game, it would generate a game - and it would provide a hash number of sorts that could be used to reproduce that same game later if you liked it.
jakydude — 17:07
i think that’s 80 neutral planets plus the 10 bases on each side

jakydude — 17:16
i could be remembering wrong.  or maybe mark hittinger did some custom coding.
Eric — 17:16
are you thinking short, medium, long output modes?
jakydude — 17:16
yeah sorry maybe mark wrote that code for the UofL version
he was known to customize every facet of the DEC-10
Noah — 17:17
active variable was 60 and i tuned it to 20 for utexas
Eric — 17:17
Joel, that brings up a good point, we wnat to start interviewing folks (players and anyone with knowledge). You are first on the list, do you know others we should try to find or reach out to?
Definitely want to ask Bob about the num planets
jakydude — 17:19
if mark H could be found, him for sure.  he would at least know others in louisville that were fans.  i haven’t been able to find mark.
Noah — 17:19
'planet fuel' - more for lots of players, less for fewer players
Eric — 17:19
what is his last name
jakydude — 17:20
there was a guy named david, forgot his last name.  went by “mole” (which fit pretty well).   smart guy but always seemed to be in life trouble.  somehow doubt he is still alive, but he would be good to contact if he could be found. 
Eric — 17:20
he was UK or UL
jakydude — 17:21
mark hittinger
Eric — 17:21
thanks, Mark H worked at UofL?
jakydude — 17:23
yes he ran the DEC-10.   knew it top to bottom.  moved to vax systems running VMS after the DEC-10 shut down.  part of that was at UL, but i think he moved a little while after.
Eric — 17:23
ok, no idea how old he was at the time?
jakydude — 17:29
i never met him (best to avoid the person who wants you off his system).   so can only guess.  he had a son in 1980 with his then wife (think they divorced).  her name was theresa i think?  just giving some data for web searches.  you can find him talking about his mazda (RX7??) in some old group archives.  anyway my guess is he is about 65-70 now.
jakydude — 17:37
probably explains why he isn’t showing up on social media, etc.  or he could have died.  i don’t know.
Eric — 18:02
yea, like that woman that ran the UK center did
jakydude — 18:05
yeah
Noah — 18:05
k, home on laptop - thinking this's another recurring theme - so started a new 'nutshell page' - how's this, up top, here? 🤔 
https://gitlab.com/decwar/history/-/blob/main/technical/game-length.md?ref_type=heads 
GitLab
technical/game-length.md · main · decwar / history · GitLab
collaboration around preserving decwar history https://www.youtube.com/@statespacedev
Image
can well believe should throw these nutshell pages into ai and make them clearer - may try that this weekend 👍
hold on 
just a sec - let me get it perfect
markdown is having a hard time with the formatting
Noah — 18:13
it's really stuggling with the mac10 comments 
well, it's best can do right now - will try to improve that and make it easier to read - but let's try link above for now 👍
Noah — 19:08
ahha! realized could build and test 🙂  fired up docker containers (utexas does a fresh build on every startup), telnetted in, got super powers, and did list - result is included at link above now 👍 
Eric — 19:51
what is currently the best way for me to run the old version
PiDP or something else
Noah — 19:53
oh dear, excellent question....
we're smack in the middle of this transition
eric if you have docker desktop on your daily driver - let's please try nextgen docker
it will be pain - but there's gonna be speed bumps any direction we go right now 😳
please get docker desktop going, where you can do one of their 'hello world' deals - and then we can step by step create the readme for nextgen? 🤔 

# 20251114

Noah — 03:04
one brainstorm to have on the radar - my 'cic' api and coming 'control center' webpages will be controlling decwar dec10 container and python robots telnetting into it -
here's the thing - the python robots are 'merely other players' - to decwar dec10 they are 'just players'
now - if the exact same robots can connect to decwarjs and play - we show that old and new are matching
it's almost a bizarre kinda turing test? 😄  are the robots playing on a dec10, or on decwarjs?
Eric — 03:05
yea, what we really need to do is train an AI on it
Noah — 03:05
so making robots able to play with old and new is some kinda weird experimental something
Eric — 03:05
simliar to what deep mind did with the atari games
just not sure what the right technique is
has nothing to do with LLMs
Noah — 03:06
yep - this is the infrastructure for that - deploy 100 containers in the cloud (kubernetes) and let robots play
or 1000 containers, 10k, etc - that's one of the points of containers and k8s
so they learn to play well - the separate thing that i'm really about is giving them personalities -
bringing back the vibe of san marcos 1983
Eric — 03:12
yea the deep mind technique will probably not result in personality, just ruthless players
Noah — 03:12
agreed - completely separate topics in my mind -

yes! it does work, their instruction manual is decent for its
Eric — 06:50
yea, is fun to see the old MIT stuff though
okay so all the games are under cwd games
Noah — 06:52
yep, did the tour myself and thankful for it - they did a great job putting it all together - it's lars's baby
yep you'll see 'trek' or something like that there - for the star trek game 
put your self in my shoes june 2024 - have played what's there and interesting, including star trek game - then think... hmmmm, that decwar code on github... can it run on this? 🤔
that was me
Eric — 06:54
yea amazing
Noah — 06:54
you realize right away - ahha! need to try the tops10 config...! boom, goodbye its hello tops10 🙂
Eric — 06:55
yup! such a strange synergy all this was
Noah — 06:56
took me three four hard months to get decwar going, with help from merlyn
round november was like alright - let's keep going and go all the way - build and run an entire decwar tops10 system from scratch (tape images) - got that working around new years?
ok, yeah, then - early 2025 - allright - we gotta decwar dec10 from scratch - but it has 10 players!
hmmm, can we reconstruct the utexas 18 player? and look at these files about the original tape structure...
project utexas was born - merlyn was half hearted - announced it on the goog group and the rest you know 🙂 
Eric — 07:02
yea

This short video traces the origins and impact of DECWAR, the groundbreaking 1978 multiplayer computer game created at the University of Texas. The film opens by setting the stage: the late-1970s era of mainframes, shared terminals, and the early stirrings of online play. It then introduces the UT students who adapted the Star Trek–style strategy game into a uniquely competitive, simultaneous-multiplayer experience that pushed the limits of the DECsystem hardware.

As the story unfolds, viewers see how DECWAR transformed a simple text interface into an intense tactical battlefield where dozens of players could join, compete, and cooperate in real time. Through reenacted terminal screens and narration, the video highlights the game’s innovations—persistent universes, team-based combat, and social dynamics that would foreshadow modern online gaming.

The final arc explores DECWAR’s legacy: how a small campus passion project quietly influenced the design philosophies behind later networked games and helped define the culture of early multiplayer computing. The video concludes by reflecting on how a handful of students, limited tools, and a lot of curiosity helped spark concepts that now dominate the gaming world.


# 20250603

From: Harris Newman <harris.s.newman@gmail.com>
Date: Tue, 3 Jun 2025 06:57:04 -0700
Subject: Re: history question
To: Noah Smith <noah@statespace.dev>
Cc: eric.freeman@utexas.edu

I was on usenet (alt.sys.pdp10) in the early 90's searching, pleading for
someone to release the code.  I at that time used sdf.org for email.  (If
you don't know about sdf.org, it's out of San Antonio, and is a bunch of
unix servers that are exposed to the internet.  He runs several pdp-10
simulations on it as well, which you can get access to for free.  I got a
lifetime membership for like $35 and still use it!).

I got an email around 1995 with a large mime attachment with the source
code on sdf.org.  I am sure I got it around then because I remember other
things that set that year (I was married to my 1st wife then, etc).

I normally keep my old emails (esp so important as this one), but I can't
find it now (I looked multiple times on sdf.org too).  I had a ton of cd's
and floppies with it backed up that I went through last week but none have
the original email.   I moved from Round Rock to Portland Oregon 4 years
ago and during that time we downsized multiple times and most of my
floppies/cd's are gone.

I had no way to distribute the code until I came across the Dolph Briscoe
Center for American History, and in 2011 and arranged for the return of the
code to UT, for distribution.

It's frustrating to me that I can't find that email.  I'm going to continue
looking, but I am losing faith that I can find it.  Those floppies I
had...I am so frustrated that I didn't keep them.

I do have emails of who I talked with at the Briscoe center, it was Zach
Vowell,
Hope this helps,  So, when can we play a game?
HN

On Mon, Jun 2, 2025 at 8:47=E2=80=AFPM Noah Smith <noah@statespace.dev> wro=
te:

> hi harris - just curious, and have cc'd eric here because we were just
> discussing -
> did you get the compuserve code from compuserve personally? and if so -
> when, how, where did that happen? sometime around 2010 maybe?
> eric and me are going to talk with a briscoe person tomorrow, and will as=
> them for 'best practices' around creating a new catalog item for the new
> 'utexas23-reconstruction' - how to document the history, etc:)
> cheers,
> noah

# 20250604

Noah — 00:19
so after sleeping on it a bit, realized we should update joel - we got a beautiful reply from harris today. here's a nutshell -
harris was on alt.sys.pdp-10 in the early nineties, hunting for decwar source code - i was lurking there too and suspect i remember this 
in 1995 somebody sent harris an email with the compuserve source code attached
that original email is now lost and we don't know who the sender was 
to add one additional fact, merlyn got the compuserve code from harris and around 2012 did some intense hacking and got it to run on simh pdp-10. he put that on github at that time. merlyn has said he was using ddt debugger to accomplish that - it was a major achievement. 
with project utexas, roughly april and may this year we set out to start from the compuserve code and go backwards, to converge back on the utexas original and to make it more easily usable by more people. and now here we are 

jakydude — 08:06
wow that’s all so cool
so “he put that on github at that time” means it is on github?  the version you started with?  or it was put and then lost?

Noah — 08:14
yep the github repo drforbin decwar is the compuserve code that merlyn got from harris and debugged in 2012.
for a little more detail about that compuserve code - it is essentially the tape that utexas sent to compuserve in 1982
compuserve added a few things, and modified a few things - but the skeleton is all there - pure 'utexas tape'
so what we're doing now in 'the utexas folder' is washing out the compuserve impurities - we want it to look, taste, smell and feel like the original utexas tape - and everyone to be able to easily use it on their raspi
and the dream is - if we can recover a real life physical original utexas tape - it will match up closely with our 'utexas23-reconstruction' 
this is all what we mean by going 'backwards in time'
it's fun, and not impossible - the key thing is that our starting point is actually close to the destination - the compuserve impurities are pretty minor - cosmetics basically 

20250608

this is fun - hit some kinda milestone - 
have multiple 'agents' telnetting in from laptop and 'playing the game'!
it's alive!!!
the agents are super brainless - just randomly moving around 😄 
but they create a 'game loop' and drive the action - the romulan is jumping in and creating some mayhem😄
not even going to begin thinking about adding brains to the agents, aka 'machine learning training em', yet - for this weekend will just add fun things like look for targets, and auto attack if anything's in range🙂
wow, brainstorm - will put a cli on the agent code and have a shell script start a few agents on each side
will start creating personalities for some of them already - dialog for them to send over the radio
Eric — 00:40
cool
Noah — 00:41
a memory came back - back in the day, had just seen blade runner
would play as 'batty' and radio stuff like 'fiery the angels fell' etc
Eric — 00:42
i worked in a movie theater when Bladerunner came out
Noah — 00:42
batty will ride again this weekend!
Eric — 00:42
very fun to watch reactions of people leaving after the movie
Noah — 00:43
can have some fun star trek personalities too - scotty lives!
and bones mccoy;)
he's dead, jim:)

looking at eric's folder listing, here's a fun historical note - compuserve had each command as a separate file - so torpedo, tractor, tell, etc - merlyn worked on and debugged that compuserve code from 2011/2012 onward - makes tons of sense and totally natural, no problemo 
then the pidp-10 came out around a year ago -
my first thought was of course 'hey, let's get that github decwar going, it uses simh so can go on raspi and pidp-10'...! 
so i started looking more and more intently at that big pile of files there in the github repo - what you see in the root of the main branch is the starting point - simply a huge pile of files, unstructured, no signals what really matters and what not - 99.99% that this is exactly what merlyn got from harris around 2011, and what harris received as an email attachment in 1995 (what's there in the root has been debugged enough by merlyn, it was my starting point and was able to build and run it pretty quickly) 
now, here's the first exciting discovery - sometime last fall? 
first this one https://github.com/drforbin/decwar/blob/master/utexas/utexas23-reconstruction/hlp/DECWAR.IMP - and then https://github.com/drforbin/decwar/blob/master/utexas/utexas23-reconstruction/hlp/DECWAR.TAP and https://github.com/drforbin/decwar/blob/master/utexas/utexas23-reconstruction/hlp/DECWAR.LTR 
Noah — 07:13
as i studied these, there were the very first glimmers of 'project utexas'  in the old brain - 'ahha, there's deeper layers of archeology here!' 😍
this's how 'project utexas' and the concept of 'going backwards' were born - it's been a complete and total surprise, and has really evolved from zero - there was nothing this time last year - it took a loooooooong time for all the puzzle pieces to fit together and understandings to grow - latest big breakthroughs were very recent, april and early may, right around when eric and me first met! 
Noah — 08:11
i'd say, fully formed concept was there around christmas - begin telling merlyn about it there over the holidays, and he was rightfully skeptical - call with merlyn in april was when flat out declared, it's happenin, and he blessed it all with 'will be happy to see it in action'. btw fwiw merlyn's working in the 'development' branch - that's where he has his 'cloaking device' code going. 
he's done really cool and fun stuff there - the way it works is, if you build on a planet, there's a probability your science officer will say 'sir, we've discovered an ancient ruin with cloaking technology' - you then get the ability to cloak

Where did you and Merlyn meet?
I'd seen some references to normal ships cloaking and wonder what the story was
Noah — 17:22
purely through the github repo - roughly a year ago - once i was able to run the compuserve code there in the repo, on top of simh pdp10 tops10, confirming it was all legit, contacted merlyn to discuss directly 👍
ar first, it was purely to try to figure out what the heck was going on in that code and what the big pic story with utexas and compuserve was😄
needless to say, it was very confusing understanding the roles of harris and merlyn, on top of everything else😄
Eric — 19:10
what were their roles with respect to the two original developers
finally back together:
Image
refactored but i had to touch way too much code (converted from (x,y) to (v,h) for one thing.  To quote another movie, I bet it has more bugs than a bait store.
Noah — 21:36
looks good! agents are much more robust now - they've been playing for many hours now - going to start a little personality now just for fun - we have monday off here
they have not been in direct  contact with the two developers - what shannon mentioned with briscoe speaking to bob is the only contact i'm aware of - pretty special!👍
Eric — 21:40
Oh did she say they'd actually spoken?
Noah — 21:43
yep, something like 'briscoe did contact bob, and he stated he doesn't have any source code' - not too surprising - q is if he has any clues towards places that would have tapes;)
Eric — 21:45
oh okay
he's the JP Morgan VP?
Noah — 21:45
yep, chicago guy
Eric — 21:46
So is pretty much nothing known about why this game was created or exactly in what org at UT?
Noah — 21:49
well, because of those earlier single player versions - there was some kind of 'community' at utexas, and it seems to have had ties to the cc. and cs and ee? this is a part i'd like to explore
and note eric raymond states he has worked with one of the utexas 'super star trek' devs - so there is more out there to learn, for sure!
this is why i say, for some library school grad student - their dissertation would write itself😀
between like 73 and 83 something very special happened at utexas
Noah — 21:59
as project utexas goes backwards in time, at some point it will bump into the two player 'war' on the cdc6600 and the single player 'super star trek' - all right there in the cc - the hardware was definitely big iron in the cc 
Eric — 22:03
yea i need to check out those precursors
Noah — 22:06
yep, the story gets extremely complicated there, but the utexas fortran 'super star trek' seems to be the root genetics throughout
so we know of like five to ten descendants of decwar - seems to be like a factor of ten more descendants of super star trek😮
Eric — 22:34
have you tried to talk to any of those folks
Noah — 22:39
not yet:) would love to know more and looking forward to it - just taking one baby step at a time, always 'backwards', hahaha
Eric — 22:46
http://www.catb.org/~esr/super-star-trek/sst-doc.html#idm161
historical research by
                 Eric S. Raymond
Noah — 22:50
yep - discovered esr's stuff just a few months ago - huuuge eye opener
Image
Image
dave matuszek - this is the guy esr has been working with 👍 and/or paul reynolds!?:) 
there's tons of stuff piled up and hidden in this repo - have had good luck with a local clone and using search https://gitlab.com/esr/super-star-trek
Noah — 23:03
have renamed 'monitor' to 'nomad';)
Image
Eric — 23:24
ah good history overview there
any sign of the 1978 basic version?
Noah — 23:25
total respect for esr in this regard - had a similar experience with him on a separate topic - he thinks for himself and is persistent
Eric — 23:26
https://gitlab.com/esr/super-star-trek/-/blob/master/historic/UT-Trek.basic?ref_type=heads
GitLab
historic/UT-Trek.basic · master · Eric S. Raymond / super-star-tr...
Super Star Trek is almost the oldest of all heritage computer games, originating in 1973 on the CDC6600. This port has been prepared with the assistance of the...
Image
Hmm I wonder which verison of basic
Noah — 23:27
clone that repo and search it - huge pile of stuff in there -
good question
Eric — 23:29
https://www.youtube.com/watch?v=L-XWl9x13PU
YouTube
Space Game Junkie
January, 2015 Game of the Month: Super Star Trek - Entry 1 - Riding...
Image
Noah — 23:30
thinking, don't know much at all on those topics!🤔
awesome!
Noah — 00:02
btw, very highly recommended!!! and the author also has a book about basic😉
Image
Eric — 00:07
oh interestng, have not come across that 
Noah — 00:08
excellent read - good author - real cs guy, and can write
Eric — 00:09
i see his BASIC book too
okay we were debating how a game ends, here's the definitive way in your ut source code:

This routine is called whenever a base or planet is destroyed
C    to see if the game is over. (all the planets gone, and one
C    side's bases).  If so, the appropriate message is printed out
C    and the job is returned to monitor level.

Note I don't think this rules out a tie.
Noah — 00:12
looks like the real answer right there -
Eric — 00:12
yea
and makes sense
Noah — 00:13
yep totally agree - 'get the planets and bases'


ok! good news - the three amigos have run nicely for over six hours! no obvious bugs for them, at least ❤️ 
dam

All devices functional.
let me try to get a little damage...
ahha! boom - memory bug right away 

** Lockup on queue Q by job 528
Fatal ENQ. error code 5?
?Illegal memory reference at user PC 463224

Eric — 06:19
wow
Noah — 06:19
it was bringing in this fourth ship - from a normal interactive terminal session
saw something similar a couple times yesterday about the 'Q' - at least that's one clue
ok, well this is probly telling us something, good to know 👍
after going for six hours with three players of the same type - bringing in a fourth player of a slightly different type was a prob for 'the Q'
Hmm the Q wasn’t even a thing yet was it in this timeframe
Noah — 06:29
think it's just shorthand for queue - there's definitely a 'command queue' - hmmm, wonder if it concerns the 'timing topics' eric?
could be of interest
real quick before i forget - note to self! there was also something odd with tops10, before entering the game - had to login as decwar, not demo - file permissions were wrong for demo, which shouldn't have been true, at all? 


the new ship
**** Lockup on queue Q by job 514
?atal ENQ. error code 5
?Illegal memory reference at user PC 463224

an older ship
**** Lockup on queue F by job 526
Fatal ENQ. error code 5

**** Lockup on queue Q by job 526
Fatal ENQ. error code 5
**** Lockup on queue F by job 514
Fatal ENQ. error code 5?
?IO to unassigned channel at user PC 455426

20250612

it was bringing in this fourth ship - from a normal interactive terminal session
saw something similar a couple times yesterday about the 'Q' - at least that's one clue
ok, well this is probly telling us something, good to know 👍
after going for six hours with three players of the same type - bringing in a fourth player of a slightly different type was a prob for 'the Q'
Eric — Yesterday at 06:25
Hmm the Q wasn’t even a thing yet was it in this timeframe
Noah — Yesterday at 06:29
think it's just shorthand for queue - there's definitely a 'command queue' - hmmm, wonder if it concerns the 'timing topics' eric?
could be of interest
real quick before i forget - note to self! there was also something odd with tops10, before entering the game - had to login as decwar, not demo - file permissions were wrong for demo, which shouldn't have been true, at all? 
eric i'll try to get a good damage example today - have to get started here, slept late:)
Noah — Yesterday at 06:36
Image
lots more following that code - lots of qmanager stuff👍
for now, starting four agents together - see how long they go
Eric — Yesterday at 06:54
cool!
Eric — Yesterday at 07:04
deep down this timing stuff is a little crazy
based on players using time consuming commands
Noah — Yesterday at 07:06
guessing will be learning many things about these topics 🤔 😄 
will be studying warmac a bit more today - try to get an overview
Noah — Yesterday at 12:18
funny, feeling is that in just the few days since agent was 'invented' had been getting a valid feel for the boundaries of the problem / challenge - nutshell - three agents good, four agents bad! four seems to be a bridge too far 
and now with more stress testing those questions about tty / telnet are growing - evidence seems to be piling up that problem is in i/o and the tty situation - have noticed some more curious things this morning! 😄  so, with old school we're on the path, climbn the mountain 👍 
Noah — Yesterday at 12:40
fwiw btw, suspect merlyn wouldn't have seen this stuff since he probly didn't have many 'ships in the game' simultaneously - doubt he had anything like 'agents' - will discuss with him next time it makes sense - meanwhile, still lots to learn 'beginners brain' style 🤔 
Noah — Yesterday at 13:48
https://groups.google.com/g/pidp-10/c/k_2wizDtcdE/m/AqCGesrqAwAJ - asked the google group - 😄 
Noah — Yesterday at 14:28
there ya go eric🙂
Image
Noah — Yesterday at 14:36
good grief - may have fixed it!😮  four laptop agents and three raspi players are doing fine 
one liner - set tty lines=16
may not have been enough lines - if this holds up will put in a commit later today
Noah — Yesterday at 14:45
eric this really seems to be it 😍  - please make sure to have this little one liner fix in your local utexas 🙏  https://github.com/drforbin/decwar/commit/d26d360b18c9fac49549d0b7bd68412ebd89835c 
Noah — Yesterday at 14:55
really looking like we can celebrate - seven ships, everything looking great! 🎉
Eric — Yesterday at 15:41
perfect thanks!
Eric — Yesterday at 16:19
Image
Noah — Yesterday at 16:20
looks good!
Noah — Yesterday at 17:20
three hours of brainless mayhem with seven ships - we got it! radio does seem to need a fix - but that's a separate topic 🙂
Image
Eric — Yesterday at 21:32
what's the radio do
Noah — Yesterday at 22:18
radio was just lazy way of saying 'tell' - nomad is doing 'tell all' and that should be received by six ships, not four as in the pic
Eric — 01:55
as long as radio on
and not radio damaged
Noah — 03:35
ahha, woke up with a guess what's happening - picture the 'usual list' of ships - fed then emp
the ships with radio trouble are at the bottom of the list!
betcha a tribble the first ten ships are ok and the last eight are not ok
there's a cis value of 10 somewhere that needs changing 18
Eric — 03:38
see if they have radio damage as well, that will defeat
Noah — 03:38
their silly ten ships again!
shoooould be able to hunt this down quickly, another cis thing to be 'reconstructed' backwards to utexas:)
they enter the game with radio silence - brand new ship, cant send or receive
but nothing worse - everything else seems ok, but radio silence
Noah — 03:47
never mind! shot that theory down already
just joined game as wolf - it can send!
but not receive... ok may be something to the theory - but just for receive, send is ok 
running eight hours now, eight ships - ahhh it's really nice to see - we're in really good shape - can start evolving the agent:)
Noah — 04:14
argh, really shot the theory down now - no good idea yet why some ships have a prob sending🤔
this could be a 'fun' bug hunt
Eric — 05:46
hmm so some ships can receive radio but some aren't?
Noah — 06:06
it's confusing - sorry for thinking our loud here😄  for many ships the radio is fine - for a few, can receive but not send - and for a few, can do neither - very confusing situation - main thing is, there's def a bug in the radio👍
Eric — 06:07
ah yea seems there are some bugs in there
Noah — 06:07
it's only annoying, kind of an edge case - but wanna stomp it
yep, for sure - side effects from our friends at cis, no doubt about that
Eric — 06:08
https://www.youtube.com/watch?v=ksL232PHivI
YouTube
Bob Alexander
Star Trek, and the evolution of a BASIC programmer
Image
Noah — 06:08
it's doing great overall, but some good improvements to be done
he's got a vt52 sitting there!!! jealousy!!!😳
Eric — 06:11
Attachment file type: acrobat
Super Star Trek.pdf
1.12 MB
Noah — 06:18
pdf is sweeeeeet!!! nice! see - we're gonna be piling up a huge mountain of stuff, especially with the single player versions - could be worth getting methodical - we'll see! 🤔 
Eric — 06:19
https://www.youtube.com/watch?v=1Q_4k41Y7eM
YouTube
Bob Alexander
The Other Star Trek Game
Image
to be complete here's the entire book:
Attachment file type: acrobat
YXpsme-Basic_Computer_Games_Microcomputer_Edition_1978_Creative_Computing.pdf
12.81 MB
He seems like a good resource (Bob Alexander)
https://www.galacticstudios.org/
Noah — 06:25
yeah i recognize his name - let's find out how he connects with esr - the potential problem with esr is he's such a militant unix fanboy🤔 
and with the single player stuff, especially the basic stuff, there's a loooooot of people - have seen some off-putting arguments about who did what first over there
Eric — 06:33
the text game is interesting
Noah — 06:34
i really wonder if i played it - am 95% certain i messed with it for like five minutes - early or mid eighties
messed with several versions of the single player game, but never got into it
decwar was just in a completely different universe😍
Eric — 07:52
okay, the refactored version i think is very buggy, but it is up
http://decwarjs.com/ or telnet decwarjs.com
no idea how well the browser verrsion works, haven't played with it much
now seeing this on pdp: 

 Command: points all
Too many words -- line ignored
Noah — 09:18
awesome! will play with it later today 👍
weird - old school has been running non stop here with eight ships
after adding that line, didja restart simh - boot from disk.ini ?🤔 
Eric — 09:22
havent done that yet
Noah — 09:22
that brings in the fix👍
Eric — 09:22
cool
Mk — 09:22
You guys! Talking bout old labs.. just came across photos of a cad machine I got to use at Umass circa 1987…
Image
Image
Image
So freaking cold in there yiu had to wear full winter gear inside
Noah — 09:23
close to 24 hours now🎉 
Image
Eric — 09:25
i've switched to IP addresses
Image
Noah — 09:25
hahaha - i had a winter coat in 'office'
Mk — 09:25
Can’t see it super well.. but I recreated the pencil drawings of falling water
Image
Eric — 09:25
wow good eye
Mk — 09:26
There was a skinny long window and if campus cops saw a light on they would pop in.
Brought me cocoa more than once. After seeing how cold it was in there
Noah — 09:27
nice - what year mk?
Mk — 09:28
Ps my one and only pair of Calvin Klein acid wash jeans..
Noah — 09:28
ah 1987!
just caught it
Mk — 09:28
Yeah… I’m guessing
I mean, obvs tye outfit is timeless.. so hard to eyeball it
Noah — 09:32
mk do you remember much lisp stuff and what that lisp machine was like?
ah i missed something
cad - not cadr!
Mk — 09:33
Nope. I forgot I made a 10 foot by 10 foot architectural plan
Noah — 09:34
sorry - i was just reading about lisp machines and was stuck in my brain!
roughly what type of machine are ya using in the pics?😀 
Mk — 09:44
Trying to remember..  it was donated.. had a fax 11/780 in grad school.. but this machine was cad only
Fax. Ha. I said what I said autocorrect! Vax
Noah — 09:47
what department, cs?
Mk — 09:47
O can make out a red and brown label…
I got a bfa in computer o graphics ftom unass in 1990 furst class in the country we were told to get a degree in computer graphics from an art deot.
Noah — 09:49
awesome!!!
Mk — 09:50
Course my classes were in coins ( that’s what they called computer science) math, electrical engineering, had to take differential equations at smith college, and large scale welding to understand 3 dimensions
Noah — 09:51
have ya written some of your story down? should do! all three of us should 🙂
Mk — 09:52
How weird these git sent to me just as we were talking about old skool labs…
This one is a gem too. Lawd I was fabulous..
Image
Noah — 09:56
nice!!!
the mashup of art school and computers is really interesting topic - should def do something with that, history wise 🤔
Mk — 10:02
Copper Giloth made it happen. She’s got a show of her work in Paris right now.. so some histiry right there.
Noah — 10:03
cool - will google it! 👍
Mk — 10:03
Patric prince used to chair the siggraph traveling aet show and many artists just said “keep it” rather than pay to ship it home. So that’s another collection
And Jacki Morie just got a lifetime award from VES
She dud some of the earliest VR art stuff
Noah — 10:05
will google that too - i remember the name siggraph from pretty far back?
Mk — 10:05
Yep.
Guerilla galkery she did
Rogue artists!
Noah — 10:06
outside the outsider art 😄
Mk — 10:07
The digital rebels
Noah — 10:07
this is my old crew in austin - pretty non digital though! https://www.timkerr.net/home.htm
Mk — 10:09
My bfa dissertation was a kids book. Apple paint program… hand colored and bound
Noah — 10:09
gonna google me some art stuff today - nice!!! makes me happy😍
Mk — 10:09
Mfa was 3 6 foot high skate laser etched Celtic crosses
So dang heavy…
Celtic knot work
Disney let me use thier laser cutter as long as I documented how to use it
Noah — 10:12
sweet! want to hear about that disney story when time is right 🙂
Mk — 10:12
Righto

20250615

there ya go - flat out memory error
major bug in the code somewhere...🤔
PC is program counter register - total system crash 
the code that went on the tape in step3 has a bug for sure
Eric — 00:35
restarted fine, still seeing that collision stuff
Noah — 00:48
so simh is working ok? and in tops10 when you run decwar it crashes with memory error?🤔
if so, could go to a safe git commit
confirm decwar runs ok at that commit
then look for what went wrong in the following commits?🤔
Eric — 01:01
well i can play a bit bfore it crashes, the garbage output happens around collisions
just tried to chagne a line of code, and rebuild:

Step expired, PC: 705735 (POPJ 1,0)
sim>
Noah — 01:03
argh... simh trouble again...
Eric — 01:03
then rebooted
EXPECT "\r\n" send "decwar/seg:def\r"; continue
    EXPECT "\r\n" send "msg\r"; continue
    EXPECT "\r\n" send "warmac\r"; continue
    EXPECT "\r\n" send "sys:forlib/sea/seg:def\r"; continue
    EXPECT "\r\n" send "setup/seg:low\r"; continue
    EXPECT "\r\n" send "setmsg\r"; continue
    EXPECT "\r\n" send "sys:forlib/sea/seg:low\r"; continue
    EXPECT "\r\n" send "/g\r"; continue
    EXPECT "\r\n." send "get decwar\r"; continue
    EXPECT "\r\n." send "ssave\r"; continue
    EXPECT "\r\n." send "protect decwar.exe <055>\r"; continue
    EXPECT "\r\n." send "protect decwar.hlp <055>\r"; continue
    EXPECT "\r\n." send "protect decwar.nws <055>\r"; continue
    EXPECT "\r\n." send "protect decwar.grp <000>\r"; continue
    EXPECT "\r\n." send "protect decwar.ini <000>\r"; continue
    EXPECT "\r\n." send "k/f\r"; continue
    EXPECT "\r\n." send -t after=1000k "login 1,2\r"; continue
    EXPECT "\r\n." send "assign gam: dskb:[5,30]\r"; continue
    EXPECT "\r\n." send "k/f\r"; continue
BOOT V3(47)

BOOT>

Step expired, PC: 705617 (MOVEI 2,0(5))
Noah — 01:04
were fighting two separate battles
one with simh
other with decwar
Eric — 01:04
getting further
Noah — 01:05
for the decwar topic - wonder if my commit to drforbin/decwar will help - does seem possible!
Eric — 01:05
ok ay running agian
Noah — 01:06
you want to pull that commit asap🙂
Eric — 01:06
Command: M R -4 0

Command: $?
?Illegal UUO at user PC 000000

.
Noah — 01:07
memory error - decwar crash - shouldn't happen
have a sec for a call?
Eric — 01:09
Command: M R -1 4
?
?Illegal UUO at user PC 000000
Noah — 01:10
want to learn what your git situation is - if we can get you on a know good commit
Eric — 01:10
oh i've just been downloading straight
can do whatever
Noah — 01:13
wondering if you have this latest commit - if we can be in sync via git, we'd know for sure what code is running 🤔
definitely should not be seeing those memory error crashes - those are veeeery surprising🤔
Eric — 01:16
i just did a straight download from github, should be
Noah — 01:18
ok, hmmm. stumped... game is running fine here - six hours straight now...
hmmm....
just a sec, checking something...
ahha - possible idea!
Noah — 01:26
ok, just now pushed this commit to drforbin/decwar https://github.com/drforbin/decwar/commit/ca0070f4a4d24a7c3631d18a05c39542c046bfec
it has some little mods to simh scripts - nothing major
but it's at least remotely possible that one of those could help...🤔
Eric — 01:27
ok
Command: 
Command: 
Step expired, PC: 000001 (DATAO 774,@35034(14))
sim>
that is on current
not your new one
Noah — 01:27
ok, shouldn't be happening...:(
this is the new simh line that i wonder if it could help - it's possible...
expect "\r\n." send "del *.sta\r"; continue
you'll see it in the new commit
what that does is delete the on disk game state - that's what the .sta file is
i added that within the last week because have a suspicion that file can get corrupted
and that once it's corrupt, it can totally crash and ruin the game
just a suspicion / feel - but worth a try
it's at least remotely possible it's literally causing the crashes you're having...🤔
corrupt game state coming from that decwar.sta file...
Noah — 01:42
geez, getting hopeful actually... you can do it manually as well - on tops10 be logged in as decwar - then just do command 'del *.sta' - clear that old game state, right before starting the game - fresh new decwar 🙂 
bout a week ago, i might have been in the same kinda 'doom loop' your in right now - that's why i started deleting that state file...
if this cures your decwar - we'll have learned something big here...:)
Eric — 04:55
im> Resetting all devices...  This may not have been your intention.
The GO and CONTINUE commands do not reset devices.

Step expired, PC: 000000 (LUUO00 0,0(1))
sim> Resetting all devices...  This may not have been your intention.
The GO and CONTINUE commands do not reset devices.

Step expired, PC: 000000 (LUUO00 0,0(1))
sim> Resetting all devices...  This may not have been your intention.
The GO and CONTINUE commands do not reset devices.

Step expired, PC: 000000 (LUUO00 0,0(1))
sim> Resetting all devices...  This may not have been your intention.
The GO and CONTINUE commands do not reset devices.

Step expired, PC: 000000 (LUUO00 0,0(1))
sim>
everytime something different
Noah — 05:09
hmmm, so not getting booted into tops10 at all anymore? of the two probs (booting tops10, running decwar), seems like booting tops10 is the worse one? 🤔
Noah — 05:21
thinking out loud here - just brainstorming - and purely about prob1, booting tops20, not prob2 
so dec10blinken is a simh exe built on my raspi - could try the plain vanilla one called just 'dec10' there just to see if it does better, but it's not the real answer for us
well maybe it is, at least it can't conflict with pidp package - should be safe in that regard
but bigger pic is may need to move on to building dec10blinken locally, local build instead of my pre canned exes...
Noah — 05:28
will find the link for that this morning - it's not hard at all, just wanted to avoid it if possible:)
will need to create expanded instructions to help guide people who encounter this situation🤔
Eric — 05:31
oh i can get it to work, just take a couple times
Noah — 05:32
should start working on those this morning as well - really? that's good news then!
i was thinking was totally blocked kinda
need better instructions though for sure - things aren't as simple as i wanted and hoped - will start on those this morning, somewhere where you can edit and add...
is there some kinda cloud thing you'd go for? github or gitlab could both work... or even here in discord, am new to discord so not sure?
Noah — 05:39
am super serious about making project utexas package as friendly and usable as possible, as ya can see - it matters to me🙂
living time capsule like this is a work of art
Noah — 06:24
notes to self - three links that have to be the core of utexas user guide 
most essential - fundamental - https://github.com/rcornwell/sims
on top of previous, for the software side - https://sky-visions.com/dec/tops10.shtml
and for broader context, perspective surrounding utexas - https://github.com/obsolescence/pidp10
these three can be skeleton for expanded utexas user guide

20250629

---------- Forwarded message ---------
From: Harris Newman <harris.s.newman@gmail.com>
Date: Sat, Jun 28, 2025 at 8:52 PM
Subject: Re: history question
To: Noah Smith <noah@statespace.dev>
Cc: Eric Freeman <eric.freeman@austin.utexas.edu>


I looked on the Texas Scholarworks for the item I gave to UT in 2011, and now it only has 1 file and it's a license:
https://repositories.lib.utexas.edu/items/e0e0aa09-2dc3-49c5-a919-19210d7916d3

So I went back in time to my emails to Zach about it and found my submission, and although gmail won't easily let me download it, (file type no longer allowed to be sent), I was able to recover it.   I have uploaded it to the internet archive here: https://archive.org/details/decwar-2.3.tar and that should keep it for history.  

In that email I had Bob Hysick's response to Zach concerning decwar's release.  Here is his response:
"I'd be happy to have Decwar included in the Archive.  I would also be interested in obtaining a copy of the source – anything I had was lost in a purge years ago strongly encouraged by my wife.  (The bulk of the source was an assembler program.  The remainder was Fortran.  There was also a user’s guide, though I don’t recall its format.)
 
Your call made me curious, so I checked the web for Decwar references.  I found some interesting information in a Wikipedia Decwar entry.  That page and referenced pages included details I had forgotten or wasn’t aware of.  But they were short on development history and attribution to the authors.
 
The precursor to Decwar was a game written, I believe, by Jeff Potter and an author whose name I don’t recall (Robert something, perhaps).  It was a turn-based game that we played on teletypes (there’s some ancient history for you!).  The Web told me that game was called War, something I didn’t remember.
 
That was the late 70’s, the time when programming on campus was still largely done with punch cards.  It was the time of Adventure and Zork, the early text-based adventure games that were the inspiration for the likes of Leisure Suit Larry, King’s Quest, and ultimately games like Myst (in fact, I think I recall a Zork reference in Myst).
 
We wanted to take War to the next level: make it real time, improve the interface, increase the number of players, make a number of core game changes, and generally transform and improve game play.  And so, in our spare time between classes and work, we began our task (who needs sleep anyway?).  I worked for the Computation Center on the DEC-10, so I had access to the necessary resources, including a much-coveted 9600 baud CRT.  I took on the task of writing the core in assembler, while Jeff worked on the Fortran component.  Writing in assembler was necessary for much of the low-level access we required, and it allowed for optimizing both CPU and memory use (both were precious resources, especially in the  day when we actually used magnetic core memory).  Besides, back then assembler was the predominant system programming language, and language choices were limited, so it was a natural choice.
 
Over time we accomplished our  goal, producing a number of versions of Decwar.  We spent many late nights in the depths of space, exploring the galaxy and battling foes with futuristic weapons.  It wasn’t much by today’s standards, but back then (more than 30 years ago now!) it was quite an accomplishment."

-Harris

---------- Forwarded message ---------
From: Noah Smith <noah@statespace.dev>
Date: Sun, Jun 29, 2025 at 3:40 AM
Subject: Re: history question
To: <harris.s.newman@gmail.com>
Cc: Eric Freeman <eric.freeman@austin.utexas.edu>


harris, this is fantastic!!!:) thank you! comments directly from bob hysick - beautiful!:)

have to process this - it's a huge step forward!:) yes we definitely would like to establish contact with bob - we've been thinking that briscoe can help with that. any way we can do that will be great!

and thanks for that link harris - briscoe mentioned that they have three catalog items, and we knew about two - this is the third one! - here are all three together!

https://repositories.lib.utexas.edu/items/1aa48343-09ab-4b3b-a9f2-e2e525074a4d
https://repositories.lib.utexas.edu/items/e0e0aa09-2dc3-49c5-a919-19210d7916d3
https://repositories.lib.utexas.edu/items/7e2ccf50-e814-4bce-91d2-a7f6440eabe4

more soon - have to think for a moment!:) 
ciaociao
