

# cust.cmd
    CISREV.DAT/SKIP:1   
    B.AN 
    Y    
    DIF:CUST.DIF   
    NLT  
    KB   
    SX   
    SY   
    HX   
    KT
    IA:X,1.5
    IA:Y,1.5
    LOC:D,2.25,1.5,7,4
    2/BLU
    \TR\CompuServe\CR\ Information Service
    VALID CUSTOMERS
    FISCAL '82
    CUSTOMERS 
    2    
    CUSTOMERS/BLU
    0,30000,5000   
    1    
    1    

# cxrf.icd
    limit sru 0
    compile/x/c lofchk,warmac,cishng
    compile/s/c msg,setmsg
    compile/s/c (nowarn)/f10 setup,@decwar,low,high
    r link
    @l
    r link
    @ldeb
    ^C
    $cref dsk:=
    printnh *.lst
    ;--printnh /r *.lst
    ;--Bill Louden
    ;--Building Four
    ;--First Floor
    ;--===============
    ;--* D E C W A R *
    ;--

# netrev.cmd
    CISREV.DAT/SKIP:1   
    B.AN 
    Y    
    DIF:NETREV.DIF 
    NLT  
    KB   
    SX   
    SY   
    HX
    kt
    ia:x,1.5
    ia:y,1.5
    loc:d,2.25,1.5,7,4
    2/BLU
    \tr\CompuServe\cr\ Information Service
    REVENUE NET OF CREDITS
    FISCAL '82
    REVENUE   
    1
    REVENUE NET OF CREDITS/GRN
    1    
    1    



