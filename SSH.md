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
            
