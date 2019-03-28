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


## License
This project is licensed under the GNU-GPL License - see the <a href="https://github.com/Zildj1an/FIFO-Driver/blob/master/LICENSE">LICENSE.md</a> file for details
