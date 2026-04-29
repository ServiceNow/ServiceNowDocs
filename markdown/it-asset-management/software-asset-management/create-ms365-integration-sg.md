---
title: Create a Microsoft 365 integration
description: Compare Microsoft 365 user subscriptions with installation usage data for a complete license compliance position.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft 365 SaaS License Management success guide, Success Guides, Success portal view in Software Asset Workspace, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Create a Microsoft 365 integration

Compare Microsoft 365 user subscriptions with installation usage data for a complete license compliance position.

## Before you begin

Role required: Navigate to the linked topics in each step for the required roles.

Enable the following plugins:

-   Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\)
-   Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\)
-   
Complete the steps in the [Request Software Asset Management](t_RequSoftwareAssetMgmt.md) topic.

## Procedure

1.  Integrate with Microsoft 365 in the cloud for user subscription data.

    For more information, see [Create a Microsoft 365 integration profile](set-up-microsoft-office-365.md).

2.  Configure Microsoft Power BI for gaining access to Power BI service content and APIs.

    Power BI service content and APIs help optimize your Microsoft 365 subscriptions, such as by downgrading subscriptions from Office 365 E5 to Office 365 E3. For more information, see [Enable service principal authentication for Power BI read-only APIs](enable-service-principal-authentication-microsoft.md).

3.  Integrate with an inventory tool for installation usage data.

    -   For integrating with Microsoft SCCM, complete the steps in the [Service Graph Connector for Microsoft SCCM](https://www.servicenow.com/docs/access?context=cmdb-integration-sccm&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) topic and all subtopics.
    -   For integrating with ServiceNow Agent Client Collector \(ACC\), complete the steps in the [Agent Client Collector installation](https://www.servicenow.com/docs/access?context=acc-installation&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) topic and all subtopics.

        **Note:** ServiceNow Agent Client Collector \(ACC\) is a separately licensed IT Operations Management \(ITOM\) product. For details, contact your ServiceNow account executive.

    -   For integrating with Jamf for MAC OS devices, complete the steps in the [Service Graph Connector for Jamf](https://www.servicenow.com/docs/access?context=cmdb-integration-jamf&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) topic and all subtopics.
    -   To integrate with a third-party inventory tool, complete the steps in the [Software asset connections](../concept/third-party-discovery-sam.md) topic and all subtopics.

## What to do next

[Validate subscription, installation, and usage data](validate-sub-sg.md)

