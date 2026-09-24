---
title: Content pack for Security Incident Response
description: Using the Process Mining content pack for Security Incident Response, you can analyze inefficiencies through the life cycle of your security incidents. You can use this information to optimize the processes for your security incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/sir-proc-min-content-pack.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Automatic content pack delivery, Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for Security Incident Response

Using the Process Mining content pack for Security Incident Response, you can analyze inefficiencies through the life cycle of your security incidents. You can use this information to optimize the processes for your security incidents.

This content pack loads automatically when SIR is installed on your instance and the relevant tables are present. For more information, see [Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md).

The content pack also extends coverage to the security incident task table \(sn\_si\_task\).

## Templates shipped with content pack

|Content pack|Template name|Table|
|------------|-------------|-----|
|SIR|Standard template for Security Incidents|sn\_si\_incident|
|Field Service Management|Standard template for Work Orders|wm\_order|
|Standard template for Work Order Tasks|wm\_task|

## What you get with this content pack

This content pack analyzes your security incident processes, including related security incident tasks. It gives you visibility into common process issues, such as:

-   Incidents that take longer than expected to resolve
-   Rework, such as incidents that get reopened or bounced back between teams
-   Deviations from the expected process flow
-   Work that stalls with a particular team or agent longer than expected

## End user and roles

If you have the required roles, you can use the Analyst workbench to access the visualized security incident workflow data, and tools for analyzing the data related to security incidents. For more information, see [Analyst workbench page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/analyst-workbench-dashboard.md).

-   Process Mining role: sn\_process\_mining\_analyst
-   Security Incident Response role: sn\_si\_read

**Parent Topic:**[Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md)

