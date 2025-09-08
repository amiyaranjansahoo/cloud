```sh
•	By default, all S3 resources are private. 
•	Only the account owner  can access all the resources. 
•	The owner can provide access to others by creating a policy. 
•	The policy are of 2 types. 
    o	Resource policy
    o	User Policy
•	The Resource policy is of 2 types.
    o	ACL
    o	Bucket policy
```
## ACL
```sh
Grants basic read/write permission on objects and buckets.
Use xml schema
```
## Bucket Policy
```sh
•	Grants permission for the bucket and objectswithin to AWS accounts
and IAM users.
•	Uses json
•	Can be used to grant fine-grained permission.
•	In most of the cases but not in all cases, they replaces ACLS
```
## User Policy
```SH
•	policies that we apply directly to IAM users/groups/roles in side the
 aws account
•	called as user based policy
•	Can be used for fine-grained access
•	Uses json
•	Can’t be used for anonymous access since they apply directly to users.
•	Can't be applied to the top level (i.e. root  ) user as this account
is not an IAM user.

```
