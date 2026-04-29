---
title: Enterprise Architecture \(formerly Application Portfolio Management\) portal
description: The Enterprise Architecture portal gives you an enterprise-wide applications landscape view of the number of applications and other key metrics. As an enterprise architect \(EA\), you can view and access all the Enterprise Architecture modules from this portal.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Exploring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Enterprise Architecture \(formerly Application Portfolio Management\) portal

The Enterprise Architecture portal gives you an enterprise-wide applications landscape view of the number of applications and other key metrics. As an enterprise architect \(EA\), you can view and access all the Enterprise Architecture modules from this portal.

You can navigate to the Enterprise Architecture portal page by clicking **Enterprise Architecture** &gt; **Enterprise Architecture Workspace**. The role required is sn\_apm.apm\_analyst.

**Important:**

You’re encouraged to use this feature in the Enterprise Architecture Workspace. Enable the Enterprise Architecture Workspace \(sn\_apm\_ws\) plugin from the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

For more information on Enterprise Architecture Workspace, see [Enterprise Architecture Workspace](ea-workspace.md). For specific documentation about these features in the Enterprise Architecture Workspace, see [Enterprise Architecture Workspace Overview](../reference/eaw-reference/eaw-overview.md).

The Enterprise Architecture \(formerly Application Portfolio Management\) portal consists of four sections. The sections provide a quick access to view the portfolios of business capability, information, application, technology, and create goals, demands, and programs.

-   **Business Portfolio**

    View the number of business capabilities defined by your organization that have been assessed and are yet to be assessed. View the number of business applications that support the capabilities but are at a major risk.

    -   Click Hierarchy Map to [view the capability map](../task/view-capability-based-planning.md) in a new tab that displays the business capabilities and subcapabilities in a hierarchy.
    -   Click [Business Planning](overview-business-capability-planning.md) to navigate to the business planning portal.
-   **Information Portfolio**

    Capture the information from the assets of your organization as information objects. You can connect the information object to your business applications to have a portfolio of application information, ready and accessible to use at any time. The entities in the information portfolio are either configuration items or columns of tables. They are structurally designed to relate to each other either by CMDB CI relationships or by referencing the data columns of tables.

    The numbers below each entity of the Information Portfolio represent the following data:

    -   Data Domains: Total number of records in the Data Domain \[sn\_apm\_data\_domain\] table.
    -   Information Objects: Total number of records in the Information Object \[cmdb\_ci\_information\_object\] table.
    -   Database Catalogs: Total number of records in the Database Catalog \[cmdb\_ci\_db\_catalog\] table.
    -   Unstructured DB Catalogs: Total number of records in the configuration item tables such as:
        -   configuration file \(cmdb\_ci\_config\_file\)
        -   file system \(cmdb\_ci\_file\_system\)
        -   exchange mail box \(cmdb\_ci\_exchange\_mailbox\)
    **Note:**

    Your enterprise might have any number of database catalogs, but only the number of database catalogs that are linked to the information objects are displayed as counts in each of the information portfolio sections. Those information objects in turn are related to the business applications, Similarly, only those numbers of database instances that are referenced in the database catalogs are summed up as database instances.

    Click the **Information Objects** link to view the details of the information objects that are related to the business applications in your enterprise. See [Information Portfolio](apm-information-architecture.md).

    **Note:** The information objects must be related to the business application for you to view them in the Information Objects page that opens.

-   **Application Portfolio**

    Track the applications that support your business capabilities and manage them effectively to fulfill the goals of your organization. The portfolio provides a list of applications with information such as their category, manufacturer, and type.

    -   Click Applications to navigate to the list view of business applications in your organization.
    -   Analyze your applications by category or family and group them the way that you want them to be in the application [Landscape](../task/application-landscape-dashboard.md) view.
    -   Click Analyze to navigate to the [Group Analysis](../task/create-a-guided-program.md) page to analyze the applications and their scores.
-   **Technology Portfolio**

    View the number of hardware models and software models that are linked to your business applications. You can also get a count of the number of these models that are at high risk. Click the **Technology Portfolio** link to go to the TPM [timeline view](../task/view-technology-risks-in-timeline.md) and know the status of the hardware and software models life cycle.

    Use the Technology Reference Model to define the software products standards and manage unapproved software in your organization. For more information, see [Exploring Technology Reference Model](technology-reference-model-in-apm.md).

-   **Opportunities &amp; Solutions**

    View the number and click to view the list of goals, demands, and programs. Click any goal, demand, or program in the list to update its details. Use the **Create** link to directly create a goal, demand, or program.

    -   [Create a goal](../task/create-a-goal.md) to track, align, and report the progress of the work toward it. For example, a goal could be set to reduce Capex or reduce the number of applications within a target date.
    -   [Create a demand](../task/create-an-idea.md) to capture your strategic goal for the application.

        To create a demand from the application menu, navigate to **Enterprise Architecture** &gt; **Enterprise Architecture Workspace** &gt; **Portfolio**

    -   [Create a program](../task/create-a-program.md) to meet the goals. Enterprise Architecture takes you through a process to add targets and identify opportunities.

        **Note:** You can view and create programs from the Program section only when you activate PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

-   **Notifications**

    View the results of [desired and scripted audits](../task/run-desired-and-scripted-audits.md), the number of hardware and software models that face high and moderate risks, expiring on the current date and in the next 90 days, and pending certification instances that are open and not 100% complete. Click the notification to open the related task or the related data certification schedule instance to view the record details.

-   **Recent Activity**

    View your most recent activity of creating a goal, demand, or program for a fiscal period.


