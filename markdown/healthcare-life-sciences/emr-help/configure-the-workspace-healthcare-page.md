---
title: Configure the healthcare record page to support your custom healthcare case type
description: Configure the healthcare record page in Workspace to include your custom case type to display EMR session information.
locale: en-US
release: zurich
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure healthcare case types, Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure the healthcare record page to support your custom healthcare case type

Configure the healthcare record page in Workspace to include your custom case type to display EMR session information.

## Before you begin

Role required: admin

Set your scope to Healthcare and Life Sciences Service Management Core.

## About this task

Video showing how to configure a HCLS Case request definition to support the newly created healthcare case type.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In Experiences, open **CSM/FSM Configurable Workspace**.

3.  In **Pages and Variants** &gt; **Record**, click on **Healthcare record page voltron**.

4.  Toggle the **Settings** button.

5.  In Conditions, under Variant conditions, append an additional OR statement that includes your new healthcare case type name: `^ORtable=<your table name>`

    For example:

    ```
    table=sn_hcls_patient^ORtable=sn_hcls_case^ORtable=sn_hcls_emr_case
    ```

    **Note:** To find your healthcare case type table name, navigate to All &gt; System Definition &gt; Tables and search for your new Healthcare Case type. The table name is displayed in the Name column.

6.  Click **Save**.


## Result

You have now configured Workspace to include your custom healthcare case type.

