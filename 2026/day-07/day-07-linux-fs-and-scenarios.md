# linux file system hierarchy & scenario Based practice

## goal to uderstand where thing live in linux and practice troubleshooting like a devops engineer

# lets understand where thing live on linux

* core directories

- / root :- this is a specific ,private folder located inside the system root (/) that server at the personal home directory for the administrator account also known as root user or superuser

- / home :- in linux acts as the personal workspace for all non administrator user on the system . its isolate personal files and application setting from the core operating system .

- / etc :- configuration file contain system wide configuration file these file control the configuration of service , users,networking and other system setting 

- /var/log :- contain system ,service ,and application log file these logs helps us understand error event and system activity

- /tmp :- contain temporary files created by application and user these files are usually needed only for a short period of time 

* Additional Directories (Good to known)

- /bin :- contain essential command -line program required for basic system operation these commad are available to users for every day linux tasks

 i would use /bin when need to access essential linux command used for basic system operaton

/opt :- contain optional or third -party software and application installed on the linux system 

 i would use this when 
   i would use /opt when i need to install or manage optional third- party software 

   # part 2 scenario- Based practice 
   
* Question: How do you check if the 'nginx' service is running?
   
   output :- `systemctl status nginx `

   Why this command? It shows if the service is active, failed, or stopped


* question : If service is not found, list all services

    output :- `systemctl list-units --type=service`

* question :    Check if service is enabled on boot

    output :- `systemctl is-enabled nginx`

    # Scenario 2 service is not starting

    A web application service called 'myapp' failed to start after a server reboot.
What commands would you run to diagnose the issue?
Write at least 4 commands in order.

  * command  :- `systemctl status myapp`
      why :- it shown service is active ,running,sleeping, stopped failed 

  * commad :- `journalctl -u n 50`
      why :- it shown the log by command Auth.logging failing starting

  * command :- `systemctl enabled myapp`
      why :- It shown properly system activated by booting process atomatically started the service 

  # scenario 3 High cpu usages

      Your manager reports that the application server is slow.
       You SSH into the server. What commands would you run to identify
        which process is using high CPU?

  * command :- `top` liveprocess
     why :-this command live track your service/process cpu ,memory

  * command :- `ps -aux --sort =% cpu |head -10 `
    why :- this command process ID to sort high level cpu usages sort the process ID services 

  * command :- `ps -p (pid) -f`
    why :- this command process for more details of the process ID and sort the process Id 
   
  * command :- `kill the (pid)`
    why :- your server high cpu consumption the into kill the process

  # scenario 4 finding service log

         A developer asks: "Where are the logs for the 'docker' service?"
            The service is managed by systemd.
                  What commands would you use? 

  * command :- `systemctl status ssh`
     why :- check the service is start stop running 

  * command :- `journalctl -u ssh -n 50 `
     why :- check the logs are service to start & failed system 

  * command :- `journalctl -u ssh -f `
     why :- A flags to follow logs in real-time (like tail-l)

  # scenario 5 file permission issues

  A script at /home/user/backup.sh is not executing.
When you run it: ./backup.sh
You get: "Permission denied"

  * command :- `ls -l demo.sh`
    why :- check current permission of file look for (read write excute permission)

  * command :- `chmod 764 demo.sh`
    why :- this command help us file ki user ko rwx permission mili hai

  * command :- `./demo.sh`
    why :- run this script  and run it
