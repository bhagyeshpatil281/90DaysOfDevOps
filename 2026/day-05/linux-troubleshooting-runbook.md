# RUNBOOK for ssh service

### This runbook provides quick troubleshooting steps if the SSH service goes down.

## Environment basics

* Command : `uname -a`

  Output : `Linux afroz 6.14.0-37-generic #37~24.04.1-Ubuntu SMP PREEMPT_DYNAMIC Thu Nov 20 10:25:38 UTC 2 x86_64 x86_64 x86_64 GNU/Linux`

  Observation : Kernel version and architecture confirmed.

* command : `cat /etc/os-release`

   output : `PRETTY_NAME="Ubuntu 26.04.1 LTS"`

   `NAME="Ubuntu"`
      
    `VERSION_ID="26.04"`
      
    `VERSION="26.04.1 LTS (Resolute Raccoon)"`
    
    `VERSION_CODENAME=resolute`
                       
    `ID=ubuntu`

    observation : this command is distribution version os name identify

## file system sanity

* command : `mkdir /tmp/runbook-demo`
  
* command : `cp /etc/hosts/tmp/runbook-demo/hosts-copy`

* command : `ls -l /tmp/runbook-demo`

    observation : create the file system sanity & usecase is 
                  filesystem/file operations properly work   in the case

## cpu/memory 

 * command : `top`

    output : live process in your system

 * command : `ps -o pid,pcpu,pmem,comm -p$ (pidof sshd)`
    
    output :         `PID %CPU %MEM COMMAND`
                    `1681  0.0  0.1 sshd`

 *  command : `free-h`
    
      output : `total        used        free`     
                     `Mem:           7.1Gi       3.2Gi       1.6Gi `
 
    observation : that scenario your process high point of consume cpu ,mem ,disk this process you find from this command and stop this process

##  Disk-space

  * command : `df-h` 
  
       output :   `/dev/sda2 233G   26G  196G  12% /`

  * command : ` iostat`nahi
     
       output : `avg-cpu:  %user   %nice %system %iowait  %steal   %idle`
            
    `10.76    0.04    4.06    0.13    0.00   85.02`

     observation :   your system is free disk is sufficient and iostat  is    realcpu and df -h performance check karana 

## network 

   * command : `ss-tulpan | grep 22`

   * command : `nc -zv localhost 22`

   observation : your system port no running in your server 
                 and next command is check your port no specific available hai ya nahi

## logs 

  * command : `journalctl -u n 50`

  * command : `tail -n 50 /var/log/Auth.log`
    
    output : ssh logging authentic and error logs are available

# worsence 

 if the system high cpu drill the in case of small troubleshooting in this scenario based assignment small troubleshooring for this case
 



        