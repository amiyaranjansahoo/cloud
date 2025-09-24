```sh
1.  This automates transitioning of objects from high storage tiers to low storage tiers.
2.	It also can expire/delete your objects eventually over a fixed amount of time.
3.  S3 life cycle management is basically a feature that allows you to specify rules that define how your object
 is managed throughout its lifetime within S3.
4.  It allows you to do is to switch your objects between different storage classes.
5.  It enables you to reduce cost.
6.  We can 
```

## rule scope
```sh
1.  Limit the scope of this rule using one or more filters : We can select one or more object by mentioning the folder name in below prefix filed 
## Demo
```sh
1.	Move 30 days old objects from standard to standard IA
2.	Move 6 months old objects to Glacier
3.	Move 1 years old objects to Glacier Deep Archive
4.	Delete 2 years old objects,
```
