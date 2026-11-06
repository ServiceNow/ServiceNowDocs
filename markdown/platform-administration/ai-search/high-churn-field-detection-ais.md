---
title: High-churn field detection
description: Some indexed source fields change so frequently that repeatedly reindexing them adds load to AI Search without adding search value. AI Search automatically identifies these high-churn fields and lets an admin decide whether to continue indexing them or to exclude them from the index going forward.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/high-churn-field-detection-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 4
keywords: [high-churn field detection, churn audit]
breadcrumb: [Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# High-churn field detection

Some indexed source fields change so frequently that repeatedly reindexing them adds load to AI Search without adding search value. AI Search automatically identifies these high-churn fields and lets an admin decide whether to continue indexing them or to exclude them from the index going forward.

## Benefits of high-churn field detection

Excluding high-churn fields reduces the frequency and duration of indexing operations, which reduces load on the system. In addition, exclusion helps keeps the index size down, which can improve search performance.

## How high-churn field detection works

A scheduled job analyzes recent indexing activity to find indexed table fields that change unusually often. The job writes or updates one audit record for each candidate field. These audit records are stored in the AI Search Datasource Churn Audit \[ais\_datasource\_churn\_audit\] table.

The audit record's **Admin Decision** field has an initial value of **Pending**. When an administrator reviews the audit record, they can set this field to one of the following values:

-   **Continue Indexing**: The field is indexed normally in future indexing operations. It doesn't appear in future churn audits.
-   **Exclude from Indexing**: The field is excluded from indexing in future indexing operations. It doesn't appear in future churn audits.

When a field is flagged as high-churn, the system continues re-scoring it on each future indexing run as long as its **Admin Decision** field value remains **Pending**. This avoids leaving the field with a stale result when its underlying activity ages out of the churn detection window.

**Note:** The **sys\_class\_name**, **sys\_domain**, **sys\_domain\_path**, **sys\_updated\_on**, **sys\_updated\_by**, and **sys\_mod\_count** system fields are never surfaced as high-churn candidates. Churn for these system fields is expected overhead, not a signal worth reviewing.

## Scoring model

Each candidate field receives two independent scores, banded as **Low**, **Medium**, or **High**:

-   **Field type score**

    How strongly the field's data type suggests it's a poor search candidate. Date/time, numeric, and boolean fields score high; string, journal, and text fields score low, since those typically include actual searchable content.

-   **Frequency score**

    How many distinct days the field churned within the detection window. A field that churns on most days scores higher than one that churned in a single short burst, so a sustained pattern outranks a spike.


The field's overall **Churn Score** is the lower severity of the two bands, meaning it's only **High** when both scores independently agree the field is high-churn. This keeps a field with only one strong signal from being overstated as a top candidate for exclusion.

## Safety Guard dependency checks

For each candidate field, AI Search checks whether any of the following dependency conditions exist:

-   An access control list \(ACL\) references the field, either by naming convention or in its condition
-   A search source's filter condition references the field
-   A field boost action in a result improvement rule references the field

    **Note:** This dependency condition can be satisfied even if the result improvement rule is still in Draft state.


If any of these dependency conditions is satisfied, the field's **Churn Score** is set to **Blocked** regardless of how it scores on field type and frequency. A field that's **Blocked** still appears in the audit list for visibility, but administrators can't change its **Admin Decision** field value from **Pending** to any other value. As a result, the field can never be excluded from indexing by accident.

**Note:** The Safety Guard dependency check can't detect when a field is referenced in a scripted ACL or a Before Query business rule. If either of these conditions is true for a field, don't exclude that field from indexing.

## Related topics

For steps on reviewing flagged fields and specifying whether to continue indexing a field or to exclude it from indexing, see [Review high-churn field audit results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/review-churn-audit-results-ais.md). For a description of the fields found on the audit record, see [List of AI Search Datasource Churn Audit fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/churn-audit-fields-ais.md).

-   **[Review high-churn field audit results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/review-churn-audit-results-ais.md)**  
Review fields that AI Search flagged as high-churn and decide whether to keep indexing them or exclude them from the index.
-   **[List of AI Search Datasource Churn Audit fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/churn-audit-fields-ais.md)**  
Field descriptions for the AI Search Datasource Churn Audit table, which lists fields that AI Search has flagged as high-churn.

**Parent Topic:**[Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/indexed-sources-ais.md)

