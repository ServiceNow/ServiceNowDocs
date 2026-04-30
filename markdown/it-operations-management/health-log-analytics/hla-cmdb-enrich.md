---
title: Add log-based CIs to the CMDB in Health Log Analytics
description: Keep the Configuration Management Database \(CMDB\) updated with host data Health Log Analytics discovered in your logs by adding log-based configuration items \(CIs\) to the database.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Enrich the CMDB with host data from logs, Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Add log-based CIs to the CMDB in Health Log Analytics

Keep the Configuration Management Database \(CMDB\) updated with host data Health Log Analytics discovered in your logs by adding log-based configuration items \(CIs\) to the database.

## Before you begin

This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). You can use it on the ServiceNow AI Platform using the Rome Patch 6 release \(scheduled to be released on January 27, 2022\) or later.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Health Log Analytics Administration** &gt; **Log-Based CI Candidates**.

2.  Handle a single CI candidate or multiple CI candidates together.

<table id="choicetable_ywx_ypy_qrb"><thead><tr><th align="left" id="d75630e101">

Option

</th><th align="left" id="d75630e104">

Procedure

</th></tr></thead><tbody><tr><td id="d75630e110">

**Take action on a single CI candidate**

</td><td>

1.  Select a CI candidate record and review the information on the form.

For field descriptions, see [Log-based CI candidates fields in Health Log Analytics](../reference/hla-cmdb-enrich-fields.md).

2.  Add the CI candidate to the CMDB or delete it.
    -   If the CI candidate is appropriate, either add it to the CMDB as is or include more information in it before adding it to the CMDB.

        -   To add the CI candidate to the CMDB as is, select **Add to CMDB** and then select **Continue**.
        -   To add more information, select **Edit additional CI fields**. Enter data that was not extracted from the logs, such as the name of the company associated with the CI, and then select **Submit**.
The CI is added to the CMDB. In the CMDB table for the relevant class type, the discovery source for the new CI is Health Log Analytics. The CI candidate record is automatically deleted from the Log-based CI candidates table.

    -   If the CI candidate is irrelevant, delete it by selecting **Delete**.


</td></tr><tr><td id="d75630e180">

**Take action on multiple CI candidates at the same time**

</td><td>

**Note:** This option does not enable you to add extra information to the selected CIs.

 -   Add multiple CIs to the CMDB.
    1.  In the Log-based CI candidates table, select the CI candidates you want to add to the CMDB.
    2.  From the Actions on selected rows list at the bottom of the page, select **Add to CMDB**.

The selected CIs are added to the CMDB. The CI candidate records are automatically deleted from the Log-based CI candidates table.

-   Delete multiple CI candidates.
    1.  In the Log-based CI candidates table, select the CI candidates you want to delete.
    2.  From the Actions on selected rows list at the bottom of the page, select **Delete**.


</td></tr></tbody>
</table>
**Parent Topic:**[Enhancing the CMDB with host data Health Log Analytics found in logs](../concept/hla-cmdb-enrich-concept.md)

