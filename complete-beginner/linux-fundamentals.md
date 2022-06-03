# Linux Fundamentals

## Process

Les signaux pour arrêter un processus:

> SIGTERM - Kill the process, but allow it to do some cleanup tasks beforehand
> SIGKILL - Kill the process - doesn't do any cleanup after the fact
> SIGSTOP - Stop/suspend a process

Les process sont des childs de `systemd`

### Boot

`systemctl`: permet d'intéragir avec le process/deamon `systemd`

#### Options
`start`: démarre un service
`stop`: arrête un service
`enable`: active un service au boot
`disable`: retire un service du boot

### Foreground & Background

`Ctrl + Z`: met en pause un process
`fg`: reprend l'exécution d'un process interrompu
