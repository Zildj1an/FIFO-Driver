# FIFO-Char-Driver
[![GPL Licence](https://badges.frapsoft.com/os/gpl/gpl.png?v=103)](https://opensource.org/licenses/GPL-3.0/)

## Main Idea (English)
👨‍🔧 Character device driver (/dev) working as a FIFO pipe, created with a Linux Kernel module.
As such, it's SMP-Safe due to the use of semaphores (working as condition variable and mutexes).

Usage: Compile, load the module, create the driver (mknod), use the pipe!


    $ make

    $ sudo insmod fifodev.ko

    $ sudo mknod -m 666 <pathname_char_file> c <major> <minor>
    
    $ # Enjoy your brand-new pipe! #

    ...

## Idea principal (Español)
Driver de caracteres (/dev) funcionando como una tubería FIFO, creado usando un módulo del Kernel Linux.
Como tal, es SMP-Safe gracias al uso de semáforos (trabajando como variables-condicón y cerrojos). Para usarlo primero hay que compilar, cargar el módulo y crear el driver (mknod), tal y como se especifica arriba.
