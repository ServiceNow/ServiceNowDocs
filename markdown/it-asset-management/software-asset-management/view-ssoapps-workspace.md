---
title: View SSO applications in workspace
description: View details related to applications that you can connect through a SSO provider in the Software Asset Workspace.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View SSO applications in workspace

View details related to applications that you can connect through a SSO provider in the Software Asset Workspace.

## Before you begin

Role required: sam\_admin or sam\_user

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select **SSO applications**.

    List of all connected and disconnected SSO applications is shown.

3.  Select a application record to view additional details such as SSO application groups, users, SSO subscriptions, and reclamation candidates for an application.

<table id="table_tp4_cvh_bzb"><thead><tr><th>

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
</table>
**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

