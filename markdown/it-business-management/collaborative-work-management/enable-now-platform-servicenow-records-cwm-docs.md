---
title: Enable ServiceNow AI Platform records in CWM Docs
description: Facilitate connecting work across ServiceNow AI Platform by enabling CWM users to add a reference to records of any ServiceNow table in CWM Docs.
locale: en-US
release: xanadu
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Collaborative Work Management, Strategic Portfolio Management]
---

# Enable ServiceNow AI Platform records in CWM Docs

Facilitate connecting work across ServiceNow AI Platform by enabling CWM users to add a reference to records of any ServiceNow table in CWM Docs.

## Before you begin

Verify that **Application Scope** of your instance is set to **Collaborative Work Management**.

Role required: admin

## About this task

By default, the **sn\_cwm.record\_mention\_config** property is configured to include only CWM task records. To include any other ServiceNow AI Platform record, update the **Value** field of this property.

Watch this video for information about enabling ServiceNow AI Platform records.

Video explaining how to enable Now platform records in CWM. Approximately one minute and 4 seconds long.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  From the Name column, search for and open the **sn\_cwm.record\_mention\_config** property.

3.  Update the **Value** field of the property.

    Include the table name, its label, and the fields that you want displayed for its record in a CWM Doc. For example, you want to include Incident table details. The updated contents of the **Value** field would be:

    ```
    [{"sourceTable":"sn_cwm_task","label":"CWM Task","fields":["short_description","number"]},
    {"sourceTable":"incident","label":"Incident","fields":["short_description","number"]}]
    ```

4.  Repeat step 3 to include other ServiceNow tables.

5.  Select **Update** to save your changes to the property.


## Result

Tables included in the property can now be referenced in CWM Docs of any space.

