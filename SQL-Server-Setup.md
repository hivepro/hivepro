## SQL Server Installation and Configuration

An On-Premise SQL Server may be used for evaluation and testing purposes.  PowerBI integration is not supported with this option (though it may be enabled using the PowerBI Gateway, PowerBI Premium, and additional configuration of the provided PowerBI Template / Dashboards).

### Install SQL Server
1. Download [**SQL Server 2016 Express SP1**](http://www.microsoft.com/en-us/sql-server/sql-server-editions-express) (or better)
1. Proceed to install as directed (**Basic** installation with defaults are fine)

**OPTION:** When using the installation from media, some of the steps below can be completed during installation (starting SQL Server Browser automatically, Authentication, etc.); the procedures below are still recommended to confirm their configuration.

### Configure SQL Server to Accept Remote Connections
1. Open **SQL Server Configuration Manager**
1. Expand to: **SQL Server Network Configuration \ Protocols for SQLEXPRESS**
1. Enable: **Named Pipes**
1. Enable: **TCP/IP**
1. Right-click on **TCP/IP**, then click **Properties**
1. Select the **IP Addresses** tab
1. Under **IPAll**, for **TCP Dynamic Ports**, enter **1433**
1. Expand to: **SQL Server Services**
1. Right-click **SQL Server**, then click **Stop**
1. Right-click **SQL Server**, then click **Start**
1. Right-click: **SQL Server Browser**, then click **Start**
1. Right-click: **SQL Server Browser**, then click **Properties**
1. Select the **Service** tab
1. For **Start Mode**, select **Automatic**

### Enable SQL Server Management Studio
##### OPTION A: Install SQL Server Management Studio:
1. Download [**SQL Server Management Studio**](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms)
1. Proceed to install as directed

##### OPTION B: Enable Windows Authentication from a Remote Connection
1. From a different machine on the same network as the SQL Server (with SSMS already installed)
1. Open **Credential Manager**
1. Under **Windows Credentials**, click **Add a Windows credential**
1. For **Internet or network address**, enter: \<IP\>:1433 where \<IP\> is the SQL Server address, within the internal (or otherwise accessible) network
1. For **User name**, enter \<HostName\>\\\<Username\> of a user with administrative permissions through Windows Authentication on the machine with the SQL Server
1. For **Password**, enter the password for that user on that host
1. Click **OK**

### Enable SQL Server Authentication
1. Open **SQL Server Management Studio**
1. Connect to the **Database Engine** using **Windows Authentication**
1. Right-click on the Server, then click **Properties**
1. Select **Security** from the list of pages on the left
1. Select **SQL Server and Windows Authentication mode**
1. Click **OK**

---

Back to: [Install the Application](Install.md#install-the-application)
