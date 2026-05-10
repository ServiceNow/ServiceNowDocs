---
title: Configure the semantic index settings for legal request tables
description: Configure the semantic index settings to define how AI Search indexes the content from the legal request tables in the Now Assist for Legal Service Delivery \(LSD\) application.
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Configure AI Agents]
breadcrumb: [Configure agentic workflow, Configure, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure the semantic index settings for legal request tables

Configure the semantic index settings to define how AI Search indexes the content from the legal request tables in the Now Assist for Legal Service Delivery \(LSD\) application.

## Before you begin

Set the application scope to **Legal Counsel Center** in the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: admin

## About this task

These semantic index settings specify how AI Search indexes the content from the indexed source for use with the semantic vector search. For more information on the indexing of sources for AI Search, see [Semantic index configuration for indexed sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/semantic-index-cfg-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  In the Name column, search for `Legal Requests`.

3.  Select the Legal Requests indexed source.

4.  Select the Semantic Index configurations related list.

5.  Add the semantic index configuration by selecting **New**.

6.  On the form, fill in the fields.

<table id="table_zwv_w5m_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the semantic index.In the **Name** field, enter `body`.

</td></tr><tr><td>

Embedded Models

</td><td>

List of the embedded models to use for the semantic index configuration.The **Embedded Models** field is automatically set to **Embedded Models**.

</td></tr><tr><td>

Active

</td><td>

Option to make the semantic index configuration active for your instance. AI Search ignores inactive semantic index configurations when indexing content from the specified index source.

</td></tr><tr><td>

Indexed Source

</td><td>

Reference to the AI Search indexed source that you want to apply this semantic index configuration to.The **Indexed Source** field is automatically set to**Legal Counsel Center**.

</td></tr><tr><td>

Application

</td><td>

Name of the application to which the semantic index belongs.The **Application** field is automatically set to **Legal Counsel Center**.

</td></tr></tbody>
</table>7.  Select **Submit**.


## Result

The data from the legal request tables are indexed for AI Search according to the semantic index settings.

![Configure semantic index record to determine how AI Search indexes content from the legal request tables.](../image/lsd-agentic-add-semantic-record.png "Semantic index record")

## What to do next

Add fields to the semantic index record by selecting **body**. For more information, see [Add fields to the semantic index for legal records](add-field-legal-requests.md).

