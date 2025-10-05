## A record:
```sh
o	Address record – Maps domain name to IP address
o	www.cloud.com IN 8.8.8.8 ( IN means internet)
o	32 bit hence A
```
## AAAA Record
```sh
o	IPv6 address Record
o	Maps domain name to an IPv6 address
o	www.cloud.com IN AAAA.2002.b7861.1
o	128 bit hence 32*4 hence AAAA
```
## CNAME Record
```sh
o	Directs one name to another name
o	Give you server to another name
o	mail.com => mail.google.com
o	So when you move you servers, you only have to change one set of records
o	Canonical name Record
o	Maps an alias to a hostname
o	web IN CNAME www.cloud.com
o	The actual name is cloud.com but people might search for www.cloud.com. So we
 can define the Canonical record as www.cloud.com and when people search for
www.cloud.com  that takes to the cloud.com 
```
