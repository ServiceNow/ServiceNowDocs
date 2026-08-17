---
title: Campaigns
description: A campaign groups related metrics into one unit for collection and approval, centralizing shared properties such as due dates and entities so you can manage and track them together.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/campaigns.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Campaigns

A campaign groups related metrics into one unit for collection and approval, centralizing shared properties such as due dates and entities so you can manage and track them together.

A campaign brings together metrics that share a group, frequency, and calendar type. These three values define the campaign's metric set and lock once the campaign is published. Entities are added to the campaign separately, as part of its scope, and remain editable even after the campaign is published. An entity already assigned to another campaign with the same group, frequency, and calendar can't be added again. Each entity's scope must be unique across campaigns that share those three values. Shared properties, such as the due date offset, live on the campaign instead of being duplicated across each metric.

Campaigns support manual, calculated, and automated metric types together. Most filters for reviewing a campaign use dropdowns instead of free-text entry, reducing the number of selections approvers must make when reviewing a large campaign. A campaign moves through In progress, Pending publication, and Published states, from setup to release. Each measurement period, the published campaign generates a campaign cycle that carries the actual data collection workflow. A cycle moves through Data collection, Approval, and Closed states, tracking every metric in the cycle together. When bulk actions are enabled, tasks within a cycle are submitted or approved together. This advances the cycle to its next state as a single unit instead of task by task.

Data owners and approvers are configured separately. A data owner, a single user or group, receives all metric data tasks for the campaign. A campaign supports one or more approver levels that approve in sequence through the GRC: Approver Configurator application. Campaigns support both small, site-level collections and larger, global collections spanning many entities and metrics. When a metric belongs to an active, published campaign, its data tasks inherit the campaign's due date offset and link to the campaign cycle instead of generating independently. This doesn't apply to ad hoc data collection tasks, which generate independently of the campaign cycle, even for metrics in an active campaign.

**Related topics**  


[Enable campaigns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/enable-campaigns.md)

[Create a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/create-a-campaign.md)

[Add or remove entities and metrics from a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/add-or-remove-entities-and-metrics-from-a-campaign.md)

[Configure data owner and approver assignments for a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configure-data-owner-and-approver-assignments-for-a-campaign.md)

[Schedule a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/schedule-a-campaign.md)

[Publish a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/publish-a-campaign.md)

[Submit metric data tasks for a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/submit-metric-data-tasks-for-a-campaign.md)

[Manage metric data tasks for a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/manage-metric-data-tasks-for-a-campaign.md)

