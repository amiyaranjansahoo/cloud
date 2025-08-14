# Policies
```sh
•	It consists of permissions/ a set of rules
```
## Types of Policy
```sh
Managed Policies :
•	Managed policies are default policies.
•	We can attach Or Assign to multiple Entities. ( roles, Users, groups )
•	Stand-alone-based policies attached to multiple users/groups. 
•	Which are Pre-defined by AWS in Root Accounts.

Customer Managed Policies : 
•	A customer-managed policy is a standalone policy that we are going to create and administer in our AWS account.
•	We can attach these policies to multiple entities.(User/role/Group)
•	You can Create Customer Managed Policies  by using Visual Editor or JSON.

Inline Policies :
•	Policies that we are going to create that are embedded directly into a single entity (USER or   GROUP).
•	These are custom Inline Polices.....
•	Once You delete IAM User/Group, along with the Entities the inline Policy will also be deleted.
```
