---
title: Exploring API Insights
description: Learn about API Insights with a sample workflow and review the benefits it can provide for different users in your organization.
locale: en-US
release: zurich
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring API Insights

Learn about API Insights with a sample workflow and review the benefits it can provide for different users in your organization.

## API Insights overview

API Insights is a centralized workspace for enterprise or software architects and Configuration Management Database \(CMDB\) administrators to analyze and take action on their organization's application programming interface \(API\) inventory.

## API Insights users

<table id="table_xml_sv3_ybc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise architect

</td><td>

Users with the sn\_api\_insights\_ws.api\_mgmt\_architect role can access the API Insights workspace to search APIs, monitor team APIs, view managed APIs, track API activity, review API access requests, and manage API life cycle aspects, including APIs without interfaces, business applications, ownership, or product models.

</td></tr><tr><td>

Enterprise architect administrator

</td><td>

Users with the sn\_api\_insights\_ws.api\_mgmt\_architect\_admin role can access the API Insights workspace to search APIs, evaluate metrics on API usage, set parameters for creating an API, connect APIs to a business context, specify the group attribute for ownership, and associate a workflow for granting access to APIs.

</td></tr><tr><td>

CMDB administrator

</td><td>

Users with the sn\_cmdb\_admin role can configure and manage the API-related Service Graph Connectors. They can accept or reject clustering recommendations, search for and compare APIs, and adjust settings related to API data management within the CMDB.**Note:** A CMDB administrator needs additional roles such as ml\_report\_user, platform\_ml\_read, and cmdb\_inst\_admin to access some of the features and data.

Additionally, the CMDB administrator needs the following security roles to access specific widgets:

-   sn\_si.basic or evt\_mgmt\_user – Required for Events and Critical alerts
-   sn\_vul.vulnerability\_read – Required for Active vulnerability items
-   sn\_msi.msi\_incident\_read – Required for Security incidents
-   sn\_si.read – Required for Incidents

</td></tr></tbody>
</table>## API Insights example workflow

![Workflow describing various tasks a user with the sn_api_insights_ws.api_mgmt_architect_admin, sn_api_insights_ws.api_mgmt_architect, or sn_cmdb_admin role can perform in API Insights.](../image/api-insights-workflow.png "Example workflow for the API Insights users")

1.  A CMDB administrator with the sn\_cmdb\_admin role logs in to API Insights and configures the API Service Graph Connectors to import API data from various sources. Also, reviews and resolves any connection errors to ensure a smooth data import process.
2.  An enterprise architect administrator with the sn\_api\_insights\_ws.api\_mgmt\_architect\_admin role accesses the settings page and adjusts the ownership settings according to their preferences.
3.  An enterprise architect with the sn\_api\_insights\_ws.api\_mgmt\_architect role navigates to the APIs missing data section to enrich API records by adding relationships and references. This includes associating business context, assigning ownership groups, linking product models, and defining API designs.
4.  The enterprise architect explores the API page, which provides a centralized view of all APIs and views all APIs in one place. They drill down into specific APIs to analyze details such as ownership, deployment locations, consumer usage, security incidents, and alerts. Additionally, they assess how each API fits within the broader ecosystem, identifying key relationships and dependencies in the API relationship map.

## API Insights benefits

<table id="table_ejf_j3j_fcc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Implement a system of record for enterprise-wide APIs.

</td><td>

Workspace to view and interact with API inventory

</td><td>

API Insights administrator

</td></tr><tr><td>

Achieve enterprise-wide visibility of APIs.

</td><td>

Automated discovery and ingestion of API data from various sources into Configuration Management Database \(CMDB\)

</td><td>

API Insights administrator

</td></tr><tr><td>

Map APIs to application services and business context.

</td><td>

Workflow for mapping APIs to relevant application services and business context

</td><td>

API Insights administrator

</td></tr><tr><td>

Integrate API data from a broad ecosystem of sources into the CMDB via Service Graph Connectors.

</td><td>

API data ingestion using API Service Graph Connectors into CMDB

</td><td>

CMDB administrator

</td></tr><tr><td>

Search for relevant APIs.

</td><td>

API search functionality with a user-friendly interface

</td><td>

API Insights administrator

</td></tr><tr><td>

Enable workflow configurations for API access requests.

</td><td>

Customization of API access request workflows

</td><td>

API Insights administrator

</td></tr><tr><td>

View the usage, security, and service mapping of each API and its components.

</td><td>

Detailed view of API inventory, requests according to minute, unique consumers, security data, IT Operations Management \(ITOM\) and IT Service Management \(ITSM\) data, and relationship mapping

</td><td>

API Insights architectAPI Insights administrator

CMDB administrator

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using API Insights, see:

-   [Configuring API Insights](api-insights-configuring.md)
-   [Administering and monitoring API data with API Insights](api-insights-overview-page.md)
-   [Managing API data in API Insights](api-insights-managing-apis.md)
-   [Managing API access within API Insights](api-insights-received-req.md)
-   [Optimizing API organization with clustering recommendations in API Insights](api-insights-cluster-recomm.md)
-   [Managing API data connections added for Service Graph Connectors in API Insights](api-insights-managing-connection.md)
-   [API Insights reference](api-insights-reference.md)

