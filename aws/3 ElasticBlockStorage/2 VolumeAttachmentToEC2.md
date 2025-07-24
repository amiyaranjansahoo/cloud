## How to mount EBS to ec2
```sh
    1. lsblk                                        ----> To List Blocks or disk drives along with its Mount points.
    2  mkdir /java                --->  First Create one path to EBS Volume 
    3  mkfs -t ext4 /dev/xvdb               --->  Make File System
    4  mount /dev/xvdb /java      --->  To mount EBS Volume
    5  lsblk                               → To List Blocks or disk drives along with its Mount points.
    6  umount /dev/xvdb /java     ----> To UnMount the Disk Drives or EBS Volumes.
    7  lsblk
```
