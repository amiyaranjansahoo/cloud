```sh
1.  This automates transitioning of objects from high storage tiers to low storage tiers.
2.	 It also can expire/delete your objects eventually over a fixed amount of time.
3.  S3 life cycle management is basically a feature that allows you to specify rules that define how your object
 is managed throughout its lifetime within S3.
4.  It allows you to do is to switch your objects between different storage classes.
5.  It enables you to reduce cost.
6.  We can enable the rule for one or multiple buckets.
7.  Rules can be applied to a whole bucket or a subset of objects.
8.  Can be configured using console, CLI, SDK etc
9.  We cant configure back to previous storage class # deep archive storage class can't be transitioned back
10. Intelligent tearing can only transition to glacier or onezone.
11. Objects must be stored for at least 30 days before they can be transitioned to:
         S3 Standard-IA
         S3 One Zone-IA
         S3 Intelligent-Tiering (Infrequent Access tier)
12. Objects Smaller Than 128 KB Cannot Be Transitioned by Default
        This includes Standard-IA, One Zone-IA, Intelligent-Tiering, and Glacier classes.
```
<img width="1064" height="328" alt="image" src="https://github.com/user-attachments/assets/3955666e-ce50-47c8-b29b-17a0300691c5" />


## Demo
```sh
1.	Move 30 days old objects from standard to standard IA
2.	Move 6 months old objects to Glacier
3.	Move 1 years old objects to Glacier Deep Archive
4.	Delete 2 years old objects,
```
