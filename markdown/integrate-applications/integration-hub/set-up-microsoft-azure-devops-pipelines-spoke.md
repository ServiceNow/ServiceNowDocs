---
title: Set up Microsoft Azure DevOps Pipelines spoke
description: Integrate your ServiceNow instance and Azure DevOps Pipelines application by setting up a connection record.Configure the default connection record for your Azure DevOps Pipelines application that enables integration of your ServiceNow instance with the Azure DevOps Pipelines application. Specify whether the record is for a host, instance, custom application, or account.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure DevOps Pipelines Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up Microsoft Azure DevOps Pipelines spoke

Integrate your ServiceNow instance and Azure DevOps Pipelines application by setting up a connection record.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Azure DevOps Pipelines spoke.
-   Role required: admin.

## Configure the default connection record

Configure the default connection record for your Azure DevOps Pipelines application that enables integration of your ServiceNow instance with the Azure DevOps Pipelines application.

### Before you begin

Role required: admin

### Procedure

1.  Create a personal access token in Azure DevOps portal.

    Azure DevOps application authenticates the ServiceNow instance access request based on the personal access token presented.

    1.  Log in to Azure DevOps portal.

    2.  On the landing page, select the User Settings icon \(![User Settings icon.](../image/ms-aure-devops-pipeline-usr-settings-icon.png)\).

    3.  In the menu, select **Personal access tokens**.

    4.  On the Personal Access Tokens page, select **+ New Token**.

    5.  Fill the Create a new personal access token form.

<table id="table_acd_43n_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Custom name of the personal access token.

</td></tr><tr><td>

Organization

</td><td>

It contains all the resources and settings related to the DevOps pipeline and project management.**Tip:** To locate the name of the organization, navigate to the home page of the DevOps Pipeline application. The name of the organization is provided above the Projects tab.

</td></tr><tr><td>

Expiration \(UTC\)

</td><td>

Expiration date of the personal access token.

</td></tr><tr><td>

Scopes

</td><td>

Resources or settings in Azure DevOps Pipelines application that you can access with the personal access token. Select Custom defined and under the Build section, select Read &amp; execute.

</td></tr></tbody>
</table>    6.  Select **Create**.

    7.  To copy the personal access token, click the Copy to clipboard button.

        ![Copy to clipboard button.](../image/ms-azure-devops-pipeline-copy-access-token.png)

    8.  Select **Close**.

2.  Configure the default connection record in your ServiceNow instance.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    3.  Click the **Integrations** tab.

    4.  Select **Connections**.

    5.  In the Search all connections field, enter `Microsoft Azure DevOps Pipelines`.

    6.  In the Microsoft Azure DevOps Pipelines card, click **View Details**.

    7.  Click **Configure**.

        ![Configure button.](../image/ms-azure-devops-pipelines-configure-button.png)

    8.  Fill the form.

<table id="table_tfb_vpn_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection record. The default and read-only name of the first connection is Microsoft Azure DevOps Pipelines.**Note:** To provide a custom name of a connection, you must create a connection record. To create, select **Add Connection**.

</td></tr><tr><td>

Connection URL

</td><td>

URL to the Azure DevOps Pipelines application. The URL format is `https://dev.azure.com/<organization>`. Replace the placeholder &lt;organization&gt; with the organization name in the Azure DevOps Pipelines application.

**Tip:** You can find the organization name under the Organization column of the Personal Access Tokens page.

</td></tr><tr><td>

Personal Access Token

</td><td>

Enter the personal access token you had created.

</td></tr></tbody>
</table>    9.  Select **Configure Connection**.

        The connection record is created.

        ![Connection record created.](../image/ms-azure-devops-pipelines-conn-created.png)


