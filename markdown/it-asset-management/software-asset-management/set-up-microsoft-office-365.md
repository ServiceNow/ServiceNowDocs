---
title: Create a Microsoft 365 integration profile
description: Create an integration profile to track software subscriptions and optimize stale licenses for the Microsoft 365 service.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a Microsoft 365 integration profile

Create an integration profile to track software subscriptions and optimize stale licenses for the Microsoft 365 service.

## Before you begin

ServiceNow Role required: sam\_integrator or admin

To integrate with Microsoft 365, activate the following plugins:

-   Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin
-   Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin from the [ServiceNow Store](https://store.servicenow.com/)

    For more information, see [Request SaaS License Management](request-saas-license-management.md).


## About this task

If you’re using Software Asset Workspace, the option to create the direct integration profile in Core UI is inactive.

## Procedure

1.  From a web browser, open your ServiceNow instance.

<table id="choicetable_w41_4c4_2cc"><thead><tr><th align="left" id="d325435e127">

Interface

</th><th align="left" id="d325435e130">

Action

</th></tr></thead><tbody><tr><td id="d325435e136">

**Core UI**

</td><td>

Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**

</td></tr><tr><td id="d325435e159">

**Software Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations**.
2.  Under **User subscription**, select **Direct integration profiles**.


</td></tr></tbody>
</table>2.  Select **New**.

3.  Select **Microsoft 365 Integration Profile**.

4.  On the form, fill in the fields.

<table id="table_e5p_q3w_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `Microsoft 365 integration for <*your-company*>`.

</td></tr><tr><td>

Client Id

</td><td>

Client ID of the application that you registered in the Microsoft Azure portal. Enter the application \(client\) ID that you copied in [Register a Microsoft Entra ID application](register-microsoft-app.md).

</td></tr><tr><td>

Client secret

</td><td>

Client secret of the application that you registered in the Microsoft Azure portal. Enter the client secret that you copied in [Register a Microsoft Entra ID application](register-microsoft-app.md).

</td></tr><tr><td>

Tenant name or Id

</td><td>

Globally unique identifier \(GUID\) of the application that you registered in the Microsoft Azure portal. Enter the directory \(tenant\) ID that you copied in [Register a Microsoft Entra ID application](register-microsoft-app.md).**Warning:** When entering the directory \(tenant\) ID, don’t add any additional extensions to the ID. Enter the ID exactly as it was copied in [Register a Microsoft Entra ID application](register-microsoft-app.md).

</td></tr><tr><td>

REST message

</td><td>

Message that enables you to send requests to a REST web service endpoint.

</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **Microsoft 365**.

</td></tr><tr><td>

Permission type

</td><td>

The type of permission for the integration profile to access data correctly and securely.Values include:

-   **Application**: Permissions that enable the application to access any data without a signed-in user.
-   **Delegated**: Permissions that enable the application to act in place of a signed-in user.


</td></tr></tbody>
</table>5.  In the Process configuration section, view the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see [Minimal user permissions](../concept/integrate-with-microsoft.md) table.

    -   The **Download subscriptions** check box is selected by default and you can't clear it.
    -   The **Download Activity** check box is selected by default. If you clear it, activity data for this integration profile isn't pulled.
    -   The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

6.  Select **Submit**.

7.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    If the connection is successfully validated, the integration profile downloads subscriptions and activity data.

    **Note:** If the **Download Activity** field is selected without configuring the optional Power BI settings, the Validate connection feature will issue the following warning message: "All required APIs are validated successfully, but the optional Power BI API validation has failed."

8.  Check the status of the user subscription job by navigating to **Software Asset** &gt; **Administration** &gt; **Job Results**.


## What to do next

View all automatically generated software models for Microsoft 365 by navigating to **Integration - Microsoft 365** &gt; **Software Models**. A software model is a profile of the software that you have purchased, including information about the publisher, version, and discovery map. Software models record publisher information and create a profile.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select a Microsoft 365 integration profile to view the following related lists:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](../concept/subscription-exclusions.md#).

When you create an integration profile, a reclamation rule is automatically created for the software. It's important that you review the reclamation rule to ensure that it meets your specifications. You can view all automatically generated reclamation rules for Office 365 by navigating to **Software Asset** &gt; **Administration** &gt; **Reclamation Rules**. Reclamation rules are applied based on the Microsoft System Center Configuration Management \(SCCM\) usage data that is pulled through the Microsoft SCCM usage integration. For more information on these reclamation rules, see [Create a reclamation rule to import Microsoft SCCM usage data](create-reclamation-rule-sccm.md).

**Note:** ServiceNow automatically creates one default reclamation rule for Office 365. You can also update the Last activity threshold field under the Subscription Usage Condition tab.

**Related topics**  


[Review a software reclamation rule](add-reclamation-rule-sub.md)

[Reclamation rules for Microsoft 365 integration](../reference/m365-reclamation-rules.md)

[Software Asset Management software suites](../concept/software-suites.md)

