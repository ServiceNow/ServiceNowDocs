---
title: Health Log Analytics architecture
description: Health Log Analytics collects logs streaming into your ServiceNow instance from endpoints or data lakes, such as Splunk and Elasticsearch.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics architecture

Health Log Analytics collects logs streaming into your ServiceNow instance from endpoints or data lakes, such as Splunk and Elasticsearch.

The ServiceNow instance receives the logs either via a [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) connector instance or via MID-less Ingest, which supports integration with services such as Amazon Data Firehose. Health Log Analytics identifies and triages anomalies in your log data using unsupervised machine-learning \(ML\) models. It then groups the anomalies together and applies further algorithms to help identify the root cause of the issue.

![Health Log Analytics scaled architecture](../image/MMASSET0021014-health-log-analysis-landing.svg "Health Log Analytics scaled architecture")

**Parent Topic:**[Exploring Health Log Analytics](hla-exploring.md)

