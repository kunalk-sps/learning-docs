```
Export Data from Kubernetes MongoDB (mongodump)
	kubectl exec -it <mongodb-pod-name> -- bash

	mongodump --out=/tmp/mongodump

if DB has authentication
mongodump \
  --db=test_abc \
  --username=<your-username> \
  --password=<your-password> \
  --authenticationDatabase=admin \
  --out=/tmp/mongodump

mongodump \
  --db=my_db_name\
  --username=my_userName \
  --password=my_pass \
  --authenticationDatabase=admin \
  --out=/tmp/mongodump

Then copy it to your local system
	kubectl cp <mongodb-pod-name>:/tmp/mongodump ./mongodump.
	docker cp guacamole:/opt/guacamole/mysql/schema C:\guac_schema

	# Use a relative or WSL-style path for the destination.
	kubectl cp my-pod-c648cbbb9-rdn99:/tmp/mongodump ./mongo_dump

	# Use Git Bash or WSL and format it like:
	kubectl cp my-pod-c648cbbb9-rdn99:/tmp/mongodump /c/mongo_dump


mongorestore --db to_db D:\mongo_dump\folder_name
mongorestore --db to_db_avc C:\Users\user\Desktop\mongo_dump\folder_name
mongorestore --db to_db_avc C:\Users\user\Desktop\mongo_dump\folder_name
mongorestore --db to_db D:\mongo_dump_v1\folder_name
```