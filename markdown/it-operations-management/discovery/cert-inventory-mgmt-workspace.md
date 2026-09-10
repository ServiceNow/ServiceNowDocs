---
title: Certificate Management workspace
description: The Certificate Management workspace provides centralized visibility into your organization's certificates so you can make data-driven decisions. For example, you can avoid outages by looking at the numbers that are soon to expire.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/cert-inventory-mgmt-workspace.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Management workspace

The Certificate Management workspace provides centralized visibility into your organization's certificates so you can make data-driven decisions. For example, you can avoid outages by looking at the numbers that are soon to expire.

## Roles Required

-   Certificate user \[sn\_disco\_certmgmt.pki\_user\]
-   Certificate approver \[sn\_disco\_certmgmt.pki\_approver\]
-   Certificate admin \[sn\_disco\_certmgmt.pki\_admin\]

## Accessing the Certificate Management workspace

To open the workspace, navigate to **Workspaces** &gt; **Certificate Management Workspace**.

The Certificate Management workspace has five tabs:

<table><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Inventory**

</td><td>

Displays key insights about all certificates including certificates that are active, that have expired, that are expiring soon, and that have been revoked. Select each widget to view its list. This is the default tab of the workspace.**Note:** The data on this tab is refreshed automatically every day.

</td></tr><tr><td>

**Tasks**

</td><td>

Displays manage tasks to track the upcoming tasks that will expire soon. These tasks are organized into four categories: Renewals, Requests, Expirations, and Automation trends.

</td></tr><tr><td>

**Certificate records**

</td><td>

Displays a filterable list view of all certificates in the system. Use this tab to search, inspect, and manage individual certificate records. You can switch between record types and access the configuration options.

</td></tr><tr><td>

**Downloads**

</td><td>

Displays the files that are required to set up the ServiceNow external issuer \(`sn-external-issuer`\) in Kubernetes.

</td></tr><tr><td>

**Settings**

</td><td>

Displays the settings to manage the notifications of this workspace. For more information on setting up these notifications, see [Receive certificate notifications via Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-ms-teams-cert-notifications.md) and [Receive certificate notifications via email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/receive-email-certificate-notifications.md).

</td></tr></tbody>
</table>