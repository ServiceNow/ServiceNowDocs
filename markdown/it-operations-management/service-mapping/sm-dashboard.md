---
title: Service Mapping Workspace
description: The Service Mapping workspace provides a central location to streamline the process of mapping your application services. Use the visualizations and reports to analyze, monitor, and update your resources, create application services, and manage your service mapping tasks efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-dashboard.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping Workspace

The Service Mapping workspace provides a central location to streamline the process of mapping your application services. Use the visualizations and reports to analyze, monitor, and update your resources, create application services, and manage your service mapping tasks efficiently.

## Access

Navigate to **Workspaces** &gt; **Service Mapping**.

## Key features and capabilities

-   **Machine Learning \(ML\) readiness**

    Confirm that your Machine Learning environment is prepared before you start to map application services.

-   **Detailed service maps**

    Drill down for detailed information on service maps across various categories.

-   **Automated Service Suggestions**

    Leverage Automated Service Suggestions to evaluate suggested application service candidates, using them to create application services or enhance existing ones.

-   **Improved resource utilization**

    Use unmapped servers linked to an application service candidate to create application services.

-   **Tag-based service mapping**

    Use the Tag-based mapping dashboard to map your organization's configuration items \(CIs\) into application services.

-   **Create a service instance or a unified service**
    -   Create a service instance to leverage your resources in unmapped services.
    -   Create a unified service from various sources. For more information, see: [Multi-source service mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/multi-source-service-mapping.md).

**Important:**

Access to tag-based service mapping in the Service Mapping workspace requires the installation of Service Mapping Plus version 1.16.3. For more information, see [Install Service Mapping Plus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/install-service-mapping-plus.md).

## Key metrics

-   **Mapped application services**

    The number of application services previously mapped. Select to view specific information about these services such as operational status and business criticality.

-   **ML-powered candidates**

    The number of application service candidates identified using the Automated Service Suggestions feature.

    **Note:** Starting with Service Mapping Plus version 1.16.3, the filtering process has been updated to include only the most relevant candidates, excluding any ignored or irrelevant ones. This enhancement requires the installation of ITOM Content Service.

-   **Mapped servers**

    The number of servers currently linked to an application service. Select to view information such as operational status and owner. The **Mapped servers** tile is replaced with Now Assist metrics, once Now Assist is installed.


## Service Mapping AI Agents

When Now Assist is installed, the **Service Mapping home** page displays the AI Agent activation panel. Use this panel to activate or deactivate AI agents that automate service mapping tasks. For more information, see [AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-ai-specialists.md).

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

\[Omitted image "icon-bar-report-p.png"\] Alt text:

</td><td>

Mapped Application Service \[cmdb\_ci\_service\_discovered\]

</td><td>

A bar report that presents the mapped application services grouped by operation type.

</td></tr><tr><td>

Service maps by creation method

</td><td>

Pie report

\[Omitted image "icon-pie-report-p.png"\] Alt text:

</td><td>

Mapped Application Service \[cmdb\_ci\_service\_discovered\]

</td><td>

A pie report that presents the mapped application services grouped by creation method.

</td></tr><tr><td>

Service maps by criticality

</td><td>

Bar report

\[Omitted image "icon-bar-report-p.png"\] Alt text:

</td><td>

Mapped Application Service \[cmdb\_ci\_service\_discovered\]

</td><td>

A bar report that presents the mapped application services grouped by the level of criticality.

</td></tr><tr><td>

Unmapped servers**Note:** This view is applicable to users with Service Mapping Plus versions earlier than 1.16.3.

</td><td>

Bar report

\[Omitted image "icon-bar-report-p.png"\] Alt text:

</td><td>

Server \[cmdb\_ci\_server\]

 Service Configuration Item Association \[svc\_ci\_assoc\]

 Application service candidate \[sa\_ml\_application\_service\_candidate\]

</td><td>

A bar report that presents unmapped servers that have been matched to an application service candidate as well as those servers with no candidate.

 Select **Unmapped servers with candidate** to view servers you can map to an application service. For more information, see [Create an application service for unmapped servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/unmapped-servers.md).

</td></tr><tr><td>

Unmapped servers**Note:** This view is available starting with Service Mapping Plus version 1.16.3.

</td><td>

Bar report

 \[Omitted image "icon-bar-report-p.png"\] Alt text:

</td><td>

Server \[cmdb\_ci\_server\]

 Service Configuration Item Association \[svc\_ci\_assoc\]

 Application service candidate \[sa\_ml\_application\_service\_candidate\]

</td><td>

A bar report that presents the number of unmapped servers, divided into two categories:

-   **Unmapped servers with candidate** - servers that have been matched to an application service candidate.
-   **Unmapped servers without relevant candidate** - servers that have no candidate.

 **Note:** Starting with Service Mapping Plus version 1.16.3, the filtering process has been updated to include only the most relevant candidates, excluding any ignored or irrelevant ones. This enhancement requires the installation of ITOM Content Service.

</td></tr></tbody>
</table>## Additional components

-   **Refresh icon**

    You can select this button to refresh the page and update the displayed information to reflect the most recent data.

-   **Search for server**

    You can use this field to locate a specific server and review it's detailed information.


## Tag-based service mapping

Select the Tag-based service mapping icon \[Omitted image "tag-outline-24.svg"\] Alt text: to access the Tag-based service mapping dashboard. Here you can categorize and map your organizaton's on-prem and cloud resources into application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/tag-based-mapping-dashboard.md).

## Application service readiness dashboard

Select the Application service readiness icon \[Omitted image "icon-clipboard-check.png"\] Alt text: to access the Application service readiness dashboard.

Use this dashboard to ensure you have enabled Predictive Intelligence, verify Machine Learning readiness, and confirm that your data has been trained.

For more information about application readiness, see [Application service readiness dashboard in configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/readiness-dashboard-ml.md).

**Parent Topic:**[Service Mapping reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-reference.md)

**Related topics**  


[Automated Service Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/auto-serv-suggest.md)

[Map application services based on Automated Service Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/map-application-suggestion.md)

[Name suggestions for application service candidates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/app-services-name-suggestions.md)

[Map your application services using tags in the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/map-tag-based-services-workspace.md)

