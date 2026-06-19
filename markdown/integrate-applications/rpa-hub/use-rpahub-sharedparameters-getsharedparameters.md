---
title: Use the GetSharedParameters component
description: Get the values of multiple shared parameters set up for multiple bot processes on the RPA Hub using the GetSharedParameters component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-rpahub-sharedparameters-getsharedparameters.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Shared Parameters, RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetSharedParameters component

Get the values of multiple shared parameters set up for multiple bot processes on the RPA Hub using the GetSharedParameters component.

## Before you begin

Set multiple shared parameters and associate multiple bot processes on the RPA Hub. For more information, see [Create a shared parameter in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-shared-parameter.md) and [Assign a bot process to a shared parameter in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/assign-botprocess-shared-parameter.md).

Assign the automation to the bot process by using the **Assign bot process** option in the **Design** tab of RPA Desktop Design Studio. For more information, see [Assign bot process to an automation project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/assign-bot-process.md).

Role required: none

## About this task

You can configure the properties for the GetSharedParameters component. For more information about these properties, see [Properties of the shared parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/properties-rpahub-shared-parameters.md).

## Procedure

1.  In the Toolbox pane, navigate to **RPA Hub** &gt; **Shared Parameters**.

2.  Drag the GetSharedParameters component to the Design surface.

3.  Click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

4.  Click the add key icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add key icon.\).

5.  Enter the shared parameter name.

6.  Update the shared parameter data type.

7.  Repeat the steps to set more shared parameters.

8.  Click **OK**.

9.  Connect the data and control ports of the GetSharedParameters component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data Out \(Shared Parameter\)

</td><td>

Returns the value of the shared parameter and passes to the next component.

</td><td>

No. Connecting the port is optional.To view the output, right-click the **Return** field and click **Preview Data**

.

</td></tr><tr><td>

Data In \(Return\)

</td><td>

Returns the values of multiple shared parameters as an object and passes to the next component.

</td><td>

YesTo view the output, right-click the **Return** field and click **Preview Data**

</td></tr><tr><td>

Control In

</td><td>

Connects to the Control Out port of one or more components.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Connects to the Control In port of another component or the default end component.

</td><td>

Yes

</td></tr></tbody>
</table>10. To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Shared Parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/shared-parameters.md)

