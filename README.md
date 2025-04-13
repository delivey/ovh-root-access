# ovh-root-access
How to gain root access on an OVH server

Ubuntu 22.04 used in this example. Original method: https://github.com/2M4U/OVHRootAccess

1. `sudo vim /etc/ssh/sshd_config`
2. `/Permit` to find `#PermitRootLogin`, change it to `PermitRootLogin yes` (don't forget to remove the #)
3. `sudo passwd ubuntu`, change it to whatever password you want
4. `sudo service sshd restart`, and enter the password you chose in step 4
5. `sudo passwd root`, change it to whatever password you want
6. `su root`, enter the password from step 5
7. `vim ~/.ssh/authorized_keys`
8. `d/ssh` to delete the rules not allowing root ssh
9. `ssh root@your_server` should now work, enjoy!
