# CREATE RDS
## Dev/Test

- Select MySQL database.
- Select Dev/Test - MySQL.
- Leave everything as default.
	- Except: 
		- DB instance class: \<t2.micro\>
- **Estimated monthly costs**: **15.68 USD**.
- Database instance identifier: \<databaseinstancename\>
- Master username: \<masterusername\>
- Master password: \<masterpassword\>
- Database name: \<databasename\>
- Port: always 3306 for MySQL.
- Backup retention period: \<0 days\>

## Relational databases

Remember the following points:

- RDS runs on virtual machines.
- You can not log into these operating systems however.
- Patching of the RDS Operating System and DB in Amazon's responsability.
- RDS is **NOT** serverless.
- Aurora serverless **IS** serverless.