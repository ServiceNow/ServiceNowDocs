---
title: Set up the Databricks spoke
description: Integrate your ServiceNow instance and the Databricks workspace by using an OAuth secret to authenticate the ServiceNow requests.Create an OAuth secret in Databricks workspace to authenticate the ServiceNow requests.Configure a connection to your Databricks workspace. The Databricks spoke connection and credential aliases use these connections to perform actions in the Databricks workspace.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Databricks Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Databricks spoke

Integrate your ServiceNow instance and the Databricks workspace by using an OAuth secret to authenticate the ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Databricks spoke.
-   Role required: admin.

## Create an OAuth secret in Databricks workspace

Create an OAuth secret in Databricks workspace to authenticate the ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the Databricks workspace as an admin.

2.  Click the user icon and click **Settings**.

3.  Under **Workspace admin**, click **Identity and access**.

4.  On the Identity and access page, for **Service principals** click **Manage**.

5.  On the Service principals page, click **Add service principal**.

6.  On the Add service principal form, click **Add new**.

7.  On the Add service principal form, select the **Databricks Managed** option and for **Service principal name**, enter a name to identify the record.

8.  Click **Add**.

    Service principal is added to the workspace and the list of service principals records is displayed.

9.  Click and open the service principal record you have created.

10. Click the **Secrets** tab.

11. Under **OAuth secrets**, click **Generate secret**.

12. On the Generate OAuth secret form, for **Lifetime \(days\)** enter the required number of days the secret should be valid for.

13. Click **Generate**.

    The values of **Secret** and **Client ID** are generated.

14. Copy the values of **Secret** and **Client ID** for later use and click **Done**.

15. Click the **Permissions** tab.

16. Click **Grant access**.

17. On the Grant access to others form, select **User, Group or Service principal** and **Permission** as per your requirement and click **Save**.


## Configure a connection for the Databricks spoke

Configure a connection to your Databricks workspace. The Databricks spoke connection and credential aliases use these connections to perform actions in the Databricks workspace.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Databricks** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Databricks spoke, click **View Details**.
    -   To manage more than one Databricks spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Name|Auto-generated name to identify the connection record.|
    |Connection URL|URL of the Databricks workspace.|
    |Credential Information|
    |OAuth Client ID|Client ID you created in the Databricks workspace.|
    |OAuth Client Secret|Key value you created in the Databricks workspace.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.|

6.  Click **Configure and Get OAuth Token**.


