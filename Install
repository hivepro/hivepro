### Prerequisites

Requirement|Details|
------------ | ------------ |
**Operating System**|Windows 8.1<br>Windows 10<br>Windows Server 2012 R2<br>Windows Server 2016|
**SQL Server**|SQL Server 2014 (Express or better)<br>SQL Server 2016 (Express or better)|
**Information**|SQL Server / Instance (host address and instance name)<br>SQL Server Credentials for Server Administrator<br>Proxy Server (Server Address and Port, if required for outbound internet connectivity)<br>Name and Email Address|

**REFERENCE:** [**SQL Server Setup**](https://github.com/dmellenthin/Hive/wiki/SQL-Server-Setup) for instructions to install and configure **SQL Server** and **SQL Server Management Studio**.  If the database will be hosted in Azure, use the Server Administrator credentials with an instance of **SQL Server Management Studio** (on any machine), to proceed with the processes below.

### Create Database
- Open **SQL Server Management Studio**
- Connect to the **Database Engine** using authentication for a Server Administrator
- Right click on **Databases** (under the Server), then click **New Database**
- Enter a **Database name**
- Click **OK**

**OPTION:** The Server Administrator credentials may be used to **Install HivePro**, and skip **Create Login** and **Grant ownership of the Database to a Login**; this is not recommended (outside of internal testing purposes).

### Create Login
- Open **SQL Server Management Studio**
- Connect to the **Database Engine** using authentication for a Server Administrator
- Expand to **Server \ Security \ Logins**
- Right-click on the **Logins**, then click **New Login**
- Within the **General** page
  - Enter a **Login name**
  - Select **SQL Server authentication**
  - Enter a **Password** and **Confirm password**
  - Uncheck: **Enforce password policy**
- Click **OK**

### Grant ownership of the Database to a Login
- Open **SQL Server Management Studio**
- Connect to the **Database Engine** using authentication for a Server Administrator
- Expand to **Server \ Security \ Logins**
- Right-click on the Login that will be used for administration of the database, then click **Properties**
- Select the **User Mapping** page
- Check the database under **Users mapped to this login**
- Check: **db_owner** under **Database role membership for: \<database\>**
- Click **OK**

### Enable IIS and .NET 4.5
- Open **Windows Features** on the machine that will host the **HivePro** website
- Check: **Internet Information Services** (you may leave all sub-features default)
- Check: **Internet Information Services \ World Wide Web Services \ Application Development Features \ ASP.NET 4.5** (which also checks dependencies within **Application Development Features**)
- Check: **.NET Framework 4.5 Advanced Services \ ASP.NET 4.5**
- Click **OK**

### Install HivePro
- Download the installer under **Artifacts** from the latest build in [TeamCity](http://104.214.105.174:8090/viewType.html?buildTypeId=HivePro_Build)
- Open the **Command Line** as Administrator
- Navigate to the folder containing **HivePro.msi**
- Run: `MSIEXEC /i HivePro.msi /l log.txt`
- Accept the End-User License Agreement, then click **Next**
- Enter the **SQL Server \ Instance**, **Database Name**, and Credentials, click **Test Connection**, then click **Next**
- Optionally change the **Web Server Address** and **Application Pool** name, then click **Next**
- Enter your **Name** and **Email Address**, then click **Next**
- Optionally enter a **Proxy Server** and **Proxy Port** (only if hosted within a network that requires use of a Proxy Server for outbound internet connections), then click **Next**
- Click **Next** to confirm all features will be installed to the default location
- Click **Install**
- Click **Finish**, which should then launch the website in the default browser
- Login using the Email address specified during installation (default password: **administrator**)

### Add a Project
- Within the **Projects** page, click **Add Project**
- Enter a **Name**
- Click **Submit**

### Add an Integration
- Within the Project Details page, click **Add Project**
- Select the **Type** (i.e. **ProjectManagement**)
- Select the **Product** (i.e. **JIRA**)
- Enter the **Server URL** (i.e. **https://hiveapps.atlassian.net**)
- Enter the **ProjectKey** (i.e. **JIRADemo**)
- Enter the **Username**
- Enter the **Password**

### Verify Data Feed
- Open **SQL Server Management Studio**
- Connect to the **Database Engine**
- Verify the records (or record count) resembles the data within that Product / Project using a **New Query** targeting the database, with a query below:
  - **JIRA:** `SELECT * FROM Jira.Issues`
