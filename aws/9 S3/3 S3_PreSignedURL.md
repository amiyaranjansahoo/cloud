## What is Pre Signed URL?
```sh
•	A pre-signed URL in Amazon S3 is a temporary, time-limited URL that gives
someone secure access to an S3 object without requiring them to have AWS
credentials.
```
## How it works:
```sh
•	Normally, to access a private S3 object, you need AWS IAM permissions.
•	With a pre-signed URL, you (the object owner or an authorized AWS user)
generate a signed link using your credentials.
•	This link includes:
    o	The object’s location (bucket + key).
    o	Expiration time (minutes, hours, or days).
    o	A signature based on your AWS credentials.
•	Anyone with the URL can perform the allowed operation (GET, PUT, etc.)
until it expires.
```
## Key points:
```sh
•	Expiration can be from 1 second up to 7 days (default max with AWS SDK/CLI).
•	Works only for the action you specify (get_object, put_object).
•	After expiration, the link is invalid.
```
## How to generate:
```sh
•	To generate a presigned URL using the AWS Management Console
•	Sign in to the AWS Management Console and open the Amazon S3 console at
https://console.aws.amazon.com/s3/.
•	In the Buckets list, choose the name of the bucket that contains the object
that you want a presigned URL for.
•	In the Objects list, select the object that you want to create a presigned
URL for.
•	On the Actions menu, choose Share with a presigned URL.
•	Specify how long you want the presigned URL to be valid.
•	Choose Create presigned URL.
•	When a confirmation appears, the URL is automatically copied to your
clipboard. You will see a button to copy the presigned URL if you need to
copy it again.
•	It works even the object is private
```
## AWS CLI
```sh
Aws cli: aws s3 presign s3://my-bucket/myfile.txt --expires-in 3600
```


