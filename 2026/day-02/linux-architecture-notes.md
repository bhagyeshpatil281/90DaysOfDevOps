# Linux Architecture ,process and systemd 

# today goal is to understand how linux work underthehood 

  # the core components of linux (kernal,user-space init)
   
   * the core component of linux 

    kernal :- the linux kernal is the core foundation of the operating system it runs a priviledged mode of Kernal mode with direct full access to hardware 
    EX. process scheduler, memory management,Device

    user space :- userspace is the isolated memory region where regular user application,shell and system utilities run with restricted permission 
    EX . Application , system libraries, shell and GUIs

    init system/systemd :- the init system is the very first user-space program started by the kernal during boot assigned process ID 1 modern linux distribution use systemd as this 

    * 