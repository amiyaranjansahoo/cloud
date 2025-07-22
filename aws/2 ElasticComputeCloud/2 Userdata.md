## Userdata
```sh
It's a script that is executed on an EC2 instance at launch time, for example we are launching 50 EC2 instances
and we want to install a tool on all 50 that can be automated using userdata scripts.
→ Note: Its default behavior is to execute userdata script only ones i.e. at launch time, however there is a way
 to re-execute scripts.
--> Userdata can be used to automate the EC2 post installation steps
--> userdata is also called as bootstrap scripts
→ You can modify user data for instances, the instance must be in the stopped state.

Example: Website hosting or webserver configuration

Along with the EC2 insatnce, By default we get the below

		-- Operating system
		-- Operating system configuration

```
