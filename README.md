# initraid
init raid


The code runs on centos6.9. The background is that there is only one program and data partition. In order to protect the program, partition encryption is implemented. At this time, when the partition space is not enough, it cannot be expanded.

The scheme is to create a new data partition to separate the program partition from the data partition.

(1).
The program detects that if there is a new single disk, it will use the disk to cut out a data partition and migrate data through soft connection.
(2).
The program detects that if there are new dual disks, it will use two disks to form RAID1, cut out a data partition and migrate data through soft connection.
