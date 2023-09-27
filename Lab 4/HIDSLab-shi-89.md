## Host Intrusion Detection System Lab

### Error Code ID 3005
Error Description: 
The option PermitEmptyPasswords should be set to no

Steps Taken: 
1. I ran the following command `sudo vim /etc/ssh/sshd_config` to access the configuation file.
2. Hovered over to the `# PermitEmptyPasswords yes`, and un-commented out the line, and updated it to `# PermitEmptyPasswords no`.
3. Saved and exited the configuation file using `:wq`.
4. I used the command `sudo systemctl restart ssh` to restart the host connection.  
5. `sudo service wazuh-agent restart` to refresh the error status. Confirmed it is now resolved for Error 3005.

![](img/Error3005Fixed.JPG)
    Updated to PermitEmptyPasswords yes

----

### Error Code ID 3002
Steps Taken: 
1. I ran the following command `sudo vim /etc/ssh/sshd_config` to access the configuation file.
2. I located the `#PermitRootLogin yes ` line and un-commented out the line, and updated it to `PermitRootLogin no `.
3. Saved and exited the configuation file using `:wq`.
4. I used the command `sudo systemctl restart ssh` to restart the host connection.
5. `sudo service wazuh-agent restart` to refresh the error status. Confirmed it is now resolved for Error 3002.

![](img/Error3002Fixed.JPG)
    Updated from from commented PermitRootLogin yes to PermitRootLogin no

----

### Error Code ID 3004
Steps Taken: 
1. I ran the following command `sudo vim /etc/ssh/sshd_config` to access the configuation file.
2.  I located the `#PasswordAuthentication yes` line and un-commented out the line, and updated it to  
`PasswordAuthentication no`.
3. Saved and exited the configuation file using `:wq`.
4. I used the command `sudo systemctl restart ssh` to restart the host connection.
5. `sudo service wazuh-agent restart` to refresh the error status. Confirmed it is now resolved for Error 3004.

![](img/Error3004Fixed.JPG)
    Updated from from commented PasswordAuthentication yes to PasswordAuthentication no


----

![](img/Wuzuh-Passed-All-3.JPG)
    Error 3005, 3002, 3004 are now Passed instead of Failed. 
