```sh
•	S3 Bucket versioning is used to protect against accidental object/data
deletion or overwrites.
•	Versioning can also be used for data retention and archive
•	By default its disable
•	if you upload same 5 GB video 10 times on S3, this object is stored with
10 different versions which will occupy the size 10*5 = 50GB
•	Once you enable the versioning on a bucket, it can’t be disabled however
it can be suspended
•	When enabled, bucket versioning will protect existing and new object and
maintains their versions as they are updated.
•	Versioning works on bucket level, we can’t enable the versioning on
object level
•	When versioning is enabled and you try to delete an object, a delete marker
is placed on the object
o	You can still view the object and delete the marker
•	You can delete the “Delete marker” and object will be available again
•	You will be charged for all S3 storage cost for all object versions stored.
•	You can use versioning with S3 life cycle policies to delete older versions
or you can move them to a cheaper S3 storage ( or glacier)
•	Bucker versioning State:
    o	Enabled
    o	Suspended
    o	Un-versioned # It wont see this option any where.
•	Object existing before enabling versioning will have a version id or null
•	If you have a bucket that is already versioned, then you suspend versioning
existing object and their versions remain as it is.
o	However they will not be updated/versioned further with future updates while
 the bucket versioning is suspended
•	New object ( uploaded after suspension ) they will have a version id “null”
if the same key ( name) is used to store another objects, it will override the
existing one.
•	An object detention in  a suspended versioning bucket , will only delete the
 object with ID null
```
