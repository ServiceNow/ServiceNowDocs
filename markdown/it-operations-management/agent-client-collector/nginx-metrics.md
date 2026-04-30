---
title: Nginx metrics
description: The following table lists the metrics that are gathered as output from Nginx checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Nginx metrics

The following table lists the metrics that are gathered as output from Nginx checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|nginx.active\_connections \(featured metric\)|admin|count|Total number of connections opened on the server, including waiting connections \(**nginx.waiting** value\). It reflects the number of current users on the website. There can be multiple connections opened for a single user.|
|nginx.accepts \(featured metric\)|admin|count|Represents the total established connections when `https://yoursite.com/nginx_status` is triggered.|
|nginx.handled \(featured metric\)|admin|count|Total number of connections handled by the Nginx server.|
|nginx.requests \(featured metric\)|admin|count|Total number of requests handled by the Nginx server.|
|nginx.reading \(featured metric\)|admin|count|Current number of connections where Nginx server is reading the request header.|
|nginx.writing \(featured metric\)|admin|count|Represents the current number of connections where the Nginx server is writing the response back to the client.|
|nginx.waiting \(featured metric\)|admin|count|Number of idle client connections waiting for a request.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

