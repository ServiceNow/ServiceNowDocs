---
title: Create event field mappings
description: Use event field mappings to map values from specific event fields to values in other fields to provide more comprehensive information in an alert. Use team-based integrations in event rules to make sure that connector ownership and execution of rules give precedence to global rules. Teams can maintain consistency and hierarchy while offering flexibility and customization options.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 14
breadcrumb: [Event field mapping configuration, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Create event field mappings

Use event field mappings to map values from specific event fields to values in other fields to provide more comprehensive information in an alert. Use team-based integrations in event rules to make sure that connector ownership and execution of rules give precedence to global rules. Teams can maintain consistency and hierarchy while offering flexibility and customization options.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Create the rule to match the event by its class and original values. Also, specify the new values to replace the original values in the event.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Field Mapping**.

2.  Select **New** or open an existing rule to edit and fill in the fields.

    ![Event field mapping](../image/event-mapping-rule.png "Event field mapping")

<table id="table_EventFieldMappingForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Event field mapping name.

</td></tr><tr><td>

Source

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

Order

</td><td>

Number to define the order in which this action should be processed. Actions with lower numbers are processed first.

</td></tr><tr><td>

Assignment group

</td><td>

For Team-based integrations, select an assignment group. If no assignment group is defined in the event field-mapping rule, then this rule is considered global.

When the rules are running – first the global rules run and then the rules that belong to the assignment group that the event’s source instance belongs to.

</td></tr><tr><td>

Mapping type

</td><td>

Mapping mechanism that is used to change an event field value. -   **Map field and transform value \(Single field\)**:

Maps the **Source field** value to the matching value in the Transform value pairs \[em\_mapping\_pair\] table and populates the **Target field**. Source and Target fields may be event fields, additional info fields, or alert tags.

-   **Create or update field and set constant value \(Constant\)**:

Sets a constant value to a **Target field**. The **Target field** may be an event field, additional info field, or alert tag.

-   **Map field \(Copy field\)**:

Copies the exact value of a Source field to the specified Target field. The Source and Target fields may be Event field, Additional info field, or alert tags.

-   **Map field and transform value using regex**: Generically maps the value from the Source field to the matching value in the Transform value pairs table and populate the **Target field**. Source and Target fields may be event, additional info, or alert tags fields.
-   **Map field using regex**:

Copies the value from a generically defined **Source field** to the **Target field**. The Source field must be a field from the event additional info field. The Target field may be the field of event, additional info, or alert tag. With this type, you can generically find the name of the Source field by using a regular expression \(regex\).

-   **Map field and copy value from regex group**:

Copies part of the Source field value to the Target field. Source and Target fields may be event fields, additional info fields, or alert tags. Define a regex to specify what part of the **Source field** should be copied.

-   **Advanced mapping using script**:

Implements your own logic for event values transformation by using a script. When the 'Run after binding' check box is selected, the rule is executed after the CI binding phase and uses the dedicated script that also has the sys\_id of the CI in the input parameters.

**Warning:** Complex scripts may affect event processing performance.

-   **Map field from reference table**

Use this rule type to extract a **Source field** value from the selected **Reference table** by matching the **Field to match**value to the **Matching alert field** value and then mapping the **Source field** value to the **Target field**. The **Matching alert field** and the **Target field** may be event fields, additional info fields, or alert tags.

</td></tr><tr><td>

Filter

</td><td>

A condition for event field mapping.Select **Add Filter Condition** or **Add "OR" Clause** to configure multiple conditions.

</td></tr><tr><td>

Active

</td><td>

Activates or deactivates the event field mapping. If possible, find and apply another event field mapping rule.

</td></tr><tr><td>

Run after binding

</td><td>

-   When selected, the rule is executed after the CI binding phase.

-   Use the relevant prefix to retrieve values from the CI record:

    -   **alert\_cmdb\_ci.** to retrieve a field from the CI record. For example: Use 'alert\_cmdb\_ci.assignment\_group’ to populate \(and transform\) an alert 'assignment\_group' field with the value of the CI’s assignment group. Dot-walk to a related record is also possible. For example, use alert\_cmdb\_ci.asset.model
    -   **alert\_cmdb\_ci\_key.** to retrieve a value from the CMDB Tags table. For example, alert\_cmdb\_ci\_key.subscription notes.
**Warning**: Using the 'Run after binding' feature may affect event processing performance.

 **Note:** This check box is displayed only for the following Mapping types: **Map field and transform value \(Single field\)**, **Map field \(Copy field\)**, **Map field and transform value using regex**, **Map field and copy value from regex group**, and **Map field from reference table**.

</td></tr></tbody>
</table>    -   If you selected **Map field and transform value \(Single field\)**, fill in the fields as appropriate.

<table id="table_d2n_plh_wy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source field

</td><td>

Event field to map - includes all event and additional info fields. Note: For Additional info fields use: "additional\_info.&lt;field name&gt;". When the 'Run after binding' check box is selected, you can use the **alert\_cmdb\_ci** and the **alert\_cmdb\_ci\_key** prefixes to receive CI related data.

</td></tr><tr><td>

Target field

</td><td>

Event field where the mapping rule inserts or updates the value. When this field is identical to the **Source field**, the mapping rule updates the value in memory of the event field. Alert tags can also be defined by using the **&lt;t\_&gt;** prefix.

</td></tr><tr><td>

Run after binding

</td><td>

-   When checked, activates Event field mapping after CI binding.
-   Use the following prefix to retrieve values from the CI record:

    -   **alert\_cmdb\_ci.** to retrieve a field from the CI record. For example, use 'alert\_cmdb\_ci.assignment\_group’ to populate \(and transform\) an alert 'assignment\_group' field with the value of the CI’s assignment group. Dot-walk to a related record is also possible. For example, use alert\_cmdb\_ci.asset.model
    -   **alert\_cmdb\_ci\_key.** to retrieve a value from the CMDB Tags table. For example, alert\_cmdb\_ci\_key.subscription notes.
**Warning**: Using the 'Run after binding' feature may affect event processing performance.

</td></tr></tbody>
</table><table id="table_kg4_twv_ytb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key

</td><td>

Value that the mapping rule searches for. Whenever the event field has this value, the mapping rule adds the value listed in the **Source field** field to the field listed in the **Target field**. This field is displayed when the **Mapping type** is **Map field and transform value \(Single field\)**. Select **+** to add more **Key** fields, as required.

</td></tr></tbody>
</table>        **Typical use case:** To map the 'event\_severity' field in the additional info field with possible values \[such as WARNING, MINOR, CRITICAL, CLEAR, MAJOR\] to the severity field, configure the following:

        -   Source field: 'event\_severity'
        -   Target field: 'severity'
        -   Transform value pairs:
            -   From value: 'WARNING', to value: '4'
            -   From value: 'MINOR', to value: '3'
            -   and so forth...
    -   If you selected **Create or update field and set constant value \(Constant\)**, fill in the fields as appropriate.

<table id="table_r4p_cmh_wy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target field

</td><td>

The **Target field** may be an an event field, additional info field, or alert tag.

 Typical use case: Set alert severity to 1 for all events that match the filter.

</td></tr><tr><td>

Value

</td><td>

Value you want to use for the **To field**. This field is displayed when the **Mapping type** is **Constant**.

</td></tr></tbody>
</table>        **Typical use case:** Set alert severity to 1 for all events that match the filter.

    -   If you selected **Map field \(Copy field\)**, fill in the fields as appropriate.

<table id="table_uff_rws_qvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source field

</td><td>

**Source field** value to be copied to the **Target field** field. The **Source field** may be an event field, additional info field, or alert tag.

</td></tr><tr><td>

Target field

</td><td>

Event field where the mapping rule inserts or updates the value.The **Target field** may be an event field, additional info field, or alert tag.

</td></tr><tr><td>

Run after binding

</td><td>

-   When checked, activates Event field mapping after CI binding.
-   Use the relevant prefix to retrieve values from the CI record:

    -   **alert\_cmdb\_ci.** to retrieve a field from the CI record. For example, use 'alert\_cmdb\_ci.assignment\_group’ to populate \(and transform\) an alert 'assignment\_group' field with the value of the CI’s assignment group. Dot-walk to a related record is also possible. For example, use alert\_cmdb\_ci.asset.model
    -   **alert\_cmdb\_ci\_key.** to retrieve a value from the CMDB Tags table. For example, alert\_cmdb\_ci\_key.subscription notes.
**Warning**: Using the 'Run after binding' feature may affect event processing performance.

</td></tr></tbody>
</table>        **Typical use case:** To copy the IP field from the event additional info field to the alert field node, use the following:

        -   'Source field': ip
        -   'Target field': node
    -   If you selected **Map field and transform value using regex**, fill in the fields as appropriate.

<table id="table_lnn_pws_qvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source field

</td><td>

Source field value to be copied to the **Target field** field. The **Source field** may be an event field, additional info field, or alert tag.

</td></tr><tr><td>

Target field

</td><td>

Event field where the mapping rule inserts or updates the value.The **Target field** may be an event field, additional info field, or alert tag.

</td></tr><tr><td>

Run after binding

</td><td>

-   When checked, activates Event field mapping after CI binding.
-   Use the relevant prefix to retrieve values from the CI record:

    -   **alert\_cmdb\_ci.** to retrieve a field from the CI record. For example, use 'alert\_cmdb\_ci.assignment\_group’ to populate \(and transform\) an alert 'assignment\_group' field with the value of the CI’s assignment group. Dot-walk to a related record is also possible. For example, use alert\_cmdb\_ci.asset.model
    -   **alert\_cmdb\_ci\_key.** to retrieve a value from the CMDB Tags table. For example, alert\_cmdb\_ci\_key.subscription notes.
**Warning**: Using the 'Run after binding' feature may affect event processing performance.

</td></tr></tbody>
</table>        **Typical use case:** To map severity from the field color in the Additional info field to the Severity field, use:

        -   Source field: 'color'
        -   Target field: 'severity'
        -   Transform value pairs:
            -   From value: '.\*red', To value: '1'. This covers both 'dark red', 'light red', and other values containing 'red' and maps them all to '1'.
            -   and so forth...
<table id="table_a2p_fxs_qvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key

</td><td>

Value that the mapping rule searches for. Whenever the event field has this value, the mapping rule adds the value listed in the **Source field** field to the field listed in the **Target field**. This field is displayed when the **Mapping type** is **Map field and transform value \(Single field\)**. Select **+** to add more **Key** fields, as required.

</td></tr></tbody>
</table>    -   If you selected **Map field using regex**, fill in the fields as appropriate.

<table id="table_nht_pws_qvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source field

</td><td>

Generically defined Source field value to be copied to the **Target field** field. The **Source field** must be a field from the event additional info field. With this type, you can generically find the name of the Source field by using a regular expression \(regex\).

</td></tr><tr><td>

Target field

</td><td>

Event field where the mapping rule inserts or updates the value.The **Target field** may be an event field, additional info field, or alert tag.

</td></tr></tbody>
</table>        **Typical use case:** To map the 'region' field from the additional\_info field that appears as 'tags.region' or 'tags\|region' or 'cloud.region' to an alert tag **t\_region**, use:

        -   'Source field': \*region
        -   'Target field': t\_region
    -   If you selected **Map field and copy value from regex group**, fill in the fields, as appropriate.

<table id="table_tm5_pws_qvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source field

</td><td>

Generically defined Source field value to be copied to the **Target field** field. The Source field must be a field from the event additional info field. With this type, you can generically find the name of the Source field by using a regular expression \(regex\).

</td></tr><tr><td>

Target field

</td><td>

Event field where the mapping rule inserts or updates the value.The **Target field** may be an event field, additional info field, or alert tag.

</td></tr><tr><td>

Run after binding

</td><td>

-   When checked, activates Event field mapping after CI binding.
-   Use the relevant prefix to retrieve values from the CI record:

    -   **alert\_cmdb\_ci.** to retrieve a field from the CI record. For example, use 'alert\_cmdb\_ci.assignment\_group’ to populate \(and transform\) an alert 'assignment\_group' field with the value of the CI’s assignment group. Dot-walk to a related record is also possible. For example, use alert\_cmdb\_ci.asset.model
    -   **alert\_cmdb\_ci\_key.** to retrieve a value from the CMDB Tags table. For example, alert\_cmdb\_ci\_key.subscription notes.
**Warning**: Using the 'Run after binding' feature may affect event processing performance.

</td></tr><tr><td>

Regex group expression

</td><td>

.\*\_.\*\_\(.\*\)\_.\*

</td></tr></tbody>
</table>        **Typical use case:** To extract the third octet from the IP and save it in the additional info **third\_octet** field, use:

        -   'Source field': ip
        -   'Target field': third\_octet
        -   'Regex group expression': .\*\_.\*\_\(.\*\)\_.\*
    -   If you selected **Advanced mapping using script**, fill in the fields as appropriate.

<table id="table_vtv_pws_qvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script

</td><td>

The code editor gives text editor support for inline scripts. The code editor has these features for the supported language services and Inline scripts: Syntax coloring, indentation, line numbers, and automatic creation of closing braces and quotes, Auto-suggestions, and auto-completions.Editing tips:

-   To insert a fixed space anywhere in your code, press the Tab key.
-   To indent a single line of code, select in the leading white space of the line and then press Tab.
-   To indent one or more lines of code, select the code and then press Tab.
-   To decrease the indentation, press Shift+Tab.
-   To remove one tab from the start of a line of code, select in the line and press Shift+Tab.
-   To declare variables, use the var keyword so that they remain within the proper JavaScript scope.


</td></tr><tr><td>

Run after binding

</td><td>

When the 'Run after binding' check box is selected, the rule is executed after the CI binding phase and uses the dedicated script that also has the sys\_id of the CI in the input parameters.

 **Warning:** Complex scripts may affect event processing performance.

</td></tr></tbody>
</table>    -   If you selected **Map field from reference table**, fill in the fields as appropriate.

<table id="table_jrn_r3g_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reference table

</td><td>

The reference table. Select the table from where the field is to be mapped to the Target field in the event.

</td></tr><tr><td>

Field to match

</td><td>

The field from the Reference table to be matched with the Matching alert field from the event. It’s used to filter out the Reference table records.

</td></tr><tr><td>

Source field

</td><td>

**Source field** value to be copied to the **Target field** field. The **Source field** is the field of the table that was selected as the Reference table.

</td></tr><tr><td>

Matching alert field

</td><td>

Event field to find matching Reference table records. The **Matching alert field** is matched with the **Field to match** field.

The Matching alert field may be the Event field, Additional info field, or the Alert tag.

</td></tr><tr><td>

Target field

</td><td>

Event field where the mapping rule inserts or updates the value.The **Target field** may be an event field, additional info field, or alert tag.

</td></tr><tr><td>

Run after binding

</td><td>

-   When checked, activates Event field mapping after CI binding.
-   Use the relevant prefix to retrieve values from the CI record:

    -   **alert\_cmdb\_ci.** In the **Matching alert field**, to retrieve a value of a field from a CI record. For example: 'alert\_cmdb\_ci.ip\_address’ retrieves IP address information of bound CIs. When the **Matching alert field** and the **Field to match** fields are reference fields, dot-walking to sys\_id in the **Matching alert field** is required. For example, to use the 'assignment\_group' value of bound CIs to match with the **Field to match** field, use the following expression in the **Matching alert field**: alert\_cmdb\_ci.assignment\_group.sys\_id
    -   **alert\_cmdb\_ci\_key.** to retrieve a value from the CMDB Tags table. For example, alert\_cmdb\_ci\_key.subscription notes.
**Warning**: Using the 'Run after binding' feature may affect event processing performance.

</td></tr></tbody>
</table>        **Typical use case:** Extract 'short\_description' from the 'pc\_vendor\_cat\_item' records matching its 'name' field with the 'cat\_item\_name' field in the Additional info field of the event and map it to the 'description' field on the event in the following fields:

        -   'Reference table': pc\_vendor\_cat\_item
        -   'Field to match': name
        -   'Source field': short\_description
        -   'Matching alert field': cat\_item\_name
        -   'Target field': description
3.  Right-click the form header and select **Save**.

4.  Select **Submit**.


## Example

The following values comprise a predefined rule that is applied to events in the Trap From Enterprise 9 class. If the events contain the `snmpTrapOID` element with a value of `iso.org.dod.internet.private.enterprises.cisco.0.0`, the mapping rule changes the value to `reload` in the alerts. If the events contain the `snmpTrapOID` element, a value of `iso.org.dod.internet.private.enterprises.cisco.0.1`, the mapping rule changes the value to `tcpConnectionClose` in the alerts.

<table id="simpletable_lvs_5hf_jt"><thead><tr><th>

Field

</th><th>

Values

</th></tr></thead><tbody><tr><td>

Name

</td><td>

cisco.snmpTrapOID

</td></tr><tr><td>

Source

</td><td>

Trap From Enterprise 9

</td></tr><tr><td>

Mapping type

</td><td>

Map field and transform value \(Single field\).

</td></tr><tr><td>

Source field

</td><td>

snmpTrapOID

</td></tr><tr><td>

Target field

</td><td>

snmpTrapOID

</td></tr><tr><td>

Transform Value Pairs

</td><td>

-   Pair 1
    -   **Key**: iso.org.dod.internet.private.enterprises.cisco.0.0
    -   **Value**: reload
-   Pair 2
    -   **Key**: iso.org.dod.internet.private.enterprises.cisco.0.1
    -   **Value**: tcpConnectionClose

</td></tr></tbody>
</table>## What to do next

Test an event field mapping by sending an event that includes a field that is present in the event field mapping.

**Parent Topic:**[Event field mapping configuration](../concept/c_EMEventFieldMapping.md)

