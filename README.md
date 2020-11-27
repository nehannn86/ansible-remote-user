# ansible-remote-user

#Set Host Key checking to False in your ansible.cfg file 
          host_key_checking=False

#If your Host machine is not having Password then set password using following command. 
          sudo passwd ec2-user
  
#Edit /etc/ssh/sshd_configsudo file and enable:

1. Find the Line containing 'PasswordAuthentication' parameter and change its value from 'no' to 'yes'
          PasswordAuthentication yes

2. If you want to set up 'root' login, find 'PermitRootLogin' parameter and change its value from 'prohibit-password' to 'yes'
          PermitRootLogin yes

#Restart sshd service. sudo service sshd restart

