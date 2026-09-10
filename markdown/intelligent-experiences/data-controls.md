---
title: Data controls
description: Data controls in AI Control Tower enable you to manage how ServiceNow Otto traffic and data are handled across ServiceNow and external datacenters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/data-controls.html
release: australia
topic_type: concept
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Configure ServiceNow AI settings, Configure, AI Control Tower, Enable AI experiences]
---

# Data controls

Data controls in AI Control Tower enable you to manage how ServiceNow Otto traffic and data are handled across ServiceNow and external datacenters.

You can access Data controls from the **Settings** page in AI Control Tower by selecting the **Data controls** tab. Data controls contain two settings: Data sharing and Data overflow processing. Each setting has its own default state and can be opted out of independently.

## Data sharing

Data sharing enables ServiceNow to use anonymized instance data to improve AI model accuracy, enhance user experiences, and better understand business needs.

|Setting|Default|Effect|
|-------|-------|------|
|Data sharing|Active \(on\)|ServiceNow uses anonymized instance data to improve AI model accuracy and products. Opting out does not affect your instance's access to AI features, but your instance no longer contributes data to improve ServiceNow AI products.|

To stop sharing instance data with ServiceNow for AI model improvement, select Opt out on the Data sharing card.

## Data overflow processing

During high-traffic periods, ServiceNow Otto traffic can burst to Microsoft Azure datacenters to maintain performance. Data overflow processing gives you control over this behavior.

If you opt out of data overflow processing, all ServiceNow Otto traffic remains within ServiceNow datacenters. However, opting out can result in processing delays or capacity overflow errors during high traffic periods.

|Setting|Default|Effect|
|-------|-------|------|
|Data overflow processing|Inactive \(off\)|By default, bursting to Azure datacenters is allowed when ServiceNow datacenters experience traffic spikes. Opting in keeps all ServiceNow Otto traffic exclusively within ServiceNow datacenters, but may result in processing delays or capacity errors during high-traffic periods.|

To prevent ServiceNow Otto from bursting to Microsoft Azure datacenters, select Opt out on the Data overflow processing card.

**Note:** The Data sharing and Data overflow processing cards are available for a sub-prod \(managed\) instance in read-only mode, when Multi-instance setup is configured and active.

**Parent Topic:**[Configure ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-ai-settings.md)

