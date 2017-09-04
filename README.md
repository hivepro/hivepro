## How it works
Follow the step-by-step instructions to setup the application, connecting to a SQL Database hosted in Azure.  This provides a Web Application for configuration, and a Windows Service for automated data collection for the tools and projects that you choose.  At a specified frequency, the Service will collect the data from those tools, and store it to your database (there is no need for additional gateways or connectivity configuration).  Then download a PowerBI Dashboard template to build and publish reports.

This application, including all data and communication, is maintained within your network (it does not transmit data externally).

## Setup Procedures
1. <a href="mailto:admin@hiveapps.io?subject=HivePro: Evaluation Request&body=Please sent me a link to download the HivePro Installer.">Download the Installer</a>
1. [Procure a SQL Server Database](Procure-a-SQL-Server-Database.md)
1. [Install the Application](Install.md)
1. [Add a Project](Add-a-Project.md)
1. [Configure Integrations](Configure-Integrations.md)
1. [Publish a PowerBI Dashboard](Publish-PowerBI-Dashboard.md)

## Supported Integrations

Product|Hosting Options|
------ | ------------- |
**GitHub**|On-Premise or github.com|
**JIRA**|On-Premise or JIRA Cloud|
**PivotalTracker**|pivotaltracker.com|
**TeamCity**|On-Premise|
**Jenkins**|On-Premise|

For more info about these Integrations: [click here](Supported-Integrations.md)

---
