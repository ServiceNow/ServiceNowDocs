---
title: Use the Compare component
description: Compare two string objects that are based on their ASCII values by using the Compare component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the Compare component

Compare two string objects that are based on their ASCII values by using the Compare component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

Compare method is used to compare given text with provided options. If option is matched, it opens the matching control out port.

You can configure the properties for the Compare component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Compare component to the Design surface.

3.  In the Compare component, double click the title bar to launch the Configuration editor.

4.  Select the Add icon \(![Plus icon.](../image/add-image-icon.png)\) to add the string options from the Comparison Options drop-down list.

    For example, select the following options.

    ![Comparison options selected in the configuration window.](../image/compare-options-rpa.png "Comparison options window")

5.  Connect the data and control ports of the Compare component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Name

</th><th>

Purpose of connection

</th><th>

Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Text

</td><td>

Provide text that must be compared with multiple control out ports based on the comparison type.For example, if you provide `hello welcome` as the comparison text, the component compares option 0 and option 1. Since Option 1 starts with hello, it matches with the text provided. Connect this to a MessageBox component to view the output.

![Compare component with text and comparison options, after running this component, the output is displayed using MessageBox component.](../image/compare-text-messagebox-rpa.png "Compare component")

</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>6.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

