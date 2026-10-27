# today goal is to practice user and group management by completing hand-on challange 

# challange task 
 
 * create three user with home directories and password 
   
    command :- `sudo adduser tokyo`
            :- ` sudo adduser berlin`
    
    verify  :- `cat/etc/passwd`
    
    check it :- `/home dirctories`

*  create group 
  
    command :- `sudo groupadd developers`
            :- `sudo groupadd admin`

     verify :- `cat/etc/group`

     check it  its true

*  Assign to group 

    command :- ` sudo gpasswd -aG tokiyo developers`
            :- ` sudo gpasswd -aG developers,admin berlin`

     verify :- `cat/etc/group`

*  shared directory 

     command :-  `sudo mkdir /opt/dev-project`
             :- `sudo chgrp developers dev.txt`
             :- `sudo chmod 775 dev.txt`

       verify :- `sudo su tokiyo`
                 ` echo "iam tokiyo" > file.txt`

                   `sudo su berlin`
                   `echo "i am berlin` > demo.txt`

* team workspace 

     command  :- `sudo adduser nairobi`
                 `sudo groupadd project-team`
                 ` sudo usermod -aG nairobi project-team`
                 ` sudo usermod -aG tokiyo project-team `

    create dirctory :- `sudo mkdir /opt/team-workspace` 



    set permission :-  `sudo chgrp project-team team-workspace`
                       `sudo chmod 775 team-workspace`

     Test the user :- `sudo su nairobi`
                       `echo "i am nairobi " > test.txt`
                       
                     

