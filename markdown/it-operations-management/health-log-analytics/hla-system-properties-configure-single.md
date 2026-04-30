---
title: Configure Health Log Analytics system properties for a single log source
description: Configure system properties for a specific log source if you need to alter the default values, which should not usually be necessary.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Health Log Analytics administration, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure Health Log Analytics system properties for a single log source

Configure system properties for a specific log source if you need to alter the default values, which should not usually be necessary.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Changing Health Log Analytics system properties affects back-end processes and can produce unexpected results. Therefore, if you need to make changes to these properties, keep a record of your adjustments. For example, note the value before and after a modification and the time of the change.

**Note:** To modify a Health Log Analytics system property whose **Requires restart** value is **true**, contact ServiceNow support to modify it for you.

For a complete description of all the Health Log Analytics system properties, see the [HLA System Properties \[KB0869842\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0869842) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Log Sources**.

2.  On the **Source properties** tab, right-click a property.

3.  Select **Override property value** from the pop-up menu.

4.  In the **Value** field, enter the appropriate value.

5.  Select **Submit**.


## Result

The new value overrides the previous setting for the selected log source.

-   **[Configure global Health Log Analytics system properties](hla-system-properties-configure.md)**  
Configure global Health Log Analytics system properties if you need to alter the default values, which should not usually be necessary.

**Parent Topic:**[Health Log Analytics administration](../concept/hla-administer.md)

**Related topics**  


[Configure global Health Log Analytics system properties](hla-system-properties-configure.md)

