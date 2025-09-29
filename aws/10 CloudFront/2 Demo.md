## For public access
```sh
{
  "Id": "Policy1675245969017",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Stmt1675245966980",
      "Action": [
        "s3:GetObject"
      ],
      "Effect": "Allow",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*",
      "Principal": "*"
    }
  ]
}
```
## FOR CF access # OAC control
```sh
{
    "Version": "2012-10-17",
    "Statement": {
        "Sid": "AllowCloudFrontServicePrincipalReadOnly",
        "Effect": "Allow",
        "Principal": {
            "Service": "cloudfront.amazonaws.com"
        },
        "Action": "s3:GetObject",
        "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*",
        "Condition": {
            "StringEquals": {
                "AWS:SourceArn": "ARN-OF-YOUR-CF-DISTRIBUTION"
            }
        }
    }
}
```
