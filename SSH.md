# SSH  [ACCESSING THE TERMINAL(RHEL) IN THE CMD(WINDOWS)]
## Prerequisites
  - Redhat Linux is installed in VMware, which runs on the Windows.
  - RHEL VMware must be running
  - RHEL should have SSH server installed and in the active status.
  - SSH should also be installed in Windows
## Step by Step procedure to run Linux into CMD.
### Step 1: Install OpenSSH Client on Windows
      - open Powershell as Administrator.
      - run command "ssh" to check if it is working.
### Step 2: Enable SSH on Red Hat Linux
      - Install ssh server if not installed use this command --> "sudo yum install -y openssh-server"
      - start and enable the ssh service by using these commands --> 
                  "sudo systemctl start sshd " (note - rhel uses "sshd" and ubuntu uses "ssh")
                  "sudo systemctl enable sshd"
      - check the ip address oof the RHEL, use command --> "ifconfig".
### Step 3: Test SSH from Windows CMD
      - write this command --> "ssh username@ip_address".
      - at the place of "username" provide the name of the user which you want to login as.
      - "ip_address" change it with the ip of the RHEL which we saw in step-2.
      - after that it will ask the password of that user, write the correct password.
      - you will be logged in as the user of the RHEL into the cmd, now you can run commands as the provided user.
### Step 4: Setup key Authentication (Login without using password via keygen)
      - Open windows CMD and write the command -> "ssh-keygen -t rsa", 
      - This will save the file in location-> "c:\Users\<your-name>\.ssh\id_rsa"
      - There will be two files generated named as "id_rsa" (private key) and "id_rsa.pub" (public key).
      - Copy the public key to the Linux using the command -> "ssh-copy-id username@<linux-ip>"
      - Or Manually copy the content of "id_rsa.pub" into the linux at this location -> "~/.ssh/authorized_keys". (here "~" is the home of the particular user for which you want to give             keygen access.
      - Now test it, write this command --> "ssh username@ip_address".

### NOTE- When we place or copy the public key to the given folder, it will only work on the same user in which you have given the public key. 
          for example - you cannot access root user without password if you have only provided public key into the other users folders and not to the root user.

      
            
