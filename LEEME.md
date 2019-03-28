## Idea principal (Español)
👨‍🔧 Driver de caracteres (/dev) funcionando como una tubería FIFO, creado usando un módulo del Kernel Linux.
Como tal, es SMP-Safe gracias al uso de semáforos (trabajando como variables-condicón y cerrojos). Para usarlo
primero hay que compilar, cargar el módulo y crear el driver (mknod), tal y como se especifica abajo.




    $ make

    $ sudo insmod fifodev.ko

    $ sudo mknod -m 666 <pathname_char_file> c <major> <minor>
    
    $ # Enjoy your brand-new pipe! #

    ...


## Licencia
Este proyecto tiene la licencia GNU-GPL- ver el archivo <a href="https://github.com/Zildj1an/FIFO-Driver/blob/master/LICENSE">LICENSE.md</a>  para más detalles.

