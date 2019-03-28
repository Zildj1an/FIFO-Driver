# FIFO-Char-Driver [![GPL Licence](https://badges.frapsoft.com/os/gpl/gpl.png?v=103)](https://opensource.org/licenses/GPL-3.0/)

<span>Language:</span> 
  <a href="https://github.com/Zildj1an/FIFO-Driver/blob/master/LEEME.md">Español</a> |
  <a href="https://github.com/Zildj1an/FIFO-Driver">English</a> 

## Main Idea
👨‍🔧 Character device driver (/dev) working as a FIFO pipe, created with a Linux Kernel module.
As such, it's SMP-Safe due to the use of semaphores (working as condition variable and mutexes).

Usage: Compile, load the module, create the driver (mknod), use the pipe!


    $ make

    $ sudo insmod fifodev.ko

    $ sudo mknod -m 666 <pathname_char_file> c <major> <minor>
    
    $ # Enjoy your brand-new pipe! #

    ...

## Loading module in Android's Kernel

The module was developed for Debian, but the can be easily used in Android.
You just need to use the <a href="https://github.com/Zildj1an/FIFO-Driver/blob/master/Makefile_Android">Makefile</a> for re-compiling. Please notice that the Makefile employs a compiled Android-x86 kernel <a href= "https://www.android.com/versions/oreo-8-0/"> oreo version </a>


## License
This project is licensed under the GNU-GPL License - see the <a href="https://github.com/Zildj1an/FIFO-Driver/blob/master/LICENSE">LICENSE.md</a> file for details
