---
title: Monitor inbound API integration usage
description: Monitor inbound integration usage requests, data egress, and domain-level usage through the Inbound API Integration Usage dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/inbound-api-integration-usage-dashboard.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-09-29"
reading_time_minutes: 3
breadcrumb: [Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Monitor inbound API integration usage

Monitor inbound integration usage requests, data egress, and domain-level usage through the Inbound API Integration Usage dashboard.

The Inbound API Integration Usage dashboard contains visualizations that help you assess the usage of your inbound integration calls. With the **inbound\_integration\_metering\_admin** role, you can view usage data across three tabs: Transactions, Data Egress, and Usage by Domain.

\[Omitted image "inbound-api-integration-dashboard.png"\] Alt text: Inbound API Integration Usage Dashboard

## Transactions tab

The Transactions tab shows the number of inbound integration requests. Use this tab to monitor request counts and identify which applications, requestors, or resources are making the most requests.

|Visualization|Description|
|-------------|-----------|
|Integration Requests Today|Total integration request count for the current day.|
|Integration Requests \(Daily\)|Number of integration requests for each day over the last 30 days.|
|Integration Requests \(Monthly\)|Number of integration requests for each month over the last 13 months.|
|Integration Requests by Provider|Number of integration requests by OAuth provider.|
|Integration Requests by Requestor \(Daily\)|Number of integration requests by requestor for each day over the last 30 days.|
|Integration Requests by Requestor \(Last 30 days\)|Number of integration requests by requestor over the last 30 days.|
|Integration Requests by Application \(Last 30 days\)|Number of integration requests by OAuth application over the last 30 days.|
|Integration Requests by Resource \(Last 30 days\)|Number of integration requests by resource over the last 30 days.|

## Data Egress tab

The Data Egress tab shows the data volume returned in integration responses. Use this tab to identify which applications or requestors have the highest data egress, and monitor API access volume usage by service account, user, and application. For more information on how inbound API integrations contribute to Workflow Data Fabric usage, see the [Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub-usage-dashboard.md).

|Visualization|Description|
|-------------|-----------|
|Data Egress Usage - Today \(MB\)|Total data egress for the current day.|
|Data Egress Usage - Daily \(MB\)|Data egress for each day over the last 30 days.|
|Data Egress Usage - Monthly \(GB\)|Data egress for each month over the last 13 months.|
|Data Egress Usage by Provider \(GB\)|Data egress by OAuth provider.|
|Data Egress Usage by Requestor - Daily \(MB\)|Data egress by requestor for each day over the last 30 days.|
|Data Egress Usage by Application - Last 30 days \(GB\)|Data egress by OAuth application over the last 30 days.|

## Usage by Domain tab

The Usage by Domain tab shows the number of inbound integration requests and data egress volume broken down by domain. Use this tab to attribute usage across the domains configured on your instance, not to investigate individual requests.

**Note:** The Usage by Domain tab is only visible on instances where domain separation is enabled.

Users with the admin role see usage across all domains regardless of which domain they belong to.

|Visualization|Description|
|-------------|-----------|
|Integration Requests - Daily|Number of integration requests by domain for each day over the last 30 days.|
|Integration Requests - Monthly|Number of integration requests by domain for each month over the last 13 months.|
|Data Egress Usage - Daily \(MB\)|Data egress by domain for each day over the last 30 days.|
|Data Egress Usage - Monthly \(GB\)|Data egress by domain for each month over the last 13 months.|

-   **[View Inbound API Integration Usage dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/view-inbound-api-integration-usage-dashboard.md)**  
View integration request counts, data egress volume, and domain-level usage.
-   **[Registered integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/registered-integrations.md)**  
View the list of all the inbound API integrations registered on ServiceNow.

**Parent Topic:**[Additional integration resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/additional-integration-resources.md)

