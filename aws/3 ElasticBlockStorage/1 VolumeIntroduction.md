## EBS Volumes
<img width="975" height="169" alt="image" src="https://github.com/user-attachments/assets/eca0c42f-6867-4435-bbcd-6810c32d974d" />

```sh
Amazon EBS volume is a durable, block-level storage device that you can attach to your instances.
-	Without Ec2 Instances we can’t Use EBS 
●	EBS volumes are highly durable, scalable fault tolerant persistent disks.
●	EBS is Nothing but Attaching hard disk to an EC2 instance .
●	We can  EBS Volumes For Storing Data, Loading Applications, and Booting Purpose.
●	We can run applications on this.
●	EBS volumes are AZ specific
●	If your EC2 instance want to use the volume both must create in same AZ.
●	 You can attach multiple EBS volumes to a single instance. The volume and instance must be in the same
Availability Zone. Depending on the volume and instance types, you can use Multi-Attach to mount a volume
 to multiple instances at the same time.
●	EBS volume can be detached from a instance and attached to a different instance
●	EBS volumes can be encrypted (FAQ)
●	EBS volumes can be resized (only increase)
●	Persistent storage, they are referring to a hard disk, data stored on disk is permanent even if the system reboots.
● EBS is a Network attached virtual drive.
● This is not a direct storage. The EBS will be stored somewhere in AZ and will be connected through network not
inside the same host where EC2 reside.
```
