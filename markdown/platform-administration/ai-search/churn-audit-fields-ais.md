---
title: List of AI Search Datasource Churn Audit fields
description: Field descriptions for the AI Search Datasource Churn Audit table, which lists fields that AI Search has flagged as high-churn.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/churn-audit-fields-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [churn audit]
breadcrumb: [High-churn field detection, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# List of AI Search Datasource Churn Audit fields

Field descriptions for the AI Search Datasource Churn Audit table, which lists fields that AI Search has flagged as high-churn.

For steps on using this data to make an indexing decision, see [Review high-churn field audit results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/review-churn-audit-results-ais.md).

<table id="table-churn-audit-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Datasource**

</td><td>

The indexed source that covers the flagged field's source table.

</td></tr><tr><td>

**Source**

</td><td>

The source table the flagged field belongs to.

</td></tr><tr><td>

**Field**

</td><td>

The name of the flagged field.

</td></tr><tr><td>

**Field Type**

</td><td>

A snapshot of the field's dictionary type at the time it was detected. This value is retained even if the field is later dropped from the table.

</td></tr><tr><td>

**Occurrence Count**

</td><td>

The number of times the field appeared in indexing activity during the current detection window.

</td></tr><tr><td>

**Frequency Score**

</td><td>

How many distinct days the field churned during the detection window, banded as **Low**, **Medium**, or **High**. See **Churn Score** for the combined triage signal.

</td></tr><tr><td>

**Field Type Score**

</td><td>

A 0–100 score reflecting how strongly the field's data type suggests it's a poor search candidate. See **Churn Score** for the combined triage signal.

</td></tr><tr><td>

**Churn Score**

</td><td>

The lower of the **Field Type Score** band and the **Frequency Score** band.**Churn Score** is automatically set to **Blocked** if Safety Guard detects that any ACL, search source, or result improvement rule depends on the field. This setting overrides the band derived from **Field Type Score** and **Frequency Score**. For details, see [High-churn field detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/high-churn-field-detection-ais.md).

</td></tr><tr><td>

**Has ACL Dependency**

</td><td>

Whether an ACL references this field, either by naming convention or in its condition.

</td></tr><tr><td>

**Has Search Source Filter Dependency**

</td><td>

Whether a search source's filter condition references this field.

</td></tr><tr><td>

**Has RIR Dependency**

</td><td>

Whether a result improvement rule's field boost action references this field. This checks result improvement rules that are still in Draft state as well as published rules.

</td></tr><tr><td>

**Stats Window Start**

</td><td>

The start of the detection window this record's scores were calculated from. Empty on the very first detection run.

</td></tr><tr><td>

**Stats Window End**

</td><td>

The end of the detection window this record's scores were calculated from.

</td></tr><tr><td>

**Detection Note**

</td><td>

A short, system-generated explanation of the field's type, score, and any Safety Guard dependency found for it.

</td></tr><tr><td>

**Admin Decision**

</td><td>

The only field an administrator sets directly. Values are **Pending**, **Exclude From Indexing**, and **Continue Indexing**.When **Churn Score** is **Blocked**, this field can't be set to any value other than **Pending**.

</td></tr><tr><td>

**Decided By**

</td><td>

The user who set the current **Admin Decision**.

</td></tr><tr><td>

**Decided On**

</td><td>

The date and time the current **Admin Decision** was set.

</td></tr></tbody>
</table>**Parent Topic:**[High-churn field detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/high-churn-field-detection-ais.md)

