### How it works
Follow the step-by-step instructions to setup the application On-Premises, connected to a SQL Database in Azure.  This provides a basic Web Application for configuration, and a Windows Service for automated data collection for the tools and projects that you choose. At a specified frequency, the Service will collect the data from those tools, and store it to your database (no need for additional gateways or connectivity configuration).

### Setup
- [SQL Server Setup](SQL-Server-Setup)
- <a href="mailto:admin@hiveapps.io?subject=HivePro: Evaluation Request&body=Please sent me a link to download the HivePro Installer.">Download</a>
- [Install](Install.md)
  - [Prerequisites](Install.md#prerequisites)
  - [Create Database](Install.md#create-database)
  - [Create Login](Install.md#create-login)
  - [Grant ownership of the Database to a Login](Install.md#grant-ownership-of-the-database-to-a-login)
  - [Enable IIS and .NET 4.5](Install.md#enable-iis-and-net-45)
  - [Install HivePro](Install.md#install-hivepro)
  - [Add a Project](Install.md#add-a-project)
  - [Add an Integration](Install.md#add-an-integration)
  - [Verify Data Feed](Install.md#verify-data-feed)
- [Publish PowerBI Dashboard](Publish-PowerBI-Dashboard.md)

---

### Supported Integrations / Data
- **GitHub**
  - Commits
  - Repositories
- **JIRA**
  - IssueActivity
  - Issues
  - Status
  - Users
- **PivotalTracker**
  - Members
  - Projects
  - Stories
  - StoryActivity
  - StoryComments
  - StoryLabels
  - Tasks
- **TeamCity**
  - Builds
  - BuildStatistics
- **Jenkins**
  - CodeCoverage
  - Runs

---

- [License](License.md)
