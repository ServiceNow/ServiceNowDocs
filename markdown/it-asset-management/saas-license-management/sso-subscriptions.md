---
title: Viewing SSO subscription information
description: You can view information about the Single Sign-On \(SSO\) applications, SSO users, and SSO groups that are associated with your SSO integrations.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Viewing your SaaS and SSO subscriptions, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Viewing SSO subscription information

You can view information about the Single Sign-On \(SSO\) applications, SSO users, and SSO groups that are associated with your SSO integrations.

**Important:** You can view information about your SSO applications, users, and groups in both the Software Asset Management Core UI and Software Asset Workspace. The following sections provide details on viewing this information in the Software Asset Management classic application. For details on viewing this information in the Software Asset Workspace, see [License operations view](../concept/operations-workspace.md).

## Viewing SSO integration information

To view the applications, users, and groups for an SSO integration, navigate to **All** &gt; **SaaS License** &gt; **Administration** &gt; **SSO Integration Profiles** and then select a profile. The related lists provide information about the integration.

<table id="table_ut4_dyj_wlb"><thead><tr><th>

List

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SSO Applications

</td><td>

All SSO applications.

</td></tr><tr><td>

Directory Users

</td><td>

All SSO users.

</td></tr><tr><td>

Directory Groups

</td><td>

All SSO groups.

</td></tr><tr><td>

Scheduled Jobs

</td><td>

**SAM - SSO &lt;sso-provider&gt; download applications** scheduled job that downloads all SSO apps. The job runs when the SSO integration profile is published, and then runs daily.The **SAM - SSO &lt;sso-provider&gt; update connected applications** scheduled job downloads users, groups, and subscriptions for SSO apps. The job runs daily and whenever an app is connected.

</td></tr><tr><td>

Scheduled Job Results

</td><td>

Status of the scheduled jobs.

</td></tr><tr><td>

Directory Jobs

</td><td>

The **&lt;sso-provider&gt; - Download Group Membership** directory job that downloads group memberships for all users. The job runs when the SSO integration profile is published, and then runs daily.

 The **&lt;sso-provider&gt; - Download Users** directory job downloads all users. The job runs when the SSO integration profile is published, and then runs daily.

 The **&lt;sso-provider&gt; - Download Groups** directory job downloads all groups for all users. The job runs when the SSO integration profile is published, and then runs daily.

 **Note:** On upgrading to Microsoft Entra ID spoke 4.3 version, the **Microsoft Azure AD - Download Group Membership** directory job won’t be executed for existing Microsoft Entra ID SSO or Directory integrations. This directory job also won’t be created for new Microsoft Entra ID SSO or Directory integrations. Instead, the **Microsoft Azure AD - Download Groups** directory job downloads all groups and group memberships configured on Microsoft Entra ID.

</td></tr><tr><td>

Directory Job Results

</td><td>

Status of the directory jobs.

</td></tr></tbody>
</table>## Viewing SSO application information

To view the users, groups, and reclamation candidates for an application, navigate to **All** &gt; **SaaS License** &gt; **SSO Applications** and select an application. The related lists show information for the application. For viewing the SSO application information in Software Asset Workspace, see [View SSO applications in workspace](../task/view-ssoapps-workspace.md).

<table id="id_acl_q5h_bzb"><thead><tr><th>

List

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SSO Application Users

</td><td>

All users that have direct access to the application, but not through membership in a group.

</td></tr><tr><td>

SSO Application Groups

</td><td>

All groups that have access to the application.

</td></tr><tr><td>

SSO Subscriptions

</td><td>

Total number of subscriptions for the application. A user may have both direct access to an app and have access through a group. But the user's access counts as only one subscription so as only one record in the SSO Subscriptions list.**Note:**

-   Add the **SSO application role** column to see how the user is granted access to the application. If the value is a group, then the user has access through membership in that group. If the value is the user's name, then the user has direct access to the application. User subscriptions can't be reclaimed in Software Asset Management if the user has access to the application through a group membership. To reclaim the subscription, remove the user from the group in the Azure AD portal and set the reclamation candidate state to **Closed Complete**.
-   When SSO subscriptions are created through SSO application groups, the **Subscription assigned** value is empty. When the subscriptions are created through SSO Application Users, the **Subscription assigned** value shows the date of when the subscription is assigned to the user. After you upgrade to the Software Asset Management - SaaS License Management 13.1.0 version or later, the existing **Subscription assigned** values for the subscriptions that were created through SSO application groups turns empty.

</td></tr><tr><td>

Reclamation Candidates

</td><td>

Subscriptions that don't meet the usage requirements that are defined by the reclamation rule for the application.

</td></tr></tbody>
</table>## Data synchronization with SSO providers

If you delete a user, group, or app in the Azure AD portal or in the Okta Developer Console, then the corresponding records in Software Asset Management are deleted when the daily scheduled jobs run. If you revoke a user's access to an application in the Azure AD portal or in the Okta Developer Console, either directly or indirectly by removing them from a group, then the corresponding user subscription record is deleted when the daily scheduled jobs run.

**Parent Topic:**[Viewing your SaaS and SSO subscriptions](../concept/usage-summary-saas.md)

