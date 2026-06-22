---
title: Assign data anonymization techniques
description: Assign anonymization techniques for data tables or columns, user specific data, or real time data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/dps-assign-anonymization-techniques.html
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Create anonymization policies, Data anonymization, Data privacy, Data Privacy, Platform Privacy]
---

# Assign data anonymization techniques

Assign anonymization techniques for data tables or columns, user specific data, or real time data.

## About this task

Role required: data\_privacy\_admin and admin

## Procedure

1.  Assign anonymization techniques for data tables or columns, user specific data, or real time data.\[Omitted image "bulk-assign-technique.png"\] Alt text: The bulk assign techniques form.

<table id="choicetable_ywk_ywc_dwb"><thead><tr><th align="left" id="d258785e41">

Option

</th><th align="left" id="d258785e44">

Description

</th></tr></thead><tbody><tr><td id="d258785e50">

**Select __Bulk Assign Techniques__**

</td><td>

Applies anonymization to all data records in the chosen data class. Select the data type and the anonymization technique to apply to all entries with the selected data type. Repeat this step for additional bulk assignments of different data types.See [Supported field types for anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/data-privacy-supported-data-types.md) for a list of data types.

</td></tr><tr><td id="d258785e72">

**Select an __anonymization technique__ for each data column record**

</td><td>

Your data privacy processor users can choose which records to anonymize when creating data privacy jobs. Individually apply anonymization to each data record in the chosen data class.

</td></tr></tbody>
</table>    \[Omitted image "assign-technique.png"\] Alt text: Individually assign a technique.

2.  Enter child tables to be scanned.

    Child tables of the parent will be anonymized, if a table has no children this option will not be available.

    **Warning:** A parent job will fail if a child job fails.

3.  If Data Pattern Anonymization is selected, select the anonymization technique to be used.

4.  Set the ordering for data patterns.

5.  **Tip:** Use the **Test** feature to test sample inputs. You can review metrics from the result like scan time, result, and discovered patterns.

    Select the **Test** button to test the policy.

6.  **Important:** All tables must have a correct sys\_dictionary entry.

    Select **Save**.

7.  Select **Publish** to update the anonymization policy for scheduling and be returned to Anonymization policies.

    **Note:** Only published policies can be used for anonymization job scheduling.


## What to do next

[Create anonymization job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/dps-create-anonymization-job.md).

