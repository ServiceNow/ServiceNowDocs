---
title: Configure attribute value discrepancy in CMDB 360
description: Configure attribute comparison settings in CMDB 360 to detect data inconsistencies across multiple discovery sources.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate Discrepancy and Reconciliation, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure attribute value discrepancy in CMDB 360

Configure attribute comparison settings in CMDB 360 to detect data inconsistencies across multiple discovery sources.

## Before you begin

Role required: admin

Confirm that CMDB 360 is enabled and configured in your instance.

## About this task

The following screenshot can help you to set up the fields to identify the discrepancy.![CMDB MultiSource Column Metadata user interface with the fields configured for discrepancy.](../images/set-attribute-discrepancy-value.png)

## Procedure

1.  Navigate to the table **All** &gt; **cmdb\_multisource\_column\_metadata.list**.

2.  Select **New** to create a new record.

3.  In the **MultiSource Column** field, select the attribute to compare.

4.  Select the table to compare the attributes to the fields.

    **Note:** If the table you need isn’t listed, select and hold \(or right-click\) on the Table label and select **Configure Dictionary**.

5.  To configure a dictionary entry, do the following.

    1.  In the dictionary entry, select **View** and then select **Advanced**.

    2.  In the **Attributes** field, set the attributes as `base_start=true` and `allow_public=true`.


## Result

You can use the configured attributes in the CMDB 360 query.

**Related topics**  


[Control CI attribute updates using Reconciliation rules](control-ci-attribute-updates-using-reconciliation-rules.md)

[Generate reports for attribute value discrepancies](use-attribute-value-discrepancy-in-cmdb-360.md)

