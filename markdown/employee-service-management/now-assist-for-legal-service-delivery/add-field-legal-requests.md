---
title: Add fields to the semantic index for legal records
description: Add the description, short description, and legal category field to the semantic index record to be indexed for a semantic search in the Now Assist for Legal Service Delivery \(LSD\) application. During AI Search, the legal records are retrieved based on the description, short description, and legal category fields that are added in the semantic index.
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

# Add fields to the semantic index for legal records

Add the description, short description, and legal category field to the semantic index record to be indexed for a semantic search in the Now Assist for Legal Service Delivery \(LSD\) application. During AI Search, the legal records are retrieved based on the description, short description, and legal category fields that are added in the semantic index.

## Before you begin

Set the application scope to **Legal Counsel Center** in the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: admin

## About this task

These semantic index settings specify how AI Search indexes the content from the indexed source for use with the semantic vector search. For more information on the indexing of sources for AI Search, see [Semantic index configuration for indexed sources](https://www.servicenow.com/docs/access?context=semantic-index-cfg-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  In the Name column, search for `Legal Requests`.

3.  Select the Legal Requests indexed source.

4.  Select the Semantic Index configurations related list.

5.  Select the record **body**.

6.  Select **New**.

7.  In the application picker, set the application scope to **Legal Request Management**.

8.  On the form, fill in the fields.

<table id="table_j4f_qxm_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Semantic Index Name

</td><td>

Name of the semantic index.The **Semantic Index Name** field is automatically set to **body**.

</td></tr><tr><td>

Source

</td><td>

Source table whose value you want to include in the semantic index.The **Source** field is automatically set to **Legal Request**.

</td></tr><tr><td>

Type

</td><td>

Type of object to index for a semantic vector search.From the drop-down list, select **Field**.

</td></tr><tr><td>

Application

</td><td>

Name of the application that the Semantic Index belongs to.The **Application** field is automatically set to **Legal Request Management**.

</td></tr><tr><td>

Order

</td><td>

Order of concatenation for this field's value relative to the values of other semantic index fields that are defined in the same semantic index configuration. The fields with lower values appear first in the concatenation.

</td></tr><tr><td>

Field Name

</td><td>

Name of the legal request field to include in the semantic index.Select the **short-description** field to include in the semantic index.

</td></tr></tbody>
</table>9.  Select **Submit**.

10. Repeat the steps 6 and 7 to add the following fields from the Legal Request \[sn\_lg\_ops\_request\] table.

    -   **description**
    -   **lg-category**
    **Note:** You must add all description, short description, and legal category fields \(**description**, **short\_description**, and **lg-category**\) to the Semantic Index **body** record.


## Result

The description, short description, and legal category fields are indexed for the semantic search.

![Add the description, short description, and legal category field for the semantic search.](../image/adding-fields-semantic-index-record.png "Add fields to the semantic index")

