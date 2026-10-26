# Real time output of commands I practiced

## Process commands
* `ps -aux | head -n 10` - List running processes(top 10 lines).
![snapshot](images/ps-aux.png)
* `pgrep -x sshd` - Get the process id by process name.

![snapshot](images/pgrep.png)

## Service commands
* `systemctl status | head -n 20` - Prints first 20 lines of system service status summary.
![snapshot](images/system.png)
 `systemctl list-units --type=service --state=running | head` - Prints first 10 lines of running services status.
![snapshot](images/system-listunit.png)
## Log commands
* `journalctl -u ssh` - Displays logs for the SSH service.
![snapshot](images/journal.png)
* `tail -n 40 /var/log/auth.log` - Last 40 lines of the authentication log(ssh, sudo).
![snapshot](images/tail.png)


