
for the following mac10 code in warmac.mac

    ;;;	General constants used by DECWAR

        knplay==18		;maximum number of players (can't be increased)
        knloks==^d40		; maximum number of active locks (LOCK./UNLOk.)
        knstat==10		; number of statistic entries retained
        knbase==10		;initial number of bases on each side
        kgalv==75		;maximum Vertical coordinate in galaxy
        ksid==25		;# of words to hold compressed row of galaxy
        kgalh==75		;maximum Horizontal coordinate in galaxy
        brdsiz==1875		;board size (kgalv * kgalh / 3)
        knplnt==60		;maximum number of planets
    ;these two are not used at all? I wonder why drforbin
    ;	kmnpln==20		;minimum number of planets
    ;	kmxpln==80		;maximum number of planets
    ;---
        kndev==9		;number of devices
        kpass=="*mink"		;password for system (*) commands
        knmsg==32		;maximum number of messages in queue
        msglen==17		;max # of words per msg (header + 80 chars)

here's what you see after a fresh build and entering the game with ten robots and yourself in nimitz
    
    > *password *mink
    
    > list all
    
    E  @ 6-60 -63, +9   +16.4%
    F  @ 7- 9 -62,-42   +99.5%
    I  @11-11 -58,-40   +99.1%
    L  @45-21 -24,-30  +100.0%
    N  @26-75 -43,+24   +96.8%
    V  @69-51   0,  0  +100.0%
    *B  @ 7-63 -62,+12   +55.0%
    *C  @56-68 -13,+17   +32.1%
    *D  @52-42 -17, -9   +98.5%
    *G  @59-61 -10,+10  +100.0%
    *H  @54-58 -15, +7  +100.0%
    
    <> @ 8-16 -61,-35   100.0%
    <> @60-68  -9,+17   100.0%
    <> @74-15  +5,-36   100.0%
    <> @62-34  -7,-17   100.0%
    <> @35-14 -34,-37   100.0%
    <> @50-72 -19,+21   100.0%
    <> @45-69 -24,+18   100.0%
    <> @60-44  -9, -7   100.0%
    <> @49-24 -20,-27   100.0%
    <> @37- 4 -32,-47   100.0%
    *)( @34-32 -35,-19   100.0%
    *)( @32-27 -37,-24   100.0%
    *)( @ 2-53 -67, +2   100.0%
    *)( @60-48  -9, -3   100.0%
    *)( @22-66 -47,+15   100.0%
    *)( @22-58 -47, +7   100.0%
    *)( @11-50 -58, -1   100.0%
    *)( @30-68 -39,+17   100.0%
    *)( @ 1-46 -68, -5   100.0%
    *)( @27-12 -42,-39   100.0%
      
    @ @ 6-55 -63, +4
    @ @14-35 -55,-16
    @ @59-23 -10,-28
    @ @49-21 -20,-30
    @ @11-52 -58, +1
    @ @ 9-56 -60, +5
    @ @26- 5 -43,-46
    @ @41-15 -28,-36
    @ @25-26 -44,-25
    @ @51-45 -18, -6
    @ @19-22 -50,-29
    @ @ 6-50 -63, -1
    @ @66-17  -3,-34
    @ @23-42 -46, -9
    @ @27-38 -42,-13
    @ @40-15 -29,-36
    @ @64- 5  -5,-46
    @ @52-72 -17,+21
    @ @69-64   0,+13
    @ @57-12 -12,-39
    @ @39-30 -30,-21
    @ @66-56  -3, +5
    @ @31-20 -38,-31
    @ @16-20 -53,-31
    @ @26-73 -43,+22
    @ @10-50 -59, -1
    @ @51-51 -18,  0
    @ @14- 5 -55,-46
    @ @44- 9 -25,-42
    @ @70-48  +1, -3
    @ @45-34 -24,-17
    @ @ 9-22 -60,-29
    @ @53-29 -16,-22
    @ @ 9-75 -60,+24
    @ @48-67 -21,+16
    @ @66-37  -3,-14
    @ @73-38  +4,-13
    @ @42-53 -27, +2
    @ @ 4-72 -65,+21
    @ @25-59 -44, +8
    @ @33-30 -36,-21
    @ @10- 6 -59,-45
    @ @52-28 -17,-23
    @ @70-24  +1,-27
    @ @28-32 -41,-19
    @ @21-34 -48,-17
    @ @48-51 -21,  0
    @ @71-18  +2,-33
    @ @48-38 -21,-13
    @ @21-59 -48, +8
    @ @40-47 -29, -4
    @ @63-35  -6,-16
    @ @52-29 -17,-22
    @ @43-30 -26,-21
    @ @35-56 -34, +5
    @ @65-71  -4,+20
    @ @31- 1 -38,-50
    @ @ 4-48 -65, -3
    @ @ 6-57 -63, +6
    @ @ 7-46 -62, -5z
    