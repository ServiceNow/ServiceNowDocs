---
title: Create a custom integration profile
description: Create a custom integration profile to track software subscriptions and optimize stale licenses for any SaaS application.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a custom integration profile

Create a custom integration profile to track software subscriptions and optimize stale licenses for any SaaS application.

## Before you begin

Before you create a custom integration profile in your ServiceNow instance, set up a method of authentication in the SaaS application admin or developer account. For example, create an OAuth application or an API token.

-   If you create an OAuth application, confirm that you enable the appropriate scopes. The app needs scopes to read users, read user activity, and to modify or delete users. These scopes enable the integration to get a list of users, get user activity, and reclaim unused subscriptions. Record the Client ID and Client secret for the OAuth application. You input these values in your ServiceNow instance.
-   If you create an API token, record the value for the API token. You input this value in your ServiceNow instance.

Role required: sam\_integrator

## About this task

If you’re using Software Asset Workspace, the option to create the custom integration profile in the Core UI is inactive.

## Procedure

1.  Navigate to the custom integration profile.

<table id="choicetable_mtv_n33_rcc"><thead><tr><th align="left" id="d160834e91">

Interface

</th><th align="left" id="d160834e94">

Action

</th></tr></thead><tbody><tr><td id="d160834e100">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **SaaS License** &gt; **Administration** &gt; **Create New Profile**.
2.  Select **Custom Integration Profile**.


</td></tr><tr><td id="d160834e136">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles** &gt; ****.
2.  Select **New**.
3.  Select **Custom** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_jf1_1jd_cjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the custom integration profile. For example, the name of the SaaS application that you're integrating with.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

1.  Select the lookup icon \(![Lookup icon](../../../common/image/List_SearchIcon.png)\).
2.  Select **New**.
3.  On the Connection and Credential Aliases form, fill in the fields:
    -   Name: Name of your choice. For example, *app*\_alias, where *app* is the name of the SaaS application that you're integrating with.
    -   Application: Spoke for connecting with the SaaS application. This spoke can be an existing Integration Hub spoke or a new spoke that you created. You can change the application in the Developer section of the System Settings ![Settings icon](../../../common/image/List_PersonalizeListIcon.png).
    -   Type: **Connection and Credential**.
    -   Connection Type: **HTTP**.
    -   Support Multiple Active Connections: Not selected.
    -   Default Retry Policy: **Default HTTP Retry Policy**.
    -   Configuration Template: If you're using the OAuth authorization code grant type, **OAuth Authorization Code**. If you're using an API token, **Basic Auth with API Key**. If you're using another authentication method, create a configuration template. For more information, see [Create a configuration template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-template.md) and [Configure a template for OAuth JWT Bearer grant type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/docusign-example.md).
4.  Select **Submit**.


</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. The options are **Draft** and **Published**. This value is automatically populated.

</td></tr><tr><td>

Profile type

</td><td>

Custom Integration. This value is automatically populated.

</td></tr></tbody>
</table>3.  Select **Save**.

4.  Open the Connection &amp; Credential alias record by selecting the preview icon ![](../image/preview-icon.png) and then selecting **Open Record**.

5.  Select the **Create New Connection &amp; Credential** related link.

    -   If you're using the OAuth Authorization Code configuration template, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Connection URL|Base URL for the API.|
        |Authorization URL|OAuth authorization code endpoint.|
        |Token URL|OAuth endpoint to retrieve and refresh access tokens.|
        |Token Revocation URL|OAuth endpoint to revoke access tokens.|
        |OAuth Redirect URL|`https://*instance*.service-now.com/oauth_redirect.do`, where *instance* is the name of your ServiceNow instance.|
        |Refresh Token Lifespan|**8640000**.|
        |OAuth Client ID|Client ID that you created in the SaaS application admin or developer account.|
        |OAuth Client Secret|Client secret that you created in the SaaS application admin or developer account.|
        |OAuth Scopes|Scopes that you enabled for your OAuth application in the SaaS application admin or developer account.|

    -   If you're using the Basic Auth with API Key configuration template, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Connection URL|URL for your SaaS account.|
        |User Name|Email address of the admin user that created the API token in the SaaS application admin or developer account.|
        |API Key|API token created in the SaaS application admin or developer account.|

    -   If you're using a different method of authentication, the available fields are determined by the configuration template that you created.
6.  Select **Create** and grant access for the integration.

    **Tip:** Log in to your SaaS application admin account in a new browser tab to verify that the integration connects to the correct account.

    -   If the connection is successful, a connection record is created in the Connections related list on the Connection &amp; Credential Alias record.
    -   If the connection fails, you must delete the connection record, credential record, and application registry record that were created during the attempted connection.
        1.  To delete the connection record, navigate to **Connections &amp; Credentials** &gt; **Connections** and delete the record for the SaaS application.
        2.  To delete the credential record, navigate to **Connections &amp; Credentials** &gt; **Credentials** and delete the record for the SaaS application.
        3.  To delete the application registry record, navigate to **System OAuth** &gt; **Application Registry** and delete the record for the SaaS application.
        4.  Return to the Connection &amp; Credential Alias record for the SaaS application and select the **Create New Connection &amp; Credential** related link to reattempt the connection.

## What to do next

[Create a data stream action to get users](create-data-stream-action-slc.md) and view SaaS related analytics on [SaaS overview dashboard](../reference/saas-dashboard-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](t_RunReconciliation.md) \(Software Asset Management classic application\) or the [License usage view](run-recon-workspace.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

