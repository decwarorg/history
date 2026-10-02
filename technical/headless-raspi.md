# hello world for headless raspi

this works but blinky seems to lockup the ssh session. open another ssh to kill -9 it.

    noah@dec10:~$ git clone https://github.com/obsolescence/pidp10.git
    noah@dec10:~$ pidp10/bin/pdp10-kl pidp10/systems/hills-blinky/boot.pidp 
    pidp10/bin/pdp10-kl: error while loading shared libraries: libvdeplug.so.2: cannot open shared object file: No such file or directory
    noah@dec10:~$ sudo apt install libvdeplug-dev
    noah@dec10:~$ pidp10/bin/pdp10-kl pidp10/systems/hills-blinky/boot.pidp 

# getting utexas ready

    git clone https://github.com/decwarorg/utexas.git
    cd utexas
    unzip docker/dsk-20251103.zip && mv dsk-20251103 docker/dsk
    cp -r docker/bts .
    cp -r docker/dsk .
    cd msc
    gcc back10.c -o back10
    cd ..
    cp msc/back10 .
    python3 msc/tape.py --simple
    ../pidp10/bin/pdp10-kl simh/boot-from-disk.ini
    
# from laptop
    
    telnet dec10.local 2030
