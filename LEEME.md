## Idea principal (Español)
👨‍🔧 Driver de caracteres (/dev) funcionando como una tubería FIFO, creado usando un módulo del Kernel Linux.
Como tal, es SMP-Safe gracias al uso de semáforos (trabajando como variables-condicón y cerrojos). Para usarlo
primero hay que compilar, cargar el módulo y crear el driver (mknod), tal y como se especifica abajo.




    $ make

    $ sudo insmod fifodev.ko

    $ sudo mknod -m 666 <pathname_char_file> c <major> <minor>
    
    $ # Enjoy your brand-new pipe! #

    ...


## Cargado del módulo en Android
Éste módulo fue desarrollado para Debian, pero puede usarse facilmente en Android.
Simplemente usa <a href="https://github.com/Zildj1an/FIFO-Driver/blob/master/Makefile_Android">Makefile</a> para recompilar.
Ojo: Ese Makefile usa un kernel Android x-86 <a href= "https://www.android.com/versions/oreo-8-0/"> versión oreo</a> compilado.


## Licencia
Este proyecto tiene la licencia GNU-GPL- ver el archivo <a href="https://github.com/Zildj1an/FIFO-Driver/blob/master/LICENSE">LICENSE.md</a>  para más detalles.

