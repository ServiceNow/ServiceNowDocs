---
title: Health Log Analytics architecture
description: Health Log Analytics collects logs streaming into your ServiceNow instance from endpoints or data lakes, such as Splunk and Elasticsearch.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/hla-architecture.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics architecture

Health Log Analytics collects logs streaming into your ServiceNow instance from endpoints or data lakes, such as Splunk and Elasticsearch.

The ServiceNow instance receives the logs either via a MID Server connector instance or via MID-less Ingest, which supports integration with services such as Amazon Data Firehose. Health Log Analytics identifies and triages anomalies in your log data using unsupervised machine-learning \(ML\) models. It then groups the anomalies together and applies further algorithms to help identify the root cause of the issue.

\[Omitted image "MMASSET0021014-health-log-analysis-landing.svg"\] Alt text: Health Log Analytics scaled architecture.

