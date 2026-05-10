---
title: Add legal request tables for data indexing
description: Add the legal request tables to be considered for data indexing for AI Search in the Now Assist for Legal Service Delivery \(LSD\) application. The legal request tables are indexed so that you can get relevant AI Search results for the legal records.
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Configure AI Agents]
breadcrumb: [Configure agentic workflow, Configure, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add legal request tables for data indexing

Add the legal request tables to be considered for data indexing for AI Search in the Now Assist for Legal Service Delivery \(LSD\) application. The legal request tables are indexed so that you can get relevant AI Search results for the legal records.

## Before you begin

Set the application scope to **Legal Counsel Center** in the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: admin

## About this task

Include the legal request tables to define them as indexed sources. These added tables are then selected for indexing. For more information on the indexing of sources for AI Search, see [Indexed source retention policies and filter conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/retention-policies-conditions-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  In the Name column, search for `Legal Requests`.

3.  Select the Legal Requests indexed source.

4.  Select **Index All Tables**.


## Result

The legal request tables are indexed for AI Search.

