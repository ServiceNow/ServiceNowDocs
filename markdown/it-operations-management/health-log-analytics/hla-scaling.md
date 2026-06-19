---
title: Scaling Health Log Analytics to stream logs at a higher rate
description: Stream log data to Health Log Analytics in a scalable, more stable way using the advanced ServiceNow infrastructure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/hla-scaling.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [HLA scaling, log ingestion, events per second, EPS, subscription units, SU, AI engine, queuing technology, log streaming, advanced infrastructure]
breadcrumb: [Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Scaling Health Log Analytics to stream logs at a higher rate

Stream log data to Health Log Analytics in a scalable, more stable way using the advanced ServiceNow infrastructure.

The new ServiceNow architecture leverages queuing technology in IT Operations Management Cloud Services for authentication and log ingestion. The Health Log Analytics AI engine has been enhanced to scale dynamically in response to increased log ingestion by your organization. Health Log Analytics can be scaled to support more than 50,000 events per second \(EPS\) or more than 10,000 [subscription units \(SUs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-license-module.md).

You can switch to the advanced ServiceNow infrastructure by submitting a scaling request through your ServiceNow account manager. When your scaling request is approved, ServiceNow provisions the number of Elasticsearch and AI Engine nodes required to support your subscription units.

