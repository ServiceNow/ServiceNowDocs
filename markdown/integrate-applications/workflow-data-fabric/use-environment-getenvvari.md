---
title: Use the GetEnvironmentVariable component
description: Retrieve the value of an environment variable by using the GetEnvironmentVariable component in RPA Desktop Design Studio. For example, you can get the value of the TEMP variable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-environment-getenvvari.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Environment, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetEnvironmentVariable component

Retrieve the value of an environment variable by using the GetEnvironmentVariable component in RPA Desktop Design Studio. For example, you can get the value of the TEMP variable.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetEnvironmentVariable component. For more information about these properties, see [Properties of the Environment components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/util-environment-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Environment**.

2.  Drag the GetEnvironmentVariable component to the Design surface.

3.  To configure the input field, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

4.  Connect the data and control ports of the GetEnvironmentVariable component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(variable\)

</td><td>

Takes the environment variable through the Data Out port of another component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the value of the specified environment variable and passes to another component.

</td><td>

Yes.To preview the data, right-click the **Return** field and click **Preview Data**.

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

No. Connecting the port is optional.

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


## GetEnvironmentVariable component

You want your robot to process files and save logs to different folders depending on whether it's running in Development or Production mode.

1.  At the start of the automation, use SetEnvironmentVariable to define the following variables:

    -   `ENV_MODE = Development`
    -   `LOG_PATH = C:\RPA\Dev\Logs`
    This variable defines if robot is running in the development mode, where to store the log files.

    \[Omitted image "set-env-var-dev-rpa.png"\] Alt text: SetEnvironmentVariable with development environment details.

2.  Later in the workflow, when saving log files, use **GetEnvironmentVariable** to retrieve the value of `LOG_PATH`.

    The robot dynamically stores the log files as per the value in the `LOG_PATH` variable.

3.  In production, simply update the environment variable setup to:

    -   `ENV_MODE = Production`
    -   `LOG_PATH = C:\RPA\Prod\Logs`
    \[Omitted image "set-env-var-prod-rpa.png"\] Alt text: SetEnvironmentVariable with production environment details.

    The robot now logs to the production folder automatically, because it reads the `LOG_PATH` value from the environment variable.


**Parent Topic:**[Environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/environment-utility.md)

