---
title: Create automation source
description: Associate a data source for the selected source type.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring automation summary execution, Configuring Automation Center, Automation Center, Creating integrations with applications]
---

# Create automation source

Associate a data source for the selected source type.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **All** &gt; **Admininstration** &gt; **Automation Center** &gt; **Automation Source Type**.

    The Automation source types page is displayed with a list of existing automation source types.

2.  Select the source type for which you want to create a source.

    The Automation source type page is displayed with the details of the source type.

3.  Select **New** in the Automation Sources section.

    The Automation Source form is displayed.

4.  On the form, fill in the fields.

<table id="id_jw3_jvk_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of the automation source. This name is displayed in the Automation Center dashboard.

</td></tr><tr><td>

Application

</td><td>

The associated application or the application scope in which the source is being created, such as Automation Center or RPA Hub. This is auto-populated.

</td></tr><tr><td>

Source Type

</td><td>

The source type for which you are creating the source. You can edit this field if required.

</td></tr><tr><td>

Internal name

</td><td>

Automation source internal name.

 You can edit this field. Ensure that there are no spaces when you enter a value.

 This field is auto-generated.

</td></tr><tr><td>

Description

</td><td>

Description of the automation source.

</td></tr></tbody>
</table>5.  Select **Submit**.

    **Note:** One automation source type can have multiple sources associated with it.


## What to do next

[Configure execution summary](create-exe-sum-config.md)

**Parent Topic:**[Configuring automation summary execution](../concept/config-auto-sum-exe.md)

