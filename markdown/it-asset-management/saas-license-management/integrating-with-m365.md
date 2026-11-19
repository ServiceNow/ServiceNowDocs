---
title: Integrating with Microsoft 365
description: Integrating the Software Asset Management application with the Microsoft 365 service enables you to track your software subscriptions and software usage to determine license compliance and act on optimization opportunities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/saas-license-management/integrating-with-m365.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-11-05"
reading_time_minutes: 3
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Integrating with Microsoft 365

Integrating the Software Asset Management application with the Microsoft 365 service enables you to track your software subscriptions and software usage to determine license compliance and act on optimization opportunities.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required?

</th><th>

Required user role in the Microsoft 365 application

</th><th>

Authentication scopes

</th><th>

Purpose

</th><th>

Least privilege?

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Mandatory

</td><td>

Application developer

</td><td>

-   User.Read.All
-   LicenseAssignment.Read.All

</td><td>

Permits the ServiceNow instance to read tenant, user, and license information to synchronize Microsoft 365 subscription data.

</td><td>

The user role and scope are read-only and limited to metadata access. It doesn't allow modifying users, groups, or licenses.

</td></tr><tr><td>

Pull user activity

</td><td>

Optional

</td><td>

-   Application developer
-   Power platform administrator

</td><td>

Reports.Read.All

</td><td>

-   Pulls usage of Microsoft 365 apps for Enterprise \(Microsoft Word, Excel, PowerPoint\), and other products such as Exchange Online, Teams, OneDrive, Power BI, SharePoint Online, Viva Engage \(previously Yammer\). Required for the Software Asset Management Professional application to generate optimization recommendations for low usage. For example, low usage for Microsoft 365 E1, Microsoft 365 E3-&gt; E1.
-   Pulls Power BI usage and activity metrics for license optimization. Required for the Software Asset Management Professional application to generate optimization recommendation for low usage. For example, Microsoft 365 E5-&gt; E3.

</td><td>

-   The role and scope are read-only and limited to metadata access. It doesn't allow modifying users, groups, or licenses.
-   For getting Power BI usage, this is the least privilege role. You should consider limiting membership to specific security groups and enabling read-only Power BI admin settings for the service principal.

</td></tr><tr><td>

Reclaim subscriptions

</td><td>

Optional

</td><td>

Application developer

</td><td>

-   GroupMember.ReadWrite.All
-   LicenseAssignment.ReadWrite.All

</td><td>

Permits the Software Asset Management Professional application to reclaim inactive licenses by removing Microsoft 365 subscriptions assigned to inactive users.

</td><td>

These permissions only enable modifying license assignments and don't provide tenant-wide admin capabilities.

</td></tr><tr><td>

Assign licenses

</td><td>

Optional

</td><td>

Application developer

</td><td>

-   GroupMember.ReadWrite.All
-   LicenseAssignment.Read.All
-   LicenseAssignment.ReadWrite.All
-   User.Read.All

</td><td>

Allows license assignment to users in the Microsoft 365 portal.

</td><td>

These permissions only enable Microsoft 365 license assignment.

</td></tr></tbody>
</table>**Related topics**  


[Register a Microsoft Entra ID application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/saas-license-management/register-microsoft-app.md)

[Enable service principal authentication for Power BI read-only APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/saas-license-management/enable-service-principal-authentication-microsoft.md)

[Configure updates on Microsoft 365 Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/saas-license-management/conf-update-micro-admin.md)

[Create a Microsoft 365 integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/saas-license-management/set-up-microsoft-office-365.md)

[Determine and verify Microsoft 365 subscription information in your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/ver-o365-info.md)

[Upload the Microsoft 365 Copilot, Visio Online, Planner, and Project usage reports to your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/upload-usage-reports-copilot-visio-project.md)

[Evaluating software usage activity for Microsoft 365 subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/o365-usage-activity.md)

[Evaluate Microsoft 365 compliance and optimization results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/det-comp-opt-results.md)

[Update REST and OAuth endpoints for Microsoft Office 365 Government plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/update-o365-gov-plans.md)

[Publisher optimizations for Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/pub-opt-microsoft.md)

[Reclamation rules for Microsoft 365 integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/m365-reclamation-rules.md)

