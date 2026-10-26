# Linux Architecture ,process and systemd 

# today goal is to understand how linux work underthehood 

  # the core components of linux (kernal,user-space init)
   
   * the core component of linux 

      kernal :- the linux kernal is the core foundation of the operating system it runs a priviledged mode of Kernal mode with direct full access to hardware linux-architecture-notes.md

      EX. process scheduler, memory management,Device

      user space :- userspace is the isolated memory region where regular user application,shell and system utilities run with restricted permission 
      EX . Application , system libraries, shell and GUIs

      init system/systemd :- the init system is the very first user-space program started by the kernal during boot assigned process ID 1 modern linux distribution use systemd as this 

  * how process are created and managed
linux-architecture-notes.mdlinux-architecture-notes.md


      running :- actively executing instruction on a cpu core 
      sleeping :- waiting for a resources or an event (like user input)
      stopped :- paused by a user or system signal 
      zoombie :- the process has finished executing (exit) but its entry   

  *  what systemd does and why it matter 

     systemd is a system and service manager for modern linux operating system It initialzes the system manage service and control system resources during startup and runtime 

     - intialize the system during boot
     - manage and control system service 
     - replace the traditional sysv init system 
     - Improve boot speed and performance

  *  List 5 command 

     echo :- print content 

     chmod :- change the file permission

     systemctl :- control system

     df/h :- disk space
      
     free -h :- memory space 
