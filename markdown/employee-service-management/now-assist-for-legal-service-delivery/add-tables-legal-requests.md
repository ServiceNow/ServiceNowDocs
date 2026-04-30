---
title: Add the legal request child tables for indexing
description: Add the legal request child tables to be considered for data indexing for AI Search in the Now Assist for Legal Service Delivery \(LSD\) application. The legal request child tables are indexed so that you can get relevant AI Search results for the legal records.
locale: en-US
release: xanadu
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2025-04-10"
reading_time_minutes: 1
keywords: [Now Assist, Configure AI Agents]
breadcrumb: [Configuring the Triage legal requests agentic workflow, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Add the legal request child tables for indexing

Add the legal request child tables to be considered for data indexing for AI Search in the Now Assist for Legal Service Delivery \(LSD\) application. The legal request child tables are indexed so that you can get relevant AI Search results for the legal records.

## Before you begin

Set the application scope to **Legal Counsel Center** in the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin

## About this task

Include the legal request tables as child tables to define them as indexed sources. These added tables are then selected for indexing. For more information on the indexing of sources for AI Search, see [Indexed source retention policies and filter conditions](https://www.servicenow.com/docs/access?context=retention-policies-conditions-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  In the Name column, search for `Legal Requests`.

3.  Select the Legal Requests indexed source.

4.  In the Condition section, set the filter condition to **\[State\]\[is not\]\[Cancelled\]**.

5.  Select the Child Tables related list.

6.  Add the child tables by selecting **New**.

7.  In the application picker, set the application scope to **Legal Request Management**.

8.  On the form, fill in the fields.

<table id="table_aj3_lqm_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indexed Source

</td><td>

Reference to the indexed source. The **Indexed Source** field is automatically set to **Legal Requests**.

</td></tr><tr><td>

Application

</td><td>

Name of the application that the Indexed Source belongs to.The **Application** field is automatically set to **Legal Request Management**.

</td></tr><tr><td>

Table

</td><td>

Label and name for the child table that you want to enable content indexing for. You can only select from tables that extend the indexed source table.

</td></tr><tr><td>

Active

</td><td>

Option to activate indexing for the child table.

</td></tr></tbody>
</table>9.  Select **Submit**.

10. Select **Index All Tables**, to index the data of the added tables.


## Result

The legal request child tables are indexed for AI Search.

![Enable data indexing for legal request child tables for AI Search.](../image/adding-tables-child-tables.png "Indexing legal request child tables for AI Search")

## What to do next

Define the semantic indexing configuration settings that you want to apply when AI Search indexes the records for a legal request table. For more information, see [Configure the semantic index settings for legal request tables](create-record-legal-requests.md).

