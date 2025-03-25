https://github.com/NotHarshhaa/DevOps-Projects/tree/master/DevOps-Project-03

# 1 Login to the server as super user and perform below
## 1.1 Create users and set passwords – user1, user2, user3
### 1.1 Creating the users with password
```bash
sudo useradd -m user1, -p "userlogin12345"
sudo useradd -m user2, -p "userlogin12345"
sudo useradd -m user3, -p "userlogin12345"
```

## 1.2 Create Groups – devops, aws
### creating groups
```bash
sudo groupadd devops
sudo groupadd aws
```
## 1.3 Change primary group of user2, user3 to ‘devops’ group
### 1.3 
```bash
sudo usermod -aG devops user2
sudo usermod -aG devops user3
```
## 1.4 Add ‘aws’ group as secondary group to the ‘user1’
### add user1 to aws
```bash
sudo usermod -aG aws user1
```
## 1.5 Create the file and directory structure shown in the above diagram.
### create directories 1st then files into it.
```bash
sudo mkdir -p /dir1 /dir2/dir1/dir2/dir10 /dir3/dir11 /dir4/dir12 /dir5/dir13 /dir6 /dir7/dir10 /dir8/dir9 /opt/d
ir14/dir10
sudo touch /dir1/f1 /dir2/dir1/dir2/f3 /dir4/dir12/f4 /dir4/dir12/f5 /dir7/f3 /f1 /f2 /opt/dir14/f3
```
## 1.6 Change group of /dir1, /dir7/dir10, /f2 to “devops” group
### changes group of mentioned directories
```bash
sudo chgrp devops /dir1 /dir7/dir10/ /f2 
```

## 1.7 Change ownership of /dir1, /dir7/dir10, /f2 to “user1” user.
### change the ownership of dir and files
```bash
sudo chown user1 /dir1 /dir7/dir10/ /f2 
```


# 2 Login as user1 and perform below
Create users and set passwords – user4, user5
Create Groups – app, database
Login as ‘user4’ and perform below
Create directory – /dir6/dir4
Create file – /f3
Move the file from “/dir1/f1” to “/dir2/dir1/dir2”
Rename the file ‘/f2′ to /f4’
Login as ‘user1’ and perform below
Create directory – “/home/user2/dir1”
Change to “/dir2/dir1/dir2/dir10” directory and create file “/opt/dir14/dir10/f1” using relative path method.
Move the file from “/opt/dir14/dir10/f1” to user1 home directory
Delete the directory recursively “/dir4”
Delete all child files and directories under “/opt/dir14” using single command.
Write this text “Linux assessment for an DevOps Engineer!! Learn with Fun!!” to the /f3 file and save it.
Login as ‘user2’ and perform below
Create file “/dir1/f2”
Delete /dir6
Delete /dir8
Replace the “DevOps” text to “devops” in the /f3 file without using editor.
Using Vi-Editor copy the line1 and paste 10 times in the file /f3.
Search for the pattern “Engineer” and replace with “engineer” in the file /f3 using single command.
Delete /f3
Login as ‘root’ user and perform below
Search for the file name ‘f3’ in the server and list all absolute paths where f3 file is found.
Show the count of the number of files in the directory ‘/’
Print last line of the file ‘/etc/passwd’
Login to AWS and create 5GB EBS volume in the same AZ of the EC2 instance and attach EBS volume to the Instance.
Login as ‘root’user and perform below
Create File System on the new EBS volume attached in the previous step
Mount the File System on /data directory
Verify File System utilization using ‘df -h’ command – This command must show /data file system
Create file ‘f1’ in the /data file system.
Login as ‘user5’ and perform below
Delete /dir1
Delete /dir2
Delete /dir3
Delete /dir5
Delete /dir7
Delete /f1 & /f4
Delete /opt/dir14
Logins as ‘root’ user and perform below
Delete users – ‘user1, user2, user3, user4, user5’
Delete groups – app, aws, database, devops
Delete home directories of all users ‘user1, user2, user3, user4, user5’ if any exists still.
Unmount /data file system
Delete /data directory
Login to AWS and detach EBS volume to the EC2 Instance and delete the volume and then terminate EC2 instance.


