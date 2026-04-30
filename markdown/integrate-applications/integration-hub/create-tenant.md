---
title: Define Microsoft SharePoint Online tenants
description: Define a profile for your Microsoft SharePoint Online tenant site. The Microsoft SharePoint Online spoke uses the tenant record and associated Connection and Credential alias to perform actions on Microsoft SharePoint Online.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft SharePoint Online Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Define Microsoft SharePoint Online tenants

Define a profile for your Microsoft SharePoint Online tenant site. The Microsoft SharePoint Online spoke uses the tenant record and associated Connection and Credential alias to perform actions on Microsoft SharePoint Online.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **Microsoft Sharepoint Online** &gt; **Tenants**.

2.  Click **New**.

3.  Complete the form.

<table id="table_wt3_1fd_4gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the tenant.

</td></tr><tr><td>

Alias

</td><td>

Select a connection and credential alias. If configuring the integration for a single tenant, select the **MicrosoftSharepointOnline** alias. If configuring the integration for multiple tenants, select the desired alias.

</td></tr><tr><td>

Sharepoint Root URL

</td><td>

Enter the root SharePoint URL without the https:// prefix.For example, `<SiteName>.sharepoint.com`

</td></tr><tr><td>

Tenant Id

</td><td>

Enter the Tenant ID. This is the Directory ID for the Azure AD Directory that is supporting the Microsoft SharePoint Online tenant you want to connect to. See [Configure OAuth application in Microsoft Azure](configure-oauth-application-in-microsoft-azure.md).

</td></tr><tr><td>

Resource Id

</td><td>

Auto-populated with **00000003-0000-0ff1-ce00-000000000000**.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

If configuring an integration with multiple Microsoft SharePoint Online tenants, create additional tenant profiles as needed.

