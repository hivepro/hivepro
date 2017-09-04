## Configure Integrations

Within the Project Details page for a Project within the HivePro Web Application, you may optionally add any number of Integrations to HivePro Projects.

**_NOTE:_** You may add multiple Third-Party Projects of the same Product to a HivePro Project, and the same Third-Party Projects may be associated with any number of HivePro Projects.

### GitHub
1. Click **Add Integration**
1. For **Type**, select **SourceControl**
1. For **Product**, select **GitHub**
1. Enter the **Server URL** (hostname / IP, and port if applicable; or "https://github.com")
1. Enter the **Owner**
1. Enter the **Repo**
1. Enter the **Username** (to be used for read operations)
1. Enter the **Password**
1. Click **Save**

### JIRA
1. Click **Add Integration**
1. For **Type**, select **ProjectManagement**
1. For **Product**, select **JIRA**
1. Enter the **Server URL** (hostname / IP, and port if applicable; or JIRA Cloud site URL)
1. Enter the **ProjectKey**
1. Enter the **Username** (to be used for read operations)
1. Enter the **Password**
1. Click **Save**

### PivotalTracker
1. Click **Add Integration**
1. For **Type**, select **ProjectManagement**
1. For **Product**, select **PivotalTracker**
1. Enter the **ProjectID**
1. Enter the **ApiToken** (to be used for read operations)
1. Click **Save**

### Jenkins
1. Click **Add Integration**
1. For **Type**, select **ContinuousIntegration**
1. For **Product**, select **Jenkins**
1. Enter the **Server URL** (hostname / IP, and port if applicable)
1. Enter the **JobID**
1. Enter the **RepositoryID** (if job class is **jenkins.branch.OrganizationFolder**)
1. Enter the **BranchID** (if job class is **jenkins.branch.OrganizationFolder**)
1. Enter the **Username** (to be used for read operations)
1. Enter the **Password**
1. Click **Save**

### TeamCity
1. Click **Add Integration**
1. For **Type**, select **ContinuousIntegration**
1. For **Product**, select **TeamCity**
1. Enter the **Server URL** (hostname / IP, and port if applicable)
1. Enter the **ProjectID**
1. Enter the **BuildTypeID**
1. Enter the **Username** (to be used for read operations)
1. Enter the **Password**
1. Click **Save**

Back to: [Setup Procedures](README.md#setup-procedures)
