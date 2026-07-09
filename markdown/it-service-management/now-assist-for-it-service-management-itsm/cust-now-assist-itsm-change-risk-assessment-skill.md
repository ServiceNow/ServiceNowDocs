---
title: Customize the change risk assessment answer generator skill
description: Configure the data that the answer generator skill reads to suggest answers for change risk assessment questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-itsm-change-risk-assessment-skill.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-07-10"
reading_time_minutes: 3
keywords: [Now Assist, generative AI, change risk assessment, AI Risk Data Sources, answer generator]
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize the change risk assessment answer generator skill

Configure the data that the answer generator skill reads to suggest answers for change risk assessment questions.

## Before you begin

Role required: `sn_change_manager`

## About this task

The answer generator skill is active by default and requires no activation. You can customize two aspects that control what data the skill uses to suggest answers:

-   **AI Risk Data Sources**: The skill reads related records and knowledge articles defined as data sources. Create, modify, or deactivate data source records to control what additional data the skill receives. The following six data sources are available out of the box:
    -   Related Affected CIs for change request
    -   Related Impacted Services for change request
    -   Related Impacted Business Applications for change request
    -   Related Service Offerings for change request
    -   Active change tasks linked to change request
    -   Outages linked to change request
-   **Change request fields**: The skill reads a fixed set of fields from the change request record. Add or remove fields by updating a system property.

## Procedure

1.  Navigate to **Change** &gt; **Change Administration** &gt; **AI Risk Data Sources**.

2.  Select **New** to create a data source, or open an existing record to modify it.

3.  Enter a **Name** and **Description** for the data source.

4.  In the **Source** field, select the data source type.

    |Source type|Description|
    |-----------|-----------|
    |Change Request Related Records|Reads records linked to the change request, such as affected configuration items or outages.|
    |Knowledge Articles|Reads policies and standards from knowledge articles. Adds compliance requirements, standards, and policies from your knowledge base to the skill so the skill applies these instructions when answering questions.|

5.  For a **Change Request Related Records** source, configure the data source fields.

    1.  In the **Related Table** field, select the table to retrieve records from.

    2.  In the **Change Reference Field** field, select the field that references the change request and acts as the foreign key.

6.  In the **Max Records** field, enter the maximum number of records to retrieve.

    **Note:** The maximum limit is 100.

7.  In the **Expand Reference Field**, select a field to retrieve the complete details of the referenced record instead of the display value.

    This is useful when the related record uses a many-to-many \(m2m\) relationship, where the actual data lives in a separate record that the current record points to.

    For a **Knowledge Articles** source, specify the conditions that select the articles to include. For example, set a condition on the article number and workflow state so that only published articles are sent to the skill.

8.  In the **Source Condition** field, add conditions to limit the records that the skill receives.

    Conditions remove unrelated data and reduce the prompt size, which lowers the token cost.

9.  To stop retrieving a data source, clear the **Active** check box.

10. Select **Update**.

11. To set which change request fields the skill receives, update the `sn_itsm_gen_ai.com.snc.asmt_answer_generator.change_request_fields` system property.

    1.  Navigate to **All** &gt; **System Properties** &gt; **System Properties**.

    2.  Search for `sn_itsm_gen_ai.com.snc.asmt_answer_generator.change_request_fields` and open the record.

    3.  In the **Value** field, update the comma-separated list of field names.

        For example, add `start_date` to give the skill visibility into additional change request fields.

    4.  Select **Save**.

    To get the change risk assessment answers and reasoning using AI, see [Generate change risk assessment answers by using Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/generate-change-risk-assessment-answers-now-assist.md)


