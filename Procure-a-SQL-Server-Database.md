## Create a SQL Server Database in Azure

### Create Database
1. Login to [https://portal.azure.com](https://portal.azure.com)
1. From the Resources panel on the left, click on **SQL databases**
1. Click **Add**
1. Enter a **Database name** (i.e. "hivepro")
<br>**_TAKE NOTE:_** The specified **Database name** will be used within the HivePro install process
1. For the **Resource group**, you may **Create new** or **Use existing**
1. For the **Server**, choose an existing Server, or **Create a new server**
1. For the **Pricing tier**, we recommend **Basic**
1. Click **Create**
1. Wait a few moments for the Azure deployment to complete, then refresh the **SQL databases** panel
1. Click on the database that was created
<br>**_TAKE NOTE:_** The **Server name** will be used within the HivePro install process

### Choose a Database User
Decide which of the following options you prefer for Database Credentials:
- You may use the SQL Server Administrator credentials for installing and running HivePro.  If you choose this option, no additional database administration is required; you may proceed directly to [Install HivePro](Install.md).
- You may create a new user specifically for HivePro and the database you created.  If you choose this option, proceed to [Create a Database User](Procure-a-SQL-Server-Database.md#create-a-database-user) below.

### Create a Database User
1. Using **SQL Server Management Studio**, login to the SQL Server as a user with permission to administer users and roles (i.e. sa)
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

---

Proceed to: [Install the Application](Install.md)
<br>Back to: [Setup Procedures](README.md#setup-procedures)
