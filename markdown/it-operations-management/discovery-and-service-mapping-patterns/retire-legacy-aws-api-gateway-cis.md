---
title: Retire legacy AWS API Gateway data model CIs
description: Avoid duplicate AWS API Gateway configuration items \(CIs\) by retiring legacy data model CIs through a scheduled job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/retire-legacy-aws-api-gateway-cis.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 1
breadcrumb: [Amazon API Gateways, AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Retire legacy AWS API Gateway data model CIs

Avoid duplicate AWS API Gateway configuration items \(CIs\) by retiring legacy data model CIs through a scheduled job.

## Before you begin

-   Verify you have at least version 1.29.0 of Discovery and Service Mapping Patterns.
-   Run an AWS discovery to populate the CIs in the managed API data model. For more information, see [Create Discovery schedules for cloud resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-manager.md).

Role required: admin

## About this task

Starting with Discovery and Service Mapping Patterns December release, the Amazon AWS API Gateway pattern data model has changed. To avoid duplicate CIs, activate a schedule job to mark legacy data model CIs as retired.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Name** column, search for `Retire Cloud Gateways migrated to Managed API`.

3.  Select the **Retire Cloud Gateways migrated to Managed API** scheduled job.

4.  Select **Execute Now**.


**Parent Topic:**[Amazon API Gateway discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/aws-api-gateway-discovery.md)

