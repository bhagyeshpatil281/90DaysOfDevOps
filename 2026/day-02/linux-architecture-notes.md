# the core components of linux :
 - KERNAL : the linux kernal is the core foundation of the operating system It runs a priviledged mode kernal mode With direct full of access to hardware 

example : process scheduler,memory Mangement,Device

- USERSPACE : userspace is the isolated memory region where regular user application shell and system utilities run with restricted permission 

example : Application,system libraries, shell GUIS 

- INIT system / systemd : the init system is the very first user-space program started by the kernal during boot assigned process ID 1 (PID 1) modern linux distribution use systemd as this 

example : system initilization , service management , process supervision 

# How process are created and managed 
- running : actively executing instruction on a cpu core
- sleeping : waiting for a resources or an event (like user input)
- stopped : paused by a user or system signal
- Zoombie : the process has finished executing (exit) but its entry remain in the process table until the parent read                its exits
  # systemd does and why its matter
  system d is a system and service manager for modern linux operating system It intialization the system manage service and control system resources during startup and runtime
  initialize the system during boot
  manage and control system service
  replace the traditional sysv init system
  improve boot speed and performance

  # list 5 commands
  - echo print content
  - chmod : change file permission
  - systemctl : control system
  - df/h : disk space
  - free -h : memory space

    # cheet code
    Kernal : linux ka main / core part hai
           :  hardware aur software ke beech communicaion karata hai
           :  cpu,RAM, disk,network jaise resources manage karata
 
    userpace : jahan user aur application run karata hai
             :command like ps systemctl , ssh etc userspace mein directly hardware ko access nahi karata
             : kernal ke through kaam

    init/systemd : systemd boot ke baad sabase important first process hota hai service aur process ko start                             /stop/manage karata hai 
    USERSPACE : 
