## Idea principal (Español)
👨‍🔧 Driver de caracteres (/dev) funcionando como una tubería FIFO, creado usando un módulo del Kernel Linux.
Como tal, es SMP-Safe gracias al uso de semáforos (trabajando como variables-condicón y cerrojos). Para usarlo
primero hay que compilar, cargar el módulo y crear el driver (mknod), tal y como se especifica arriba.
