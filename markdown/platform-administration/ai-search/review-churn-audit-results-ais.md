---
title: Review high-churn field audit results
description: Review fields that AI Search flagged as high-churn and decide whether to keep indexing them or exclude them from the index.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/review-churn-audit-results-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 3
keywords: [churn audit, high-churn field detection]
breadcrumb: [High-churn field detection, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Review high-churn field audit results

Review fields that AI Search flagged as high-churn and decide whether to keep indexing them or exclude them from the index.

## Before you begin

Role required: admin

## About this task

AI Search audits fields from indexed tables. If a field is frequently updated, an audit record for it appears in the AI Search Datasource Churn Audit \[ais\_datasource\_churn\_audit\] table. Administrators can review a field's audit record and decide whether to keep indexing the field or to exclude it from future indexing operations.

For background on how high-churn fields are detected and scored, see [High-churn field detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/high-churn-field-detection-ais.md).

## Procedure

1.  Navigate to the AI Search Datasource Churn Audit \[ais\_datasource\_churn\_audit\] table's list view.

    1.  Select **All**.

    2.  In the navigation field, enter `ais_datasource_churn_audit.list`.

    3.  Press Enter.

2.  Select a field audit record with an **Admin Decision** value of **Pending**.

3.  To understand why the field was flagged as high-churn, review the record's **Churn Score**, **Frequency Score**, **Field Type Score**, and **Detection Note**.

    For field descriptions, see [List of AI Search Datasource Churn Audit fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/churn-audit-fields-ais.md).

4.  Set the **Admin Decision** field value for the audit record.

    -   If the audit record's **Churn Score** is **Blocked**, leave the **Admin Decision** as **Pending**.

        **Note:** A blocked field can't be excluded from indexing because the Safety Guard dependency check found at least one ACL, search source filter, or result improvement rule that depends on it being present in the index.

    -   Otherwise, set the audit record's **Admin Decision** field value to **Exclude From Indexing** or **Continue Indexing**.

        **Note:** To undo a previous exclusion decision, you can change an audit record's **Admin Decision** field value from **Exclude From Indexing** to **Continue Indexing**. You can't set this field back to **Pending**, however.

        The Safety Guard dependency check can't detect when a field is referenced in a scripted ACL or a Before Query business rule. If either of these conditions is true for a field, don't exclude that field from indexing.

5.  Select **Update**.


## Result

Future indexing operations exclude fields that you set to **Exclude From Indexing**.

Fields that you set to **Exclude From Indexing** or **Continue Indexing** aren't re-scored in churn audits from future indexing operations.

## What to do next

If you set any field's **Admin Decision** to **Exclude From Indexing**, that field will remain in the index until the source table is reindexed. For details on reindexing content, see [Perform a full table index or reindex for a single AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/index-single-source-ais.md) and [Perform a full table index or reindex for multiple AI Search indexed sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/index-multiple-sources-ais.md).

**Parent Topic:**[High-churn field detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/high-churn-field-detection-ais.md)

