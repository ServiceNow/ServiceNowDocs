---
title: Access Service Owner Workspace
description: Open the Service Owner Workspace to access and display all your portfolios and services at a single location. Monitor and manage your services and offerings from the workspace.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Using Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Access Service Owner Workspace

Open the Service Owner Workspace to access and display all your portfolios and services at a single location. Monitor and manage your services and offerings from the workspace.

## Before you begin

Role required: service\_viewer

## About this task

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](../concept/SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Use Service Owner Workspace](../image/SOWUseBanner2.png "Navigate")

</td></tr></tbody>
</table>To access and use Service Owner Workspace, the Service Owner Workspace plugin \(com.spm\_owner\_workspace\) must be activated and you must be assigned the Service Viewer \[service\_viewer\] role.

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service Owner Workspace**.

2.  Click a portfolio name to expand the layers of services.

3.  Click **My Services** to view portfolios that you own and manage.

    Or click **All Services** to view all the services your organization owns and manages.

    A list of services displays. You can expand each service to see child services within the service taxonomy.

    ![All Services view](../image/AllServices.png)

4.  Click a service name to view pertinent information about the service.

    The **Overview** dashboard provides a recent snapshot of the service offering performance. View performance over the last 7 days. The **Additional Node Info** sidebar displays who owns and manages the service, as well as the associated **Performance score**, **Taxonomy Nodes** \(services\), and **Estimated spend** if available.

    ![Parent service view](../image/HighLevelService.png)

    To contact a service owner, service offering owner, or associated manager, click the person's name in the workspace and then click the associated email. Phone numbers are also displayed for quick access to service stakeholders.

5.  Choose how to group and sort dashboard data in the **Group by** and **Sort by** lists.

    You can group by **No grouping** or **Taxonomy node owner**. You can sort by **Ascending**, **Descending**, **Node weight**, **Performance score**, or **Name**.

6.  Click a **Taxonomy Node** \(service\) to view pertinent information about the service.

    The associated service displays in the **Overview** tab.

7.  Click in the **Service** card to drill deeper into the details and view health and performance metrics, as well as any associated service offerings.

    Service health and performance metrics, such as **Service Performance Score**, **Customer Satisfaction**, **Total Subscribers**, **Estimated spend**, and associated **Service Offerings** are displayed.

    ![Service offering view](../image/ServiceOfferingView.png)

8.  Click additional tabs besides the **Overview** tab to display data relevant to the offering, including:

    -   **Trends** — View performance over a specified time frame, as well as SLA compliance. The **Trends** tab provides you with a more strategic view of service and offering performance over a longer period of time, so you can determine if performance is trending up or down. The base system includes performance metrics for **Activity**, **Availability**, **Breached SLA**, **Customer Satisfaction**, and **Critical Incidents**. The default time frame for **Trends** performance is 30 days, except for the **Critical Incidents** metric, which shows all open major and P1 incidents per day. Use the drop down menu to change the time frame if desired. Choices include as few as the last 7 days to the last year.

        **Note:** Prior to the Quebec release, the **Critical Incidents** metric was called **Stability** and was depicted as a single score widget. The data is now visualized in a time series chart. You need to set the lower and upper boundaries for the **Critical Incident** metric. For details, refer to [Service Owner Workspace performance metrics](../concept/understanding-SPM2-perform-metrics.md).

    -   **Relationships** — View service dependency details. This tab shows offering relationships, for example, which services a service depends on and which services depend on it.

        View the **I depend on** and **Depends on me** sections to see service offering dependencies at the parent service level via a card with a highlighted label reading **Inherited relationship**.

        **Note:** Dependencies that a service inherits from a child offering are visually distinct from dependencies defined directly between services.

        Service and offering types are distinguishable in the card by a unique icon and label specifying the type of service and offering. For example, **Business Service**, **Application Service**, and **Technical Service**. When you click on an offering card, the record view of the offering is displayed.

    -   **Info** — View the service offering description, performance breakdown, general information, commitments, team, and more. You can also view your service offering to catalog item relationships via this tab. Click to open a catalog item to drill down into more details.

        Monitor fulfilled requests for all associated catalog items in the **Offering Activity** metric. For complete details about service offerings and associated catalog items, refer to [Service offering to catalog item relationships](../concept/SPM2-offering-to-catalog.md).

        **Note:** The **Create Catalog Item** action is only available when there is no catalog item mapped to a service offering and there is no catalog item with the same name as the offering. This prevents the issue of having catalog items with the same name.

    -   **Improvement Initiatives** — View all CIM initiatives as links to the records. This tab displays with activation of the Continual Improvement Management \(CIM\) plugin \(com.sn\_cim\).
9.  Click icons in the impact stream panel, on the right side of the workspace, to display related information about **Outages**, **Critical Incidents**, **Change Requests**, or **Attachments**.

    View the associated unique or critical information about the service offering in the impact stream.

    ![Contextual side panel](../image/ActivityStream.png)

10. Click an outage, critical incident, or change request to drill deeper into the details.

    Once you click an impact stream item, for example, a critical incident, you can view all details related to the item and even open the associated record by clicking **Open record**.

    Recent, current, and upcoming outage data is available. Click a type of outage for the information you want. Refer to [Outages](../concept/use-service-owner-workspace.md) for information about a unique **Outage Number** identifier and activating the Outage Numbering plugin \(com.snc.outage\_numbering\).

11. If the service you are viewing has associated child offerings, click an offering to drill down and view details.

    ![Service Offering Children view](../image/ServiceOfferingChild.png)

    View the offering overview, as well as other pertinent data, such as service offering availability, breached SLAs, customer satisfaction, stability, and activity. Available service offering tabs include, **Overview**, **Trends**, **Relationships**,**Info**, **Catalog Items**, and **Improvement Initiatives**. These tabs similar data as is provided for services. The **Catalog Items** tab displays all catalog items related to the service offering, as well as a short description of the item.


