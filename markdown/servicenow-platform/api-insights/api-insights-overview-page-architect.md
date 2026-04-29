---
title: Monitoring APIs and assessing data quality with API Insights
description: The Overview tab in the API Insights workspace provides a centralized view of data ingestion activities and integration health.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer and monitor API data, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Monitoring APIs and assessing data quality with API Insights

The Overview tab in the API Insights workspace provides a centralized view of data ingestion activities and integration health.

![API Insights overview tab.](../image/api-insights-overview.png)

## Access the API Insights Overview tab

To access the Overview tab, navigate to **Workspaces** &gt; **API Insights**. The Overview tab opens by default.

## Required roles

You need the sn\_api\_insights\_ws.api\_mgmt\_architect or the sn\_api\_insights\_ws.api\_mgmt\_architect\_admin role.

## Use cases

For examples of how different people in your organization would use this workspace, see these use cases.

|User|Workspace use|
|----|-------------|
|Enterprise architect|Search for APIs, compare APIs, request access to APIs, and address data issues.|
|Enterprise architect administrator|Manage API Insights settings, including API creation tools, business context relationship models, and ownership groups.|

## Features

Access the various cards on the Overview tab to gain insights on the API data available in your organization.

<table id="table_cnz_34b_mfc"><thead><tr><th>

Feature

</th><th>

Description

</th><th>

Required roles

</th></tr></thead><tbody><tr><td>

Search APIs

</td><td>

API search within the organization to locate specific APIs for review or management.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

Access requests received

</td><td>

Number of access requests received indicating the need for API access management.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

Your access requests

</td><td>

Number of access requests created by the logged-in user, indicating the activity for API access management.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

Helpful resources

</td><td>

Links to product documentation, knowledge base articles, and a community forum for additional support and information.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td class="sub-head" colspan="3">

APIs missing data

</td></tr><tr><td>

Missing business context

</td><td>

Count of APIs with no business context assigned.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

Missing ownership groups

</td><td>

Count of APIs with no ownership group assigned.Ownership groups enable tracking remediation and managing access requests.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

Missing product models

</td><td>

Count of APIs with no product model assigned, Product models enable accurate reporting and interactions with multiple versioned APIs.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

Missing design

</td><td>

Count of runtime APIs, available as API configuration items \(CIs\), with no design representation.Linking runtime APIs with design-time APIs, available as Digital Interface records, improves usability.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr class="sub-head"><td class="sub-head" id="entry_vc1_1n2_sfc" colspan="3">

Your team's APIs

</td></tr><tr><td>

All APIs

</td><td>

Total number of APIs managed by a team.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

In design

</td><td>

Number of APIs currently being designed.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

Operational

</td><td>

Number of APIs in active use.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td>

End of Life

</td><td>

Number of APIs that are retired or decommissioned.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr><tr><td class="sub-head" colspan="3">

APIs managed by your team

</td></tr><tr><td>

All APIs managed by your team

</td><td>

Overview of the APIs managed by a team, based on the group associated with the logged-in user and the APIs linked to that group. API details include name, consumer count, management platform, life cycle stage, version, and requests per minute.Populates data corresponding to the selected card in the [Your team's APIs](api-insights-overview-page-architect.md#entry_vc1_1n2_sfc) section.

</td><td>

-   sn\_api\_insights\_ws.api\_mgmt\_architect
-   sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

</td></tr></tbody>
</table>