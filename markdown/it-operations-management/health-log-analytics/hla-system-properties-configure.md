---
title: Configure global Health Log Analytics system properties
description: Configure global Health Log Analytics system properties if you need to alter the default values, which should not usually be necessary.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure system properties for a single log source, Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure global Health Log Analytics system properties

Configure global Health Log Analytics system properties if you need to alter the default values, which should not usually be necessary.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Changing Health Log Analytics system properties affects back-end processes and can produce unexpected results. Therefore, if you need to make changes to these properties, keep a record of your adjustments. For example, note the value before and after a modification and the time of the change.

**Note:** To modify a Health Log Analytics system property whose **Requires restart** value is **true**, contact ServiceNow support to modify it for you.

For a complete description of all the Health Log Analytics system properties, see the [HLA System Properties \[KB0869842\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0869842) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Health Log Analytics Administration** &gt; **System Properties**.

2.  Select a property with the scope Source.

3.  In the **Value** field, enter the appropriate value.

4.  Select **Update**.

    The setting will apply to log sources created from this point forward.

5.  Determine the scope of application of the new setting.

    -   To apply the setting only to log sources created from this point forward, select **Update**.
    -   To override values for this property in all existing log sources and apply the modified setting to all new log sources, select **Override source property**.

**Parent Topic:**[Configure Health Log Analytics system properties for a single log source](hla-system-properties-configure-single.md)

**Related topics**  


[Configure Health Log Analytics system properties for a single log source](hla-system-properties-configure-single.md)

