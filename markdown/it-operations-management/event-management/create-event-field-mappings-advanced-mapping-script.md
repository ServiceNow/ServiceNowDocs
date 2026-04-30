---
title: Create event field mappings with advanced mapping script
description: Create event field mappings with advanced mapping scripts to transform raw event data into structured, meaningful information. This method goes beyond basic configurations, aligns fields with business context, and improves event correlation. By reducing alert noise and enhancing visibility, it helps teams respond faster and manage incidents more effectively.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-09-10"
reading_time_minutes: 2
breadcrumb: [Create event field mappings, Event field mapping configuration, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create event field mappings with advanced mapping script

Create event field mappings with advanced mapping scripts to transform raw event data into structured, meaningful information. This method goes beyond basic configurations, aligns fields with business context, and improves event correlation. By reducing alert noise and enhancing visibility, it helps teams respond faster and manage incidents more effectively.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Field Mapping**.

2.  Select New to fill in the form fields or open an existing one to edit the required fields.

3.  In the **Mapping type** field, select **Advanced mapping using script**.

    If you selected **Advanced mapping using script**, fill in the fields as appropriate.

<table id="table_g31_jll_pgc"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

eventGr

</td><td>

glide record

</td><td>

GlideRecord representing the event.

</td></tr><tr><td>

origEventSysId

</td><td>

string

</td><td>

Id of the event.**Note:** The GlideRecord event parameter is a temporary object, and therefore does not contain the id of the original event.

</td></tr><tr><td>

fieldMappingRuleName

</td><td>

string

</td><td>

The name of this field mapping rule.

</td></tr></tbody>
</table>    |Type|Description|
    |----|-----------|
    |boolean|Value is `true` if the binding can proceed successfully, or `false` if the binding operation is aborted.|

4.  Select **Submit**.


## Example

The use case for this script is to automatically enrich incoming events with classification details before they are processed further. For example, by adding u\_alert\_classification = "Network" into the event’s metadata, the system can tag and group network-related alerts more effectively. This helps streamline event correlation, reduce noise, and improve routing so incidents are categorized and resolved faster.

This script checks the event’s additional\_info field, ensures it contains valid JSON, and then updates it by adding a new property called u\_alert\_classification with the value “Network.” If the JSON is invalid, it logs an error and stops the binding. Otherwise, it saves the updated data back to the event record and allows the binding to proceed.

```
try {
        var addInfo = eventGr.getValue('additional_info');
        if (!addInfo) {
            addInfo = "{}";
        }
        var addInfoJson = {};
        // Parse JSON
        try {
            addInfoJson = JSON.parse(addInfo);
        } catch (parseError) {
            gs.error("Error parsing additional_info: " + parseError);
            return false;
        }
        addInfoJson.u_alert_classification = "Network";
        var updatedAddInfo = JSON.stringify(addInfoJson);
        eventGr.setValue('additional_info', updatedAddInfo);
        return true;
    } catch (e) {
        gs.error("The script type mapping rule '" + fieldMappingRuleName + "' ran with the error: \n" + e);
    }

```

**Parent Topic:**[Create event field mappings](t_EMCreateEventFieldMapping2.md)

