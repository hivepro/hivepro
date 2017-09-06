---
layout: default
title: Home
---

## How it works
Follow the step-by-step instructions to setup the application, connecting to a SQL Database hosted in Azure.  This provides a Web Application for configuration, and a Windows Service for automated data collection for the tools and projects that you choose.  At a specified frequency, the Service will collect the data from those tools, and store it to your database (there is no need for additional gateways or connectivity configuration).  Then download a PowerBI Dashboard template to build and publish reports.

This application, including all communications and data, is maintained within your network (it does not transmit data externally).

## Setup Procedures
1. [Download the Installer](https://hivepro.github.io/Download/HivePro.msi) (2 min)
1. [Create a SQL Server Database in Azure](Procure-a-SQL-Server-Database.md#create-a-sql-server-database-in-azure) (10 min)
1. [Install the Application](Install.md#install-the-application) (5 min)
1. [Add a Project](Add-a-Project.md#add-a-project) (1 min)
1. [Configure Integrations](Configure-Integrations.md#configure-integrations) (3 min / each)
1. [Publish a PowerBI Dashboard](Publish-PowerBI-Dashboard.md#publish-powerbi-dashboard) (5 min)

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
For more information, or to request a [License](License.md) extension, email: <a href="mailto:admin@hiveapps.io?subject=HivePro">admin@hiveapps.io</a>
