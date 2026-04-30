---
title: Control CI attribute updates using Reconciliation rules
description: To prevent specific attributes of a Configuration Item \(CI\) from being overwritten by Discovery or other data sources, use Reconciliation Rules. These rules define which data source is trusted to update a particular attribute when multiple sources provide values.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activate Discrepancy and Reconciliation, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Control CI attribute updates using Reconciliation rules

To prevent specific attributes of a Configuration Item \(CI\) from being overwritten by Discovery or other data sources, use Reconciliation Rules. These rules define which data source is trusted to update a particular attribute when multiple sources provide values.

## Before you begin

Role required: admin

## About this task

Reconciliation Rules are processed by the Identification and Reconciliation Engine \(IRE\) and are essential for maintaining data integrity in the CMDB.

Use Case: If you want to prevent Discovery from updating a set of attributes while allowing another source \(like SCCM or manual entry\) to update them, define a rule that excludes the Discovery source.

**Note:** Only one Reconciliation Rule should be active for a specific CI class and attribute combination to avoid conflicts.

## Procedure

1.  Navigate to **All** &gt; **CI Class Manager**.

2.  Select the target CI class \(e.g., cmdb\_ci\_computer\).

3.  In the **Reconciliation Rules** tab, click **New** to create a rule.

4.  Provide the rule name and select the Discovery source to apply the rule to.

5.  Specify the attributes that this rule will govern.

6.  Set the source precedence to allow only the selected sources to update the specified attributes.


## Result

Certain CI attributes will no longer be updated by untrusted or lower-priority data sources like Discovery. Only the sources defined in the rule \(e.g., SCCM, manual updates\) will be allowed to update those attributes.

**Related topics**  


[Configure attribute value discrepancy in CMDB 360](configure-attribute-value-discrepancy-in-cmdb-360.md)

