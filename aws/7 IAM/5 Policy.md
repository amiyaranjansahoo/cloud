# Policies
```sh
•	It consists of permissions/ a set of rules
•	IAM policy is JSON document, containing a set of statements/permission, which describes AWS operations and
it can be attached to user, group and IAM role
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
<img width="678" height="361" alt="image" src="https://github.com/user-attachments/assets/44cc4c84-f52d-43ad-9b8a-79ffc8d89cb4" />

