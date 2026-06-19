---
title: Use the Script component
description: Write and execute custom Visual Basic \(VB\) scripts by using the Script component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-general-script.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Script component

Write and execute custom Visual Basic \(VB\) scripts by using the Script component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Script component. For more information about these properties, see [Properties of the General components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/Properties-general-components.md).

You can use this component to perform actions that are not covered by existing RPA components or combine actions of multiple components.

For example, you can retrieve a substring from a string by using the VB script in the Script component. You can specify the string and the start character position.

\[Omitted image "general-script-rpa.png"\] Alt text: VB script with the string specified and the start character position in the Script component.

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Script**.

2.  Drag the Script component to the Design surface.

3.  Click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

4.  Under the SCRIPT \(VB.NET\) heading, enter the custom VB script.

5.  To add parameters to the script, do the following steps.

    1.  Click the add parameter icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add parameter icon.\).

    2.  Update the data type of the parameter.

    3.  Repeat the steps to add more parameters.

    A Data In Port is added with each parameter you add.

6.  To set the output data type, under the RETURN TYPE heading, select the data type.

7.  To validate the script, click **Validate**.

    Errors, if any, are shown in the ERRORS section. You must fix all errors before proceeding.

8.  Click **OK** to close the SCRIPT EDITOR window.

9.  Connect the data and control ports of the Script component to the corresponding ports of the other component as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Description

</th><th>

Port type

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Parameter

</td><td>

Enter a value for the parameter or use the value from a previously executed component.

</td><td>

Data In

</td><td>

No. Connecting this port is optional.

</td></tr><tr><td>

Return

</td><td>

Returns the output of the script and passes to the next component.

</td><td>

Data Out

</td><td>

Yes.To view the output, right-click the **Return** field and click **Preview Data**.

</td></tr></tbody>
</table>10. To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[General](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/general-component.md)

