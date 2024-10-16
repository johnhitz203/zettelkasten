# ConnectWithFlyctl

[[index]]

## Backup Data to LOCALHOST w/ PG_DUMP
* This is a multi step process that requires creating a connection to both the fly application serving the webpages and the fly application running the database application that the web app is connected to.
* The command `$ fly ssh console` creates a vm that connects to the app that is being accessed
  * The DB port number changes w/ every connection
  * It's necessary to install net-tools on each new connection

### Connect to Web App to get DATABASE_URL
This process returns a connection string with the format: 
postgres://{username}:{password}@{hostname}:{port}/{database}
```
$ fly ssh console -a <app-name>
$ echo $DATABASE_URL
```
### Connect to Database App
```
$ fly ssh console -a <app-name-db>
$ apt-get install net-tools
$ netstat -ano | grep 5432


1. Connect to Database App
   a. `$ fly ssh console -a <app-name-db>`
   b. `$ apt-get install net-tools` 
   # Need to do w/ each new connection
   c. `$ netstat -ano | grep 5432` # returns ports

pg_dump -h 172.19.5.250 -U whodapet_demo_db -d whodapet_demo > demo_dateString.sql
fly ssh sftp get Backups/whodapet-demo_20240419.sql -a whodapet-demo-db

