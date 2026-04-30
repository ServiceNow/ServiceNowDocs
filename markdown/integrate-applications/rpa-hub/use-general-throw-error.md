---
title: Use the Throw Error component
description: Raise an exception during the automation process to indicate something incorrect has occurred by using the Throw Error component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Throw Error component

Raise an exception during the automation process to indicate something incorrect has occurred by using the Throw Error component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Throw Error component. For more information about these properties, see [Properties of the General components](../reference/Properties-general-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Throw Error**.

2.  Drag the Throw Error component to the Design surface.

3.  In the Toolbox pane, navigate to **General** &gt; **Try Catch**.

4.  Drag the Try Catch component to the Design surface.

5.  In the Toolbox pane, navigate to **General** &gt; **MessageBox** &gt; **Show**.

6.  Drag the Show component to the Design surface.

7.  Connect the data and control ports of the Throw Error component to the corresponding ports of the other components as described in the following table and image.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port name

</th><th>

Purpose of connection

</th><th>

Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Exception Type

</td><td>

Specify the category of the occurred error.For example, Application.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Message

</td><td>

Provide a detailed description of the error, explaining the issue and the suggestion solution.For example, "There was an error loading the application. Please try again."

</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>    ![The data and control ports of the Throw Error component connected to the corresponding ports of the other components - Try Catch and Show, on the Design surface.](../image/throw-error-comp-rpa-studio.png "Throw Error component")

8.  To test the component, click **Run** from the Design tab.

    ![Output of the Throw Error component.](../image/throw-error-comp-result-rpa-studio.png "Throw Error component result")


**Parent Topic:**[General](../concept/general-component.md)

