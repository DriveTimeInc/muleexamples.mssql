# Microsoft SQL Server Integrated Security in a Mule
## Prerequisites
- [Anypoint Studio](https://www.mulesoft.com/lp/dl/studio)
- [Maven](https://maven.apache.org/download.cgi)
---
## Setup
1. Download the [JDBC Driver for SQL Server](https://docs.microsoft.com/en-us/sql/connect/jdbc/microsoft-jdbc-driver-for-sql-server)
2. Copy `sqljdbc_auth.dll` to `{AnypointStudioLocation}\plugins\org.mule.tooling.server.{runtimeVersion}.ee_{studioVersion}\mule\lib\boot`
3. Copy `sqljdbc42.jar` to `{AnypointStudioLocation}\plugins\org.mule.tooling.server.{runtimeVersion}.ee_{studioVersion}\mule\lib\user`
4. Update the [Run Configuration](https://support.mulesoft.com/s/article/ka4340000004H3mAAE/How-to-pass-additional-startup-arguments-to-Mule) with an additional VM Argument indicating the location of the `sqljdbc_auth.dll`. 
```
-Djava.library.path="{AnypointStudioLocation}\plugins\org.mule.tooling.server.{runtimeVersion}.ee_{studioVersion}\mule\lib\boot"
```
## Running
1. Specify the `db.host` and `db.database` in `src/main/resources/environment.properties`. (If your `db.host` URI requires sub paths, use `\\`.)
2. Modify the Database Connector to include a relevant query to your database.
