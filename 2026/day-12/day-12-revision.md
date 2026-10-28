# what a review

* mindset & plan :-
yes my goal still right and note walks i am write direction to suddenly before 10 days are consistance & hardwork (actually I am thoda mehnat main jor kam lag raha hai)

* process & service :- 
-
 command :- `ps -aux`  :- running process High process high process high cpu low cpu grind service 

 command :- `systemctl status` :- actual service start,stop,status,booting reboot ,running ,sleeping

 command :- `journalctl -u` :- are servicelog are generated access error log are journally are  
 
                                  

* file skill :-

  
   command :-     mkdir /tmp/file-practice 
                  cp /etc/hosts /tmp/file-practice/hosts-copy
                ls-l tmp/file-practice

    command :- echo "file skills practice completed ">> /tmp/file-practice/notes.txt
               cat /tmp/file-practice/notes.txt

    command :- sudo chmod 600 /tmp/file-practice/notes.txt
               ls-l /tmp/file-practice/notes.txt

  * cheetsheet refresh :- 
  
     `ps aux`
     `pidof`
     `kill` 
     `systemctl status`  :- start,stop,active failed or restarting 
     
     `cat/var/log/nginx/error.log` :- read the log for web server error

     `free-h ` :-display memory is ages in mb to check for execution 
     
     `df-h` :- Disk free 

    1  Which 3 commands save you the most time right now, and why?
      
      `ls -l` -use it to quickly checkfiles , permission ,owner and group 
      `ps -aux` use it to see running process and identify resources usage 
      `systemctl status` i use is to quickly check whether a service is running or failed 
    
    2  How do you check if a service is healthy? List the exact 2–3 commands you’d run first.

     `systemctl is status (service)`
        `systemctl is-active (service)`
     `jornalctl -u (service) --no-pager -n 20`
     
     these command shown that service status whether it is active and recent logs for troubleshooting 

    3 How do you safely change ownership and permissions without breaking access? Give one example  command.

      i first check the current ownership and permission using ls -l then make the smallest required change 
      
      command  :- `chown professor:planner project -config-yaml`

      next three days focous 

      i will focous on improving next concept for linus shell scripting practice (Hands-on) are 
       consistency key of sucess


     

    