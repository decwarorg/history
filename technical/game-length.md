
# newer

let's try to read this part of warmac.mac while avoiding any form of abstraction. let's think only of concrete <>, )(, @ symbols that can been seen using scan command. at game startup. the initial galaxy / game board. my reading is 

<> ten can be seen using scan command

)( ten can be seen using scan command

@ between twenty and eighty can be seen using scan command. here we've tuned that control knob to twenty.

    ;;;	General constants used by DECWAR

        knplay==18		;maximum number of players (can't be increased)
        knloks==^d40		; maximum number of active locks (LOCK./UNLOk.)
        knstat==10		; number of statistic entries retained
        knbase==10		;initial number of bases on each side
        kgalv==75		;maximum Vertical coordinate in galaxy
        ksid==25		;# of words to hold compressed row of galaxy
        kgalh==75		;maximum Horizontal coordinate in galaxy
        brdsiz==1875		;board size (kgalv * kgalh / 3)
        knplnt==20		;maximum number of planets
    ;these two are not used at all? I wonder why drforbin
    ;	kmnpln==20		;minimum number of planets
    ;	kmxpln==80		;maximum number of planets
    ;---
        kndev==9		;number of devices
        kpass=="*mink"		;password for system (*) commands
        knmsg==32		;maximum number of messages in queue
        msglen==17		;max # of words per msg (header + 80 chars)

here's immediately after fresh build and game startup up with above code
    
    > *password *mink
    
    > list
    
     N  @ 5-71   0,  0  +100.0%
    
     <> @64- 1 +59,-70   100.0%
     <> @61-64 +56, -7   100.0%
     <> @69-68 +64, -3   100.0%
     <> @65-67 +60, -4   100.0%
     <> @26-41 +21,-30   100.0%
     <> @62-43 +57,-28   100.0%
     <> @44-22 +39,-49   100.0%
     <> @24-32 +19,-39   100.0%
     <> @37- 7 +32,-64   100.0%
     <> @60-46 +55,-25   100.0%
    *)( @28-19 +23,-52   100.0%
    *)( @24- 2 +19,-69   100.0%
    *)( @57-52 +52,-19   100.0%
    *)( @44-56 +39,-15   100.0%
    *)( @36- 9 +31,-62   100.0%
    *)( @ 9-25  +4,-46   100.0%
    *)( @13-22  +8,-49   100.0%
    *)( @56-10 +51,-61   100.0%
    *)( @38-57 +33,-14   100.0%
    *)( @70-52 +65,-19   100.0%
    
      @ @39-23 +34,-48
      @ @38-65 +33, -6
      @ @ 9-51  +4,-20
      @ @38-13 +33,-58
      @ @23-50 +18,-21
      @ @62-57 +57,-14
      @ @25-28 +20,-43
      @ @71-40 +66,-31
      @ @53-40 +48,-31
      @ @55-75 +50, +4
      @ @ 7- 4  +2,-67
      @ @36- 7 +31,-64
      @ @43-34 +38,-37
      @ @20-70 +15, -1
      @ @32- 4 +27,-67
      @ @58-62 +53, -9
      @ @56-43 +51,-28
      @ @ 6-23  +1,-48
      @ @16-25 +11,-46
      @ @65-66 +60, -5
    
    > 


# older

having a thought this morning - major factors controlling game length?

- shortest games - victory when enemy has no bases - likely very ahistoric
- short, and adjustable - decrease the number of planets! could also very well be what was happening in san marcos 

as have mentioned, memory is that basically only cared about planets when number of bases got low - then there was a rush to capture and build planets to get number of bases back up (to ten ideally). with fewer planets, would 'run out' earlier and eventually not be able to build bases - then the end would come quickly

hmmm, can think about switching to that in utexas - uncomment that line - then tune the number of planets to get appropriate game length - ahha! robots will have to be capturing and building appropriately! have to add a bit more brains to the robots, then could do.

and keep in mind - was fifteen - probly was not catching some of the strategic considerations that serious players understood 

just a curiosity here in warmac - min number of planets? guessing kmnpln and kmxplan were associated with some kinda compuserve stuff at some point? hmmm, maybe number of planets was variable at startup to control game length? 20 planets for short game, 80 planets for long game.