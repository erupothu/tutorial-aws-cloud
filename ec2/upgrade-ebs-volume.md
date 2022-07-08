AWS Console 

1. Volumes
  * select volume to upgrade related to Required EC2 instance
  * Modify the Volume
2. Login to EC2 Instance and Run Below Commands

df -hT
Filesystem      Type  Size  Used Avail Use% Mounted on
/dev/xvda1      ext4  8.0G  1.9G  6.2G  24% /
/dev/xvdf1      xfs   8.0G   45M  8.0G   1% /data

[ec2-user ~]$ lsblk
NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  16G  0 disk
└─xvda1 202:1    0   8G  0 part /
xvdf    202:80   0  30G  0 disk
└─xvdf1 202:81   0   8G  0 part /data

[ec2-user ~]$ sudo growpart /dev/xvda 1


[XFS volumes]
[ec2-user ~]$ sudo yum install xfsprogs
[ec2-user ~]$ sudo xfs_growfs -d /

[ext4 volumes] 
[ec2-user ~]$ sudo resize2fs /dev/xvda1

df -h
