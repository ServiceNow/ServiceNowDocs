---
title: ServiceNow Otto for Workflow Data Fabric \(WDF\)
description: The ServiceNow Otto for Workflow Data Fabric \(WDF\) application provides AI-guided assistance for discovering data fabric assets and configuring integrations. Use it to receive contextual recommendations and take actions directly without leaving your workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/exploring-now-assist-for-workflow-data-fabric.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [explore]
breadcrumb: [Explore, Workflow Data Fabric Home, Workflow Data Fabric]
---

# ServiceNow Otto for Workflow Data Fabric \(WDF\)

The ServiceNow Otto for Workflow Data Fabric \(WDF\) application provides AI-guided assistance for discovering data fabric assets and configuring integrations. Use it to receive contextual recommendations and take actions directly without leaving your workflow.

## AI entry points from WDF

ServiceNow Otto for WDF is accessible from two locations:

-   ServiceNow Otto for WDF conversational interface: Use the ServiceNow Otto conversational interface on WDF Home for comprehensive AI-assisted guidance on integrations, data products, and WDF configuration.
-   ServiceNow Otto panel: Access the ServiceNow Otto panel by selecting the sparkle \[Omitted image "image.now-assist-sparkle-icon-dark"\] icon in the page header for AI-assisted guidance while working in WDF Home or any other WDF application.

## ServiceNow Otto for WDF overview

You can use both, the ServiceNow Otto for WDF conversational interface or the ServiceNow Otto panel to discover data fabric tables, connectors, and collectors, and request guidance on how to set up integrations.

The advantage of the ServiceNow Otto for WDF conversational interface is that you receive in-depth answers. The conversational interface renders a visualized view of the search sources \(from KBs, data catalog, other applications\) in the home page interactive view.

The advantage of the ServiceNow Otto panel embedded in WDF Home page is that you get answers to a broader spectrum of questions related to different WDF and other applications. You get assistance for data integration, discovery, and action-taking tasks without leaving your current work context, across all WDF applications.

ServiceNow Otto for WDF includes the oneExtend LLM skill that enables you to find information about collectors, connectors, data fabric tables, data products, and more.

## ServiceNow Otto for WDF users

<table id="table_zq2_52f_zhc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All Workflow Data Fabric user roles

</td><td>

-   Connection Admin
-   Data Steward
-   WDF Builder
-   WDF Operator
-   WDF Consumer

</td></tr></tbody>
</table>## ServiceNow Otto Panel features and behavior

The ServiceNow Otto panel in WDF Home page includes these features:

-   Right-side positioning: Panel opens on the right side of your screen, preserving the main WDF Home page content on the left.
-   Resizable: Drag the panel's left edge to adjust its width based on your preferences and screen size.
-   Docking/Pinning: Pin the panel to keep it visible as you navigate within WDF applications \(Connect Hub, Data Products, etc.\)
-   Unpinning: Unpin the panel to focus on a specific task with more screen space.
-   Inline rendering: Content renders on the same page without opening new windows or tabs.
-   Interactive widgets: Supports form fields, buttons, and other interactive elements for direct action-taking.
-   Persistent conversation: Panel maintains your conversation history as long as your session is active.

## Prerequisites

To access the ServiceNow Otto for WDF search and ServiceNow Otto panel in WDF Home page, you must meet the following requirements.

-   Install and activate the ServiceNow Otto for WDF plugin \(sn\_nowassist\_wdf\).
-   You must have one of these roles assigned:
    -   df\_data\_steward: Full data governance and curation access
    -   connection\_admin: Full connection management access
    -   wdf\_operator: WDF operator/consumer access
    -   wdf\_builder: Custom connector and integration development access
    -   wdf\_consumer: Data discovery and request access
-   To use the ServiceNow Otto panel across WDF applications, you may need access to:
    -   Connect Hub \(for connection creation and management\)
    -   Data Catalog \(for asset discovery\)
    -   Data Workbench \(for interface and product creation\)
    -   Other WDF applications as needed

If the sparkle \[Omitted image "image.now-assist-sparkle-icon-dark"\] icon is not visible, confirm with your administrator that the ServiceNow Otto plugin is installed and your role is assigned.

## What to explore next

To learn more about configuring and using ServiceNow Otto for WDF, see:

-   [Configure ServiceNow Otto for Workflow Data Fabric \(WDF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-now-assist-for-workflow-data-fabric.md)
-   [Ask ServiceNow Otto for Workflow Data Fabric \(WDF\) for recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/ask-now-assist-for-recommendation.md)

