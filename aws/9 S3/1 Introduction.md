## Simple Storage Services
```sh
•	S3 is highly available, durable, scalable, fault tolerance object based storage.(data is
 stored as an Object )
•	S3 is an internet based service.
•	For storing and processing log files
•	S3 is a storage for the internet.
•	S3 is highly available, durable, scalable, fault tolerance object based storage
•	It has a simple web services interface for the simple storing  and retrieving of any amount
 of data anytime from anywhere on the internet
•	S3 is object based storage
•	You cannot install operating system on S3
•	S3 has a distributed data store architecture where objects are redundantly stored in
multiple locations ( minimum 3 location in same region)
•	data is stored in bucket
•	A bucket is a flat container of objects
•	Max capacity of object inside the bucket  is 5 TB
•	You can create folders in your bucket ( available through console)
•	You cannot create nested bucket
•	Bucket ownership is non-transferable
•	S3 bucket is region specific
•	You can have up to 100 buckets per account ( May expand on request )
•	Use Cases of S3
•	It's used for data lake (The storage to put unlimited amount of data)
•	Its best place to put binary data like photos, videos, audios, pdf, worddoc, etc.
•	DevOps people use S3 for storing artifacts, war, jar, zip, exe files etc..
•	For storing and processing log files
•	We can store unlimited amounts of data on S3, however an object size can't be more than
5TB.
```
## S3 bucket naming rules
```sh
•	S3 bucket name are globally unique across all AWS regions
•	Bucket names must begin and end with a letter or number.
•	Bucket names can consist only of lowercase letters, numbers, dots (.), and hyphens (-).
•	Bucket name can’t start or end with a hyphen.
•	Bucket name should not be an IP address 
•	Bucket names cannot be change after they are created.
•	If a bucket is deleted, its name becomes available again to you or other account to use
•	Bucket names must be at least 3 and no more than 63 characters long
•	Bucket names are part of the URL used to access a bucket
•	Bucket names can contain lowercase numbers and hyphen but cannot use upper case letter.
•	By default bucket and its object are private and only the owner can access.
```
## S3 Objects
```sh
•	An object size stored in an S3 bucket can be 0 byte to 5 TB
•	Each object is stored and retrieved by a unique key ( ID or name)
```

