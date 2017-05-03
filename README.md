# Microsoft SQL Server Integrated Security in a Mule
## Prerequisites
- Maven
---
## Setup
1. Download this template from the AnyPoint Exhchange at https://todo
2. Follow the guide at https://github.com/DriveTimeInc/AnypointStudio to configure Anypoint Studio to use MSSQL and Integrated Security.
3. Specify the `db.host` and `db.database` in `src/main/resources/environment.properties`. (If your `db.host` URI requires it, be sure use `/` and not `\`. Don't forget to escape it as `\\`.)
4. Modify the Database Connector to include a relevant query to your database.
