---
title: Service Mapping Workspace
description: The Service Mapping workspace provides a central location to streamline the process of mapping your application services. Use the visualizations and reports to analyze, monitor, and update your resources, create application services, and manage your service mapping tasks efficiently.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping Workspace

The Service Mapping workspace provides a central location to streamline the process of mapping your application services. Use the visualizations and reports to analyze, monitor, and update your resources, create application services, and manage your service mapping tasks efficiently.

## Access

Navigate to **Workspaces** &gt; **Service Mapping**.

## Key features and capabilities

-   **Machine Learning \(ML\) readiness** - Confirm that your Machine Learning environment is prepared before you start to map application services.
-   **Detailed service maps** - Drill down for detailed information on service maps across various categories.
-   **Automated Service Suggestions** - Leverage Automated Service Suggestions to evaluate suggested application service candidates, using them to create application services or enhance existing ones.
-   **Improved resource utilization** - Use unmapped servers linked to an application service candidate to create application services.
-   **Tag-based service mapping** - Use the Tag-based mapping dashboard to map your organization's configuration items \(CIs\) into application services.

**Important:**

Access to tag-based service mapping in the Service Mapping workspace requires the installation of Service Mapping Plus version 1.16.3. For more information, see [Install Service Mapping Plus](../task/install-service-mapping-plus.md).

## Key Metrics

-   **Mapped application services**

    The number of application services previously mapped. Select to view specific information about these services such as operational status and business criticality.

-   **ML-powered candidates**

    The number of application service candidates identified using the Automated Service Suggestions feature.

-   **Mapped servers**

    The number of servers currently linked to an application service. Select to view information such as operational status and owner.


## Reports

Select the relevant section of each report to view more detailed information.

<table id="table_aj2_bvz_cxb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service maps by operation type

</td><td>

Bar report

![](../../../use/reporting/image/icon-bar-report-p.png)

</td><td>

cmdb\_ci\_service\_discovered

</td><td>

A bar report that presents the mapped application services grouped by operation type.

</td></tr><tr><td>

Service maps by creation method

</td><td>

Pie report

![](../../../use/reporting/image/icon-pie-report-p.png)

</td><td>

cmdb\_ci\_service\_discovered

</td><td>

A pie report that presents the mapped application services grouped by creation method.

</td></tr><tr><td>

Service maps by criticality

</td><td>

Bar report

![](../../../use/reporting/image/icon-bar-report-p.png)

</td><td>

cmdb\_ci\_service\_discovered

</td><td>

A bar report that presents the mapped application services grouped by the level of criticality.

</td></tr><tr><td>

Unmapped servers**Note:** This view is applicable to users with Service Mapping Plus versions earlier than 1.16.3.

</td><td>

Bar report

![](../../../use/reporting/image/icon-bar-report-p.png)

</td><td>

Server \[cmdb\_ci\_server\]

 Service Configuration Item Association \[svc\_ci\_assoc\]

 Application service candidate \[sa\_ml\_application\_service\_candidate\]

</td><td>

A bar report that presents unmapped servers that have been matched to an application service candidate as well as those servers with no candidate.

 Select **Unmapped servers with candidate** to view servers you can use to create an application service. For more information, see [Create an application service for unmapped servers](../task/unmapped-servers.md).

</td></tr></tbody>
</table>## Additional components

-   **Populate data**

    You can select this button to refresh the page and update the displayed information to reflect the most recent data.

-   **Search for server**

    You can locate a specific server using this field by entering the server name to see a list of options. Selecting the server you want from the list, and then **Search**, takes you to the **Mapped Server** page. Select the server name for more detailed information.


## Tag-based service mapping

Select the Tag-based service mapping icon ![](../../../reuse/icons/product-icons/tag-outline-24.svg) to access the Tag-based service mapping dashboard. Here you can categorize and map your organizaton's on-prem and cloud resources into application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](tag-based-mapping-dashboard.md).

## Application service readiness dashboard

Select the Application service readiness icon ![](../image/icon-clipboard-check.png) to access the Application service readiness dashboard.

Use this dashboard to ensure you have enabled Predictive Intelligence, verify Machine Learning readiness, and confirm that your data has been trained.

For more information about application readiness, see [Application service readiness dashboard in configurable workspace](readiness-dashboard-ml.md).

**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

**Related topics**  


[Automated Service Suggestions](../concept/auto-serv-suggest.md)

[Map application services based on Automated Service Suggestions](../task/map-application-suggestion.md)

[Name suggestions for application service candidates](app-services-name-suggestions.md)

