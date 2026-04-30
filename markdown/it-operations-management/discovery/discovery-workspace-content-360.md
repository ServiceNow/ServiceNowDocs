---
title: Discovery Admin Workspace Content 360
description: The Content 360 page enables you to discover applications and evaluate application suggestions based on machine learning or crowd-sourced resources. Then, create configuration items with a single click.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-11-09"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Content 360

The Content 360 page enables you to discover applications and evaluate application suggestions based on machine learning or crowd-sourced resources. Then, create configuration items with a single click.

Content 360 uses data visualizations to offer extensive visibility of your infrastructure's applications and the resources available to create application configuration items \(CIs\). It also provides access to a list of classifiers to add to discovery. Refresh the page to view the most up-to-date visualizations.

To access the Discovery Admin Workspace Content 360 page, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Content 360**.

## Key features

-   **AI-suggested application fingerprints**

    View a list of suggested applications with fingerprints that you can add to the discovery process through the AI-suggested application fingerprints feature. You can then select a group name to view extensive details about an application.

    -   Modify certain details such as the discovery pattern name or suggested CMDB class.
    -   View additional information about process samples and related servers.
    -   Choose to ignore viewed suggestions the next time Discovery runs.
    -   Add suggestions to the Configuration Management Database \(CMDB\) the next time Discovery runs.
    The AI-suggested application fingerprints widget doesn't refresh automatically. To ensure you're viewing the most up-to-date information, refresh the page manually.

    For more information about discovery based on application fingerprints, see [Discover applications based on fingerprints](../task/discover-application-based-process.md).

-   **Application CIs discovered**

    Monitor information about application CIs discovered based on application fingerprints or ITOM Content Service suggestions through the Discovery Admin Workspace. A pie report illustrates the total number of user-defined application CIs discovered, while a bar report presents the top five application CIs discovered, created within the last two days, and grouped by class.

-   **ITOM Content Service**

    ITOM Content Service collects unrecognized application fingerprints from different environments. AI librarians analyze these fingerprints, creating dedicated classifiers that are updated and shipped to you weekly. The latest version of Discovery Admin Workspace enables you to refresh the content service suggestions manually before reviewing them. As new IT products are rapidly released to the market, this feature grants you rapidly updating visibility and provides the following benefits:

    -   It reviews the products that you’re currently using every week and delivers new application fingerprints.
    -   It identifies irrelevant processes that aren’t suitable candidates for CIs.
    -   Based on AI, it helps you identify running processes fingerprints and Simple Network Management Protocol \(SNMP\) Object Identifiers \(OIDs\) and create the CIs you need for monitoring your infrastructure.
    -   Discovers a higher number of products by using AI capabilities that cluster and classify running application processes.
    On the latest version of Discovery Admin Workspace, starting from Xanadu instances, the Content service suggestions widget refreshes automatically and displays the most up-to-date information. This is indicated by the real time icon \(![Real time icon](../image/real-time-icon-content-service-suggestions.png)\) that appears next to the widget name.

    To learn more about ITOM Content Service, see [ITOM Content Service](discovery-content-services.md).

    **Sharing data on ITOM Content Service**

    The Continuance Delivery System \(CDS\), a ServiceNow® technology, synchronizes data between the Data Services instance—which stores and distributes data—and the customer instances, using only the processes and SNMP OIDS data. Using the ITOM Content Service feature through the CDS, you can opt in to share application fingerprint process data. This data can be tagged and classified by AI librarians, enabling ITOM Content Service to deliver new CIs every week. Your data is shared with your ServiceNow® instance in a safe environment. You have the assurance that no personal information is revealed, and all information is kept anonymous. Participation is optional and you can opt out at any time.

    Starting with ITOM Content Service version 1.6.2 and Discovery Admin Workspace version 1.11.0, you can also opt in to share Service Info data of mapped candidates

    For more information, see [Share data on ITOM Content Service](../task/share-data-itom-content-service.md).


## Prerequisites

Plugins required for ITOM Content Service:

-   Discovery
-   Normalization Data Services

