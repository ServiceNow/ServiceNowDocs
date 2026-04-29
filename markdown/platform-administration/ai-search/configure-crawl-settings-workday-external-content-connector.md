---
title: Configure crawl settings for a Workday external content connector
description: Specify the content types you want your Workday external content connector to retrieve.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workday external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Workday external content connector

Specify the content types you want your Workday external content connector to retrieve.

## Before you begin

A connector admin must have already created the Workday external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Workday external content connector](create-ext-cont-connector-workday.md).

A Workday admin must have already completed the preliminary tasks shown in the following table.

|Preliminary task|Description|
|----------------|-----------|
|[Configure Workday security settings](configure-workday-security-settings.md)|Required task.|
|[Configure access to help articles in Workday](configure-public-help-articles-workday.md)|Optional task. Only required if you want the connector to retrieve searchable content and metadata from help articles accessible by all users in your Workday organization.|
|[Configure a payslip report in Workday](configure-payslip-report-workday.md)|Optional task. Only required if you want the connector to retrieve searchable content and metadata from payroll data.|
|[Configure a Learning assignment custom report in Workday](configure-learning-assignment-report-workday.md) and [Get Workday task code for Find Learning Assignments](get-workday-task-code-learning-assignments.md)|Optional tasks. Only required if you want the connector to retrieve searchable content and metadata from Learning assignment data.|
|[Get Workday task code for My Team's Birthday](get-workday-task-code-birthday.md) and [Get Workday task code for My Team Anniversaries](get-workday-task-code-anniversaries.md)|Optional tasks. Only required if you want the connector to retrieve searchable content and metadata from Manager hub data.|

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Workday external content connector crawls the following content types and sends them to AI Search for indexing:

-   Help articles accessible by all users in your Workday organization
-   Benefits information
-   PTO information
-   Vacation policy information

You only need to perform this task if you want to prevent the connector from retrieving one or more of these default content types, or if you want it to retrieve any of the following content types:

-   Payroll information
-   Learning assignments
-   Birthday, anniversary, and PTO request data from Manager Insights Hub

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Workday external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  In the Crawl content types section, deselect the options for any of these content types that you don't want the connector to retrieve from Workday:

    -   **Articles**
    -   **Benefits**
    -   **PTO information**
    -   **Vacation policy**
5.  In the Payroll information section, perform one of the following steps.

    -   If you don't want the connector to retrieve payroll information from Workday, disable the **Crawl payroll information** option.
    -   If you want the connector to retrieve payroll information from Workday, fill in the fields:

<table id="table_l1h_znw_zgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Payslip period date indicator

</td><td>

Workday ID \(WID\) for the period data indicator from the payslip report configured in your Workday tenant.If you don't have this WID, ask your Workday administrator for it.

</td></tr><tr><td>

Payslip report owner user name

</td><td>

User name for the integrated system user account that owns the payslip report configured in your Workday tenant.If you don't have this user name, ask your Workday administrator for it.

</td></tr><tr><td>

Payslip report name XML alias

</td><td>

XML alias for the name of the payslip report configured in your Workday tenant.If you don't have this XML alias, ask your Workday administrator for it.

</td></tr></tbody>
</table>6.  In the Learning assignments section, perform one of the following steps.

    -   If you don't want the connector to retrieve Learning assignments from Workday, disable the **Crawl Learning assignments** option.
    -   If you want the connector to retrieve Learning assignments from Workday, fill in the fields:

<table id="table_g2g_v4w_zgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Learning assignment manager view task code

</td><td>

Task code for the Find Learning Assignments task in your Workday tenant.If you don't have this task code, ask a Workday manager who has access to the Find Learning Assignments task for it. For details on how to find this task code, see [Get Workday task code for Find Learning Assignments](get-workday-task-code-learning-assignments.md).

</td></tr><tr><td>

Learning assignments report owner user name

</td><td>

User name for the integrated system user account that owns the Learning assignments report configured in your Workday tenant.If you don't have this user name, ask your Workday administrator for it.

</td></tr><tr><td>

Learning assignments report name XML alias

</td><td>

XML alias for the name of the Learning assignments report configured in your Workday tenant.If you don't have this XML alias, ask your Workday administrator for it.

</td></tr></tbody>
</table>7.  In the Manager hub data section, perform one of the following steps.

    -   If you don't want the connector to retrieve Manager Insights Hub data from Workday, disable the **Crawl manager Hub data** option.
    -   If you want the connector to retrieve Manager Insights Hub data from Workday, fill in the fields:

<table id="table_q25_2pw_zgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Birthday task code

</td><td>

Task code for the My Team's Birthday task in your Workday tenant.If you don't have this task code, ask a Workday manager who has access to the My Team's Birthday task for it. For details on how to find this task code, see [Get Workday task code for My Team's Birthday](get-workday-task-code-birthday.md).

</td></tr><tr><td>

Anniversary task code

</td><td>

Task code for the My Team Anniversaries task in your Workday tenant.If you don't have this task code, ask a Workday manager who has access to the My Team Anniversaries task for it. For details on how to find this task code, see [Get Workday task code for My Team Anniversaries](get-workday-task-code-anniversaries.md).

</td></tr></tbody>
</table>8.  Select **Save and validate**.


## Result

The Workday external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Workday source system using your modified crawl settings, create and run a one-time content crawl for your Workday external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Workday external content connector](../concept/workday-external-content-connector.md)

