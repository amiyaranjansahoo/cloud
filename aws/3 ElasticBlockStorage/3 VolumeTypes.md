## Differences B/w SSD & HDD
```sh
 SSD:
-	Stands For Solid State Drive
-	SSD is Durable, Faster, More Energy Efficient
-	It is used for Performing tasks like Booting & Loading Applications.
-	Very Fast Processing for Low Data
-	Small in Size 
-	SSD’s are Most Costlier than HDD
-	the performance of the SSD is measured in terms of IOPS [ Input & Output operations per second]
HDD:
-	HDD stands for Hard Disk Drive
-	It is a Type of Storage Device.
-	Compare to SSD, HDD are Slower & Less Energy Efficient but they are tend to affordable at Higher
Storage Capacities.
-	Big in Size
-	Low Cost disk drives
```
# Volume Types
```sh
EBS backed EC2
Instance Storage backed EC2
```
## EBS Types
```sh
1) Solid State Drive (SSD)  
	→  General Purpose SSD’s
	→ Provisioned IOPS SSD’s
2) Magentic Hard Disk Drive - HDD
	→ Throughput Optimized HDD volumes
        → Cold HDD volumes
3) Previous Generation
```


## General Purpose SSD’s
```sh
a.	This is a default volume, when we create an EC2, by default this gets selected.
b.	In case you want to choose different one, then you have to select explicitly
c.	GP2 volume are backed by SSD
d.	It balances both price and performance
e.	Boot volume having low latency ( less than 10 mili sec)
f.	30 GB is free under free tier .
g.	Volume size – 1 GB to 16 TB
h.	AWS recommend these volumes for most of the workloads.
i.	Not Supports Amazon EBS Multi-attach – one EC2 can attach to one general purpose SSD
j.	This is bootable i.e. Supports Boot volume – The OS can be installed in this device  like C: drive
k.	Two variants are available gp2 and gp3
i.	gp3 is more powerful compared to gp2 in terms of throughput
l.	Use case
i.	Low-latency interactive apps
ii.	Development and test environments
iii.	Use it for less critical applications even in production
iv.	Not intended for highly critical production workloads
v.	We pay for size of the disk
```
                   
		
		
