This is a script that will prepare sample objects used in parts 1-2 of my blog series:
https://rafal.hashnode.dev/use-sqlcl-liquibase-to-move-all-database-objects-from-dev-to-the-uat-environment-part-1
https://rafal.hashnode.dev/track-your-dev-database-changes-using-sqlcl-liquibase-and-move-it-to-uat-part-2


Prerequisities:
1. You need to have either:
a) Oracle OCI Free tier, and access to your ADMIN user.
or
b) Prepare On-premise Oracle DB, with access to SYS as SYSDBA user.
2. You need to have TNS names configured with your database connections.
3. To check your TNS:
log into SQLcl
  sql /nolog
check TNS by executing
  show TNS

Create sample objects:
1. Run demo script:
a) for OCI database, connect to your SQLcl and execute script @demo_oci.sql
b) for ON-Premise, execute @demo_on_premise.sql

Script will ask you for your TNS name of your DEV and UAT connections.
Provide your values or use defaults (you need to edit scripts and change default values for easier re-runnning of script in the future)

After successful running of script you will have:
- two new schemas created, DEV and UAT (or other name you provide)
- DEV schema with few sample objects
- UAT schema with no objects
WARNING: if users DEV or UAT existed before executing script IT WILL BE DELETED WITH ALL DATA.

### Now you can successfully read my blog post part 1 and do all the workshops on your database :)
https://rafal.hashnode.dev/use-sqlcl-liquibase-to-move-all-database-objects-from-dev-to-the-uat-environment-part-1

