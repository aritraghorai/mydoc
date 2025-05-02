---
{"dg-publish":true,"permalink":"/notes/learning/devops/linux/linux-concept/","title":"Linux Concept"}
---

## Linux Kernel
![Linux Kernal.png](/img/user/assets/Linux%20Kernal.png)

`Linux kernal is program which is sit between Hardware and softwors.`
### Kernel handle 4 major task 
- Memory Management
- Process Management
- Device Driver
- System call and security
### Commands
```bash
uname  ## To see kernal name
uname - ## To See kernel version
```

## Working with hardware
![Hard Wokring in linux.png](/img/user/assets/Hard%20Wokring%20in%20linux.png)

```bash
udevadm info --query=path --name=/dev/sda1 
/devices/pci0000:00/0000:00:1f.2/ata1/host0/target0:0:0/0:0:0:0/block/sda/sda1
udevadm monitor ## For monitoring kernal events
lspci ## to list all the pci
```

### Commands 
- `udevadm` for monitor kernel events
- `lspci` to list all pci devices
- `lsblk` to see all disks
- `lscpu` give information about CPU
- `lsmem` to see all available
- `free -h` to see all free memory
- `lshw` to see all hardware config

## Linux Boot Sequence
![Linux Boot Sequence.png](/img/user/assets/Linux%20Boot%20Sequence.png)

## Run level
We can run linux in multiple mode like GUI,command-line it is decide by runlevel
![Linux Runlevel.png](/img/user/assets/Linux%20Runlevel.png)

### Command
- `systemctl get-default` get default run-level
- `ls -ltr /etc/systemd/system/default.target` check default target file

### Note
The term runlevels is used in the **sysV init** systems. These have been replaced by systemd targets in **systemd** based systems.

The complete list of runlevels and the corresponding systemd targets can be seen below:

**runlevel 0 -> poweroff.target**

**runlevel 1 -> rescue.target**

**runlevel 2 -> multi-user.target**

**runlevel 3 -> multi-user.target**

**runlevel 4 -> multi-user.target**

**runlevel 5 -> graphical.target**

**runlevel 6 -> reboot.target**

## File type
### 3 Type of file
- Regular files
- Directory
- Special file
     - Character file
     - Block file - get disks
     - links 
         - Hard link - It delete actual file after deletion.
         - Soft link - it is pointer to another file.After deletion it does not delete the actual file.
     - Socket
     - Named pipe
### Check file type in Linux
![File type in linux.png](/img/user/assets/File%20type%20in%20linux.png)

## File system hierarchy
![Linux filesystem hierarchy.png](/img/user/assets/Linux%20filesystem%20hierarchy.png)

- `/home` -  all user home folder except root user 
- `/opt` for all external program
- `/mnt`for mount a temporary drive
- `/tmp` for store all temporary data
- `/media` for all external media `df -hP` to see all mounted media
 - `/dev` it is for all external drive
 - `/bin` contain all the binary
 - `/etc` contain all binary
 - `/lib` for shared library
 - `/var ` which contain all the logs
 - `/usr` for all user application data
## Compression In Linux
### Using tar utility
```bash
## Create a tar
tar -cf [name of tar] [...files] ## tar -cf my.tar ab.txt a.txt
## See the contain of the tar
tar -tf my.tar
### Extracting a tar
tar -xf test.tar
## Compress 
tar -zfc [name of tar] [...files]
```

### Different Compression
![Type of compression in linux.png](/img/user/assets/Type%20of%20compression%20in%20linux.png)

### Uncompressed with different command
![UnCompression.png](/img/user/assets/UnCompression.png)

## Searching in Linux
### Using locate
```sh
locate a.txt
```

#### Note
 Locate is depend on `updatedb`command

### Using Find Command
```sh
find /home/aritra -name a.txt 
```

### Using Grep
```sh
grep a.txt # grep is case sensitive for insesitive we can use -i flag
grep -w hi a.txt # find by word
grep -r hi [directory] # recursively find all the files
grep -A1 [search] [file] # Print 1 line after match
grep -B1 [search] [file] # print 1 line before match
```


## Networking Basics
### Dns - Domain Name System
![Domain Name.png](/img/user/assets/Domain%20Name.png)

### Domain Name
![Type of domain name.png](/img/user/assets/Type%20of%20domain%20name.png)


### Tools for dns resolution
`nslookup`
`dig`


## Linux Security
![Linux Security.png](/img/user/assets/Linux%20Security.png)

### Linux Account
- User account 
     - Each user has unique id and username , gid
  ![assets/Linux user.png](/img/user/assets/Linux%20user.png)
  ![Linux Type of User account.png](/img/user/assets/Linux%20Type%20of%20User%20account.png)
- Groups - collection of account

#### Commands 
- `id` to see user id
- `last` to see last logged in user
- `who` current user detail
### Access Control file

#### Representation `usernmae:password:UID:GID:GECOS:HOMEDIR:SHELL`
![Linux Access Control file.png](/img/user/assets/Linux%20Access%20Control%20file.png)

#### /etc/shadow
`username:password:lastchange:minage:maxage:warn:inactive:expdate`
#### /etc/group
`name:password:gid:members`
![Access Control File 2.png](/img/user/assets/Access%20Control%20File%202.png)

### Manage User
#### `useradd`  - add user
```sh
useradd bob
# -d for hom directory -s default shell -c for custom comment
useradd -u 1099 -g 1099 -d /home/app -s /bin/bash -c "Notmal user" bob
# to check the detail
id bob
```
#### `passwd` - to set password  
```sh
### it neeeds to run as root
passwd bob
```
#### `userdel` - to delete a user
```bash
userdel bob
```
#### `groupadd` - add a group
```bash
goupadd -g 1011 example
```
#### `groupdel` - to delete a goup
```sh
groupdel example
```

###  Permission
#### File Permission
![Linux File permission.png](/img/user/assets/Linux%20File%20permission.png)
#### Directory Permission
![Directory Permission.png](/img/user/assets/Directory%20Permission.png)

#### Combination of permission
![Combination of permission.png](/img/user/assets/Combination%20of%20permission.png)

#### Modifying the file permission
##### `chmod` Change permission
```sh
chmod u+rwx file.txt # giving owner full access
chmod ugo+r-x file.txt # giving owner,group,other read execute permission
chmod u+rw,g+r-x,o+--x file.txt 
chmod 777 file.txt # giving everyone full access
```

##### `chown` Change ownership
```bash
chown owner:goup file.txt
chown bob file.txt
```


### Ssh and Scp
`ssh` use ssh
```bash
ssh user@hostname
```

#### `ssh-copy-id` copy public key to remote server 
```bash
ssh-copy-id root@ip
## We can copy only particular id
ssh-copy-id root@gmai -i aritraghorai0      
```

#### `scp` copy file between two computer
```sh
# -p for preserve permission -r to copy directory
scp -pr /home/app root@app:home/app
```

### Firewall
#### Ip tables
![Ip tables.png](/img/user/assets/Ip%20tables.png)


## Service Management
![Service Management.png](/img/user/assets/Service%20Management.png)

### Commands 
- `systemctl` command
```bash
systemctl start docker ##start docker service
systemctl stop docker ## stop docker service
systemctl restart docker
systemctl reload docker 
systemctl enable docker
systemctl disble docker
##We want to tell systemd that unit file has been change
systemctl daemon-realod
systemctl edit app.service --full
systemctl list-units --all # to show all units
```

- `journalctl`
```sh
journalctl -b
journalctl -u docker.service # To checl the logs of the service
```

## Storage
![Storage basics in linux.png](/img/user/assets/Storage%20basics%20in%20linux.png)

### Block Devices
- Block device is kind of file that we can find inside `/dev` directory.
- It used to store data.
- It is called block storage because data is written to it in blocks.
- We can see block devices by `lsblk` Command

![Linux Block Devices.png](/img/user/assets/Linux%20Block%20Devices.png)

#### Commands
- `lsblk`
- `fdisk` to describe particular disk
![Fdisk.png](/img/user/assets/Fdisk.png)

### Partition type
There are three partition in Linux operating system.
- **Primary partition**:Used for boot
- **Extended partition**:We can't use it but help us to host multiple logical partition.
- **Logical Partition**:We create inside extended partition.
### Partition Scheme
#### `MBR` - Master book record
- In mbr maximum size of disk is 10 tb
- We can't create more than 4 primary partition.
#### `GPT` - Guid Partition table
- It is most recent partition scheme created for limitation for `MBR`
- `Gpt` can have unlimited number of partition no size limit.
- Limitation exposed by the operating system.Like `Rehl` has 128 partition maximum.
### Creating Partition
- `gdisk` : It is improved version of fdisk which work with gpt partition table.
```sh
gdisk [Partition]
```

### File system
It define how data store in a disk.
#### Types
![File system type.png](/img/user/assets/File%20system%20type.png)
![File Type 2.png](/img/user/assets/File%20Type%202.png)

#### Commands
- `mkfs.ext4 /dev/sd1` Create ext4 file drive
- `mount` for mounting the drive
![Fstab.png](/img/user/assets/Fstab.png)

### External Storage
![External Storage.png](/img/user/assets/External%20Storage.png)

#### `DAS` Direct Attach Storage
![DAS.png](/img/user/assets/DAS.png)

#### `NAS` Network attach Storage
![NAS.png](/img/user/assets/NAS.png)

#### `SAN` Storage Area Network
![SAN.png](/img/user/assets/SAN.png)

### `NFS` - Network Storage
![NFS.png](/img/user/assets/NFS.png)

### `LVM ` Logical Volume Manager
Grouping multiple volume into one.
![Linux LVM.png](/img/user/assets/Linux%20LVM.png)

- To use lvm we have to install package `lvm2`




