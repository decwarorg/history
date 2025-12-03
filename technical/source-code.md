# source code

we build and run the source code.
for fortran compiler we use tapes/BB-D480C-SB_FORTRAN10_V6.tap

we have one set of source code files.

we don't have any source code other than the mystery 1995 email with the compuserve code, which started as a utexas 2.3 tape sent from austin to compuserve.

we have the help file from 2.2, that's true. but no source code to go with that. current pic is there's one set of source files - they came from compuserve - started as a utexas2.3 tape, were sent from austin to compuserve - modified there. then on top of that we have confusion in the comments in that code - and the fact that we do have two help files, both a 2.2 help file and a 2.3 help file. nutshell - all the source code we have came from compuserve in that mystery 1995 email to harris.

# important files

as part of cleanup 'post project push button' - collected current understandings of 'primodial tape'. that's all a nutshell readme now - https://gitlab.com/decwar/utexas/-/tree/main/staging

can note we're the very first people known to have paid much attention to the five files discussed here - have always asked and heard only noise on this topic - actually, this topic is really one of the things that fully kicked off 'project utexas' 

one of the fascinating things in this whole topic is that teco enters the picture - direct connection back to early 60s and pdp1 - could explore that topic in the book as well - teco is discussed in depth in the steve levy hackers book for instance - actually running the decwar teco code is probly a bridge too far - but it's there and understood at the least 

# the decus tape exe file

what could cause some confusion is that we also have a modified 2.2 exe. a binary, not source code. it's a crazy thing that was modified to run on a KA. it crashes. it was grabbed off a decus tape long ago. it's kinda like getting the cracked version of a game that worked on one guys machine thirty years ago. it's kinda useless today unfortunately.

if we could get that 2.2 exe to run reliably. it would be great. occasionally people get confused into trying that. we probably should help people avoid spending too much time on that if it's a wild goose chase. there have already been efforts to decompile that weird 2.2 exe in an effort to debug it, and those were given up? if we could reliably run that 2.2 exe it would be awesome, since it's probably a pure utexas build. the source code was probably directly from a utexas 2.2 tape. but they modified it to run on their KA. in particular, they introduced some local opcodes in the mac10 that were specific to their KA. yep that was common back then. site specific custom opcodes. kinda hopeless to reverse engineer those.

20251102 note from merlyn - That binary does represent the TRUE UT example of the game. I.e. it having 9 ships per side and all the timer code. I re-implemented the timer code. Which is to say, when you were killed or exited the game it would start a timer so you could not JUST reenter the game. This code was commented out on CIS version.
