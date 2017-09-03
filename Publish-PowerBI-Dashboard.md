---
title: Publish PowerBI Dashboard
layout: default
---
# Publish PowerBI Dashboard

- Download **Hive.DataSource.xml**, and save to the root of your C:\
- Download **Template.pbix**
- Open **Template.pbix** using PowerBI Desktop
- Click **Refresh**
- Within the **SQL Server database** dialog, select the **Database** tab
- Enter the **Username** and **Password** used to Install HivePro, then click **Connect**
- Within the **Privacy levels** dialog, select **Orgainizational** for both **C:\\** and the SQL Server, then click **Save**
- Wait for the Refresh process to complete
- Click **Publish**

**_NOTE:_** Template.pbix contains Queries for the data in Tables collected for configured Integrations, but it does not contain any Reports.
