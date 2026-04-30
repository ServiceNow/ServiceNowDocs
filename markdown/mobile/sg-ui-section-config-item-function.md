---
title: Configure action functions in a record section
description: Add action functions, like buttons to the footer area of record sections to enable users to trigger functions within a record section and quickly perform repetitive processes. This capability can be added to launcher screens and section screens within a record section.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure a record UI section, Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure action functions in a record section

Add action functions, like buttons to the footer area of record sections to enable users to trigger functions within a record section and quickly perform repetitive processes. This capability can be added to launcher screens and section screens within a record section.

## Before you begin

To configure record section functions within a sections screen, at least one pre-configured record section must be created. For more information, see [Configure a record UI section](sg-ui-section-config-item.md).

Role required: admin

<table id="table_gt3_lkh_fwb"><thead><tr><th>

Vertical buttons within a launcher screen of a record section

</th><th>

Vertical button within a section screen view of a record section

</th></tr></thead><tbody><tr><td>

![Record section with two buttons.](../image/record-section-two-buttons.png)

</td><td>

![Record section with one button.](../image/record-section-one-button.png)

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All**.

2.  In the filter navigator, enter  `sys_sg_section_card_instance.list` to open a list of section card instances.

    This table associates the card instance to the record section.

3.  Select a displayed section card instance.

4.  On the form, fill in the fields.

<table id="table_i2m_mlh_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the section card instance.

</td></tr><tr><td>

Section

</td><td>

Record section associated with the card instance.

</td></tr><tr><td>

Card

</td><td>

Card instance that hosts the action functions.These cards can contain one or more elements. For example, buttons, text block, and icons. Supported action functions include navigation functions, URL links, phone calling ability, open email, open chat, and uploaded attachment.

</td></tr><tr><td>

Application

</td><td>

Pre-populated field that displays the application scope.

</td></tr><tr><td>

Location

</td><td>

The area of the card instance within the record section.

</td></tr><tr><td>

Hide if empty

</td><td>

Option to hide the footer area in the record section when there are no records to display.

</td></tr></tbody>
</table><table id="table_lcl_ym3_fwb"><thead><tr><th>

Function displayed when 'Hide if empty' field is cleared

</th><th>

Function not displayed when 'Hide if empty' field is checked

</th></tr></thead><tbody><tr><td>

![Hide if empty field is unchecked so action function displays.](../image/record-section-unhide.png)

</td><td>

![Hide if empty field is checked so action function does not display.](../image/record-section-hide.png)

</td></tr></tbody>
</table>5.  Select **Submit**.


