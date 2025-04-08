https://github.com/NotHarshhaa/DevOps-Projects/tree/master/DevOps-Project-03

# 1 Login to the server as super user and perform below
## 1.1 Create users and set passwords – user1, user2, user3
### 1.1 Creating the users with password
```bash
sudo useradd -m user1 -p "userlogin12345"
sudo useradd -m user2 -p "userlogin12345"
sudo useradd -m user3 -p "userlogin12345"
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
## 2.1 Create users and set passwords – user4, user5
```bash
sudo adduser user4
sudo adduser user5
```
Note:- It will ask you to enter password and other details.

## 2.2 Create Groups – app, database
```bash
sudo addgroup app
sudo addgroup database
```

# 3 Login as ‘user4’ and perform below
a. Create directory – /dir6/dir4
b. Create file – /f3
c. Move the file from “/dir1/f1” to “/dir2/dir1/dir2”
d. Rename the file ‘/f2′ to /f4’
```bash
sudo usermod -aG sudo user4
su user4
sudo mkdir -p /dir6/dir4
sudo touch /f3
sudo mv /dir1/f1 /dir2/dir1/dir2
sudo mv /f2 /f4
```

# 4 Login as ‘user1’ and perform below
Create directory – “/home/user2/dir1”
Change to “/dir2/dir1/dir2/dir10” directory and create file “/opt/dir14/dir10/f1” using relative path method.
Move the file from “/opt/dir14/dir10/f1” to user1 home directory
Delete the directory recursively “/dir4”
Delete all child files and directories under “/opt/dir14” using single command.
Write this text “Linux assessment for an DevOps Engineer!! Learn with Fun!!” to the /f3 file and save it.
```bash
sudo usermod -aG sudo user1
su user1
sudo mkdir -p /home/user2/dir1
sudo cd /dir2/dir1/dir2/dir10
sudo touch /opt/dir14/dir10/f1
sudo mv /opt/dir14/dir10/f1 /home/user1
sudo rm -r /dir4
sudo rm -r /opt/dir14/*
echo "Linux assessment for an DevOps Engineer!! Learn with Fun!!" > /f3
```

# 5 Login as ‘user2’ and perform below
Create file “/dir1/f2”
Delete /dir6
Delete /dir8
Replace the “DevOps” text to “devops” in the /f3 file without using editor.
Using Vi-Editor copy the line1 and paste 10 times in the file /f3.
Search for the pattern “Engineer” and replace with “engineer” in the file /f3 using single command.
Delete /f3
```bash
sudo usermod -aG sudo user2
su user2
sudo touch /dir1/f2
rm -r /dir6
rm -r /dir8
sudo sed 's/DevOps/devops/g' /f3
sudo vi /f3
```
1. Copy the first line:
   Press Esc to ensure you are in command mode.
   Type yy to yank (copy) the first line.
2. Paste the line 10 times:
   Move the cursor to the position where you want to start pasting.
   Type 10p to paste the copied line 10 times.
3. Save and exit:
   Press Esc to ensure you are in command mode.
   Type :wq and press Enter to save the changes and exit the editor.
```bash
sudo sed -i 's/Engineer/engineer/g /f3
```

# 6 Login as ‘root’ user and perform below
Search for the file name ‘f3’ in the server and list all absolute paths where f3 file is found.
Show the count of the number of files in the directory ‘/’
Print last line of the file ‘/etc/passwd’
```bash
sudo su -
find / -name f3
find / -type f | wc -l
tail -n 1 /etc/passwd
```
# 7 Login to AWS and create 5GB EBS volume in the same AZ of the EC2 instance and attach EBS volume to the Instance.

## 7.1 Login as ‘root’user and perform below
Create File System on the new EBS volume attached in the previous step
Mount the File System on /data directory
Verify File System utilization using ‘df -h’ command – This command must show /data file system
Create file ‘f1’ in the /data file system.

Here are the steps to log in to AWS, create a 5GB EBS volume, and attach it to an EC2 instance:

### Step 1: Log in to AWS
1. **Go to the AWS Management Console**: [AWS Management Console](https://aws.amazon.com/console/).
2. **Sign in**: Use your credentials to sign in as either the root user or an IAM user.

### Step 2: Create a 5GB EBS Volume
1. **Navigate to the EC2 Dashboard**:
   - In the AWS Management Console, go to the **EC2** service.
2. **Create a Volume**:
   - In the left-hand menu, click on **Volumes** under the **Elastic Block Store** section.
   - Click on the **Create Volume** button.
   - Set the **Size** to `5 GiB`.
   - Select the **Availability Zone** to match your EC2 instance's AZ.
   - Configure other settings as needed (e.g., volume type, encryption).
   - Click **Create Volume**.

### Step 3: Attach the EBS Volume to the EC2 Instance
1. **Select the Volume**:
   - In the **Volumes** section, find the volume you just created.
   - Select the volume by clicking the checkbox next to it.
2. **Attach the Volume**:
   - Click on the **Actions** dropdown and select **Attach Volume**.
   - In the **Instance** field, select your EC2 instance from the list.
   - Specify the **Device** name (e.g., `/dev/sdf`).
   - Click **Attach Volume**.

### Step 4: Format and Mount the Volume (Optional)
1. **Connect to your EC2 Instance**:
   - Use SSH to connect to your instance.
2. **Format the Volume**:
   ```bash
   lsblk
   sudo mkfs -t ext4 /dev/nvme1n1
   ```
3. **Mount the Volume**:
   ```bash
   sudo mkdir /data
   sudo mount /dev/nvme1n1 /data
   ```
4. Verify the Volume 
```bash
df -h
touch /data/f1
```

# 8 Login as ‘user5’ and perform below
Delete /dir1
Delete /dir2
Delete /dir3
Delete /dir5
Delete /dir7
Delete /f1 & /f4
Delete /opt/dir14
```bash
sudo usermod -aG sudo user5
su user5
rm -r /dir1 /dir2 /dir3 /dir5 /dir7
rm -r /f1 /f4
rm -r /opt/dir14
```
## 9 Logins as ‘root’ user and perform below
Delete users – ‘user1, user2, user3, user4, user5’
Delete groups – app, aws, database, devops
Delete home directories of all users ‘user1, user2, user3, user4, user5’ if any exists still.
Unmount /data file system
Delete /data directory
Login to AWS and detach EBS volume to the EC2 Instance and delete the volume and then terminate EC2 instance.
```bash
sudo su -
userdel user1 user2 user3 user4 user5
groupdel app aws database devops
rm -r /home/user1 /home/user2 /home/user3 /home/user4 /home/user5
unmount /data
rm -r /data
```

Login to AWS, go to volumes, checkbox the 5GB EBS volume.
go to actions -> dettach volume


