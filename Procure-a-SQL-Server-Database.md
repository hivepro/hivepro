## Procure a SQL Server Database

### Create SQL Database
1. Login to https://portal.azure.com
2. From the Resources list on the left panel, click on **SQL databases**
3. Click **Add**
4. Enter a **Database name**, such as "hivepro", and take note of this entry (this will be used within the HivePro install process)
5. For the **Resource group**, you may **Create new** or **Use existing**
6. For the **Server**, choose an existing Server, or **Create a new server**
7. For the **Pricing tier**, we recommend you choose **Basic**
8. Click **Create**
9. Wait a few moments for the Azure deployment to complete, then refresh the **SQL databases** panel
10. Click on the database that was created
11. Take note of the **Server name** (this will be used within the HivePro install process)

### Decide on Authentication / Security
- You may use the SQL Server Administrator credentials for installing and running HivePro.  If you choose this option, proceed directly to [HivePro Installation](install.md).
- You may create a new user specifically for HivePro and the database you created.  If you choose this option, proceed to [Create User](Procure-a-SQL-Server-Database.md#Create-User)

### Create User
1. From the SQL database Overview panel, click on **Tools**
2. Click on **Query editor (preview)**
<br>**_NOTE:_** You may need to agree to the **Preview terms**
3. Click **Login**
4. Proceed to login as a user with permission to administer users and permissions on the SQL Server
