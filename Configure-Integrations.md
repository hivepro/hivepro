## Configure Integrations

Within the Project Details page for a Project within the HivePro Web Application, you may optionally add any number of Integrations to HivePro Projects.

**_NOTE:_** You may add multiple Third-Party Projects of the same Product to a HivePro Project, and the same Third-Party Projects may be associated with any number of HivePro Projects.

### GitHub
- Click **Add Integration**
- For **Type**, select **SourceControl**
- For **Product**, select **GitHub**
- Enter the **Server URL** (hostname / IP, and port if applicable; or "https://github.com")
- Enter the **Owner**
- Enter the **Repo**
- Enter the **Username** (to be used for read operations)
- Enter the **Password**
- Click **Save**

### JIRA
- Click **Add Integration**
- For **Type**, select **ProjectManagement**
- For **Product**, select **JIRA**
- Enter the **Server URL** (hostname / IP, and port if applicable; or JIRA Cloud site URL)
- Enter the **ProjectKey**
- Enter the **Username** (to be used for read operations)
- Enter the **Password**
- Click **Save**

### PivotalTracker
- Click **Add Integration**
- For **Type**, select **ProjectManagement**
- For **Product**, select **PivotalTracker**
- Enter the **ProjectID**
- Enter the **ApiToken** (to be used for read operations)
- Click **Save**

### Jenkins
- Click **Add Integration**
- For **Type**, select **ContinuousIntegration**
- For **Product**, select **Jenkins**
- Enter the **Server URL** (hostname / IP, and port if applicable)
- Enter the **JobID**
- Enter the **RepositoryID** (if job class is **jenkins.branch.OrganizationFolder**)
- Enter the **BranchID** (if job class is **jenkins.branch.OrganizationFolder**)
- Enter the **Username** (to be used for read operations)
- Enter the **Password**
- Click **Save**

### TeamCity
- Click **Add Integration**
- For **Type**, select **ContinuousIntegration**
- For **Product**, select **TeamCity**
- Enter the **Server URL** (hostname / IP, and port if applicable)
- Enter the **ProjectID**
- Enter the **BuildTypeID**
- Enter the **Username** (to be used for read operations)
- Enter the **Password**
- Click **Save**
