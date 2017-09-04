## Install the Application
### Verify Prerequisites

Requirement\ \ \ \ \ \ |Details|
------------ | ------------ |
**Operating System**|Windows 8.1<br>Windows 10<br>Windows Server 2012 R2<br>Windows Server 2016|
**SQL Server**|SQL Server 2014 (Express or better)<br>SQL Server 2016 (Express or better) [click here](SQL-Server-Setup.md) to install<br>Azure SQL Server and Database (Basic Pricing tier or better) [click here](Procure-a-SQL-Server-Database.md) to create a database|
**IIS with ASP.NET**|ASP.NET 4.5 (Express or better) [click here](Enable-IIS-and-NET-45.md) to verify or install|
**Information**|SQL Server / Database (host address and instance name)<br>Database Credentials (login and password, for a user with the db_owner Role on the Database)<br>Proxy Server (Server Address and Port, if required for outbound internet connectivity)<br>Name and Email Address|

### Install HivePro
1. Open the **Command Line** as Administrator
1. Navigate to the folder containing **HivePro.msi**
1. Run: `MSIEXEC /i HivePro.msi /l log.txt`
1. Accept the End-User License Agreement, then click **Next**
1. Enter the **SQL Server \ Instance** and **Database Name**
1. Select **Database** for the **Authentication Type**, then enter the **Login** and **Password**
1. Click **Test Connection**, then upon success, click **Next**
1. Optionally change the **Web Server Address** and **Application Pool** name, then click **Next**
1. Enter your **Name** and **Email Address**, then click **Next**
1. Optionally enter a **Proxy Server** and **Proxy Port** (only if hosted within a network that requires use of a Proxy Server for outbound internet connections), then click **Next**
1. Click **Next** to confirm all features will be installed to the default location
1. Click **Install**
1. Click **Finish**, which should then launch the website in the default browser
1. Login using the Email address specified during installation (default password: **administrator**)

---

Proceed to: [Add a Project](Add-a-Project.md)
<br>Back to: [Setup Procedures](README.md#setup-procedures)
