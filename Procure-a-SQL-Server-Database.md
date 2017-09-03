## Procure a SQL Server Database

### Create Database
1. Login to https://portal.azure.com
1. From the Resources panel on the left, click on **SQL databases**
1. Click **Add**
1. Enter a **Database name** (i.e. "hivepro")
<br>**_TAKE NOTE:_** The specified **Database name** will be used within the HivePro install process
1. For the **Resource group**, you may **Create new** or **Use existing**
1. For the **Server**, choose an existing Server, or **Create a new server**
1. For the **Pricing tier**, we recommend you choose **Basic**
1. Click **Create**
1. Wait a few moments for the Azure deployment to complete, then refresh the **SQL databases** panel
1. Click on the database that was created
<br>**_TAKE NOTE:_** The **Server name** will be used within the HivePro install process

### Choose a Database User
- You may use the SQL Server Administrator credentials for installing and running HivePro.  If you choose this option, no additional database administration is required; you may proceed directly to [Install HivePro](Install.md).
- You may create a new user specifically for HivePro and the database you created.  If you choose this option, proceed to [Create a Database User](Procure-a-SQL-Server-Database.md#Create-a-Database-User) below.

### Create a Database User
1. Using SSMS, login as a user with permission to administer users and permissions on the SQL Server (i.e. sa)
1. From the main menu, click **File \> New \> Query with Current Connection**
1. Choose **master** from the **Available databases** drop-down
1. In the **Query Editor** window, enter and execute:
<br>`CREATE LOGIN hivepro WITH password='Pa55word!';`
<br>**_TAKE NOTE:_** The **login** and **password** will be used within the HivePro install process (these can/should deviate from the example above)
1. Choose \<database name\> from the **Available databases** drop-down (using the database that was created for HivePro)
1. In the **Query Editor** window, enter and execute:
<br>`CREATE USER hivepro FROM LOGIN hivepro;`
1. In the **Query Editor** window, enter and execute:
<br>`EXEC sp_addrolemember 'db_owner', 'hivepro';`