---
title: Automated license removal for Microsoft 365
description: Software Asset Management optimizes Microsoft 365 subscription usage by identifying low usage and overlapping candidates, and then automatically removing the licenses from the Microsoft 365 admin center. This proactive management helps you streamline costs and enhance the efficiency of low usage and overlapping licenses.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Automated license removal for Microsoft 365

Software Asset Management optimizes Microsoft 365 subscription usage by identifying low usage and overlapping candidates, and then automatically removing the licenses from the Microsoft 365 admin center. This proactive management helps you streamline costs and enhance the efficiency of low usage and overlapping licenses.

## Eligible candidates

After a reclamation candidate is generated, the following low usage and overlapping candidates are considered eligible for automated removal:

-   Low usage candidates with individual subscriptions such as Microsoft Teams, Microsoft SharePoint, or other single services.
-   Low usage candidates with subscription suites including Microsoft 365 and Microsoft Office 365.

    **Note:** However, due to the varied usage across different products within these suites, users are notified, and the final removal requires approval from the SAM Manager. The **Notify User** check box is selected by default in the reclamation rule. But you can clear the check box to skip the approval process.

-   Overlapping candidates with any subscription type.

## Prerequisites

Before initiating the automatic removal of licenses from the Microsoft 365 admin center, confirm that the following prerequisites are met:

-   The following spoke is set up and plugins are installed:
    -   Microsoft Entra ID Spoke
    -   Software Asset Management Professional \(com.snc.samp\)
    -   Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\)
-   Microsoft Entra ID is configured with the following permissions to access and manage user and group information:
    -   **User.Read.All**
    -   **GroupMember.ReadWrite.All**
    -   **LicenseAssignment.ReadWrite.All**

## Scenarios

Software Asset Management removes the Microsoft 365 licenses from the Microsoft 365 admin center in the following scenarios:

-   When a license is directly assigned to a user, the license is removed.
-   When a license is directly assigned to a user and also through one or more groups, the user is removed from the group and the direct license assigned to the user is removed.

    **Note:** When multiple licenses are assigned to a user through a group, the user isn't removed from the group.  If a user in a group with multiple licenses shows low usage and is subsequently removed, they may lose access to other important licenses. You must contact your Microsoft 365 Admin to address this issue. For more information, see [Manage licensing in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/users/licensing-group-advanced).

-   When a license is directly assigned to a user and also through multiple groups having the same and only one license, the user is removed from all the groups and the direct license assigned to the user is removed. 

    **Note:** When multiple licenses are assigned to a user through different groups, the user isn't removed from any groups. 

     

-   When Software Asset Management removes the Microsoft 365 licenses from the Microsoft 365 admin center successfully, the reclamation workflow closes automatically.

**Related topics**  


[Evaluating software usage activity for Microsoft 365 subscriptions](o365-usage-activity.md)

[Optimization and savings dashboard in workspace](../reference/optimization-dashboard-workspace.md)

