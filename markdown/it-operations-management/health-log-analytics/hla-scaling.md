---
title: Scaling Health Log Analytics to stream logs at a higher rate
description: Stream log data to Health Log Analytics in a scalable, more stable way using the advanced ServiceNow infrastructure.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Scaling Health Log Analytics to stream logs at a higher rate

Stream log data to Health Log Analytics in a scalable, more stable way using the advanced ServiceNow infrastructure.

The new ServiceNow architecture leverages queueing technology in IT Operations Management Cloud Services for authentication and log ingestion. The Health Log Analytics AI engine has been enhanced to scale dynamically in response to increased log ingestion by your organization. Health Log Analytics can be scaled to support more than 50,000 events per second \(EPS\) or more than 10,000 [subscription units \(SUs\)](../../it-operations-management/concept/itom-license-module.md).

You can switch to the advanced ServiceNow infrastructure by submitting a scaling request through the Now Support catalog. For more information, see [Submit a Health Log Analytics scale request through the Now Support catalog](../task/hla-scale-request.md). You can also contact your ServiceNow account manager to request scaling. When your scaling request is approved, ServiceNow provisions the number of Elasticsearch and HLA AI Engine nodes required to support your subscription units.

-   **[Submit a Health Log Analytics scale request through the Now Support catalog](../task/hla-scale-request.md)**  
Request Health Log Analytics scaling to support streaming logs at a higher rate. 

**Parent Topic:**[Administering Health Log Analytics](hla-administer.md)

