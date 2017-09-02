### Install SQL Server
- Download [**SQL Server 2016 Express SP1**](http://www.microsoft.com/en-us/sql-server/sql-server-editions-express) (or better)
- Proceed to install as directed (**Basic** installation with defaults are fine)

**OPTION:** When using the installation from media, some of the steps below can be completed during installation (starting SQL Server Browser automatically, Authentication, etc.); the procedures below are still recommended to confirm their configuration.

### Configure SQL Server to Accept Remote Connections
- Open **SQL Server Configuration Manager**
- Expand to: **SQL Server Network Configuration \ Protocols for SQLEXPRESS**
- Enable: **Named Pipes**
- Enable: **TCP/IP**
- Right-click on **TCP/IP**, then click **Properties**
- Select the **IP Addresses** tab
- Under **IPAll**, for **TCP Dynamic Ports**, enter **1433**
- Expand to: **SQL Server Services**
- Right-click **SQL Server**, then click **Stop**
- Right-click **SQL Server**, then click **Start**
- Right-click: **SQL Server Browser**, then click **Start**
- Right-click: **SQL Server Browser**, then click **Properties**
- Select the **Service** tab
- For **Start Mode**, select **Automatic**

### Enable SQL Server Management Studio
##### OPTION A: Install SQL Server Management Studio:
- Download [**SQL Server Management Studio**](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms)
- Proceed to install as directed

##### OPTION B: Enable Windows Authentication from a Remote Connection
- From a different machine on the same network as the SQL Server (with SSMS already installed)
- Open **Credential Manager**
- Under **Windows Credentials**, click **Add a Windows credential**
- For **Internet or network address**, enter: \<IP\>:1433 where \<IP\> is the SQL Server address, within the internal (or otherwise accessible) network
- For **User name**, enter \<HostName\>\\\<Username\> of a user with administrative permissions through Windows Authentication on the machine with the SQL Server
- For **Password**, enter the password for that user on that host
- Click **OK**

### Enable SQL Server Authentication
- Open **SQL Server Management Studio**
- Connect to the **Database Engine** using **Windows Authentication**
- Right-click on the Server, then click **Properties**
- Select **Security** from the list of pages on the left
- Select **SQL Server and Windows Authentication mode**
- Click **OK**
