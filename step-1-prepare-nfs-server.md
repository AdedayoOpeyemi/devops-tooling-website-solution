# STEP 1 – PREPARE NFS SERVER

1. Spin up a new EC2 instance with RHEL Linux 8 Operating System.

![](images/nfs-server.PNG)

2. Based on your LVM experience from Project 6, Configure LVM on the Server.

![](images/nfs-volumes.PNG)

![](images/default-devices.png)

![](images/configured-partition.png)


- Instead of formating the disks as ext4 you will have to format them as xfs

![](images/lvmscan.png)

![](images/pvcreate.png)

- Ensure there are 3 Logical Volumes. lv-opt lv-apps, and lv-logs

![](images/lv-vlm.png)

![](images/xfs-formatting.png)


- Create mount points on /mnt directory for the logical volumes as follow:
Mount lv-apps on /mnt/apps – To be used by webservers
Mount lv-logs on /mnt/logs – To be used by webserver logs
Mount lv-opt on /mnt/opt – To be used by Jenkins server in Project 8

![](images/mount-devices.png)

![](images/fstab-edit.png)

![](images/perm-mount.png)