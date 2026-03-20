## Configure the provider
```sh
a.	Code for provider
b.	google => terraform aws provider
```

```sh
# Configure the AWS Provider
provider "aws" {
  region = "ap-south-1"
}
```
```sh
1.	We have selected one region, during execution of aws configure , however this region will take the priority
2.	I have mentioned the Mumbai region.
3.	And type of activities will be performed in Mumbai region only 
```
