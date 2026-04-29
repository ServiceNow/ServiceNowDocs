---
title: Use the SetEnvironmentVariable component
description: Create or update an environment variable as part of an automation Workflow by using the SetEnvironmentVariable component in RPA Desktop Design Studio. These variables persist across activities and can be retrieved later using GetEnvironmentVariable.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Environment, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the SetEnvironmentVariable component

Create or update an environment variable as part of an automation Workflow by using the SetEnvironmentVariable component in RPA Desktop Design Studio. These variables persist across activities and can be retrieved later using GetEnvironmentVariable.

## Before you begin

Role required: none

## About this task

You can configure the properties for the SetEnvironmentVariable component. For more information about these properties, see [Properties of the Environment components](../reference/util-environment-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Environment**.

2.  Drag the SetEnvironmentVariable component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SetEnvironmentVariable component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(variable\)|Takes the environment variable name from a previously executed component.|Yes|
    |Data In \(value\)|Takes the environment variable value from a previously executed component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


## GetEnvironmentVariable component

You want your robot to process files and save logs to different folders depending on whether it's running in Development or Production mode.

1.  At the start of the automation, use SetEnvironmentVariable to define the following variables:

    -   `ENV_MODE = Development`
    -   `LOG_PATH = C:\RPA\Dev\Logs`
    This variable defines if robot is running in the development mode, where to store the log files.

    ![SetEnvironmentVariable with development environment details.](../image/set-env-var-dev-rpa.png)

2.  Later in the workflow, when saving log files, use **GetEnvironmentVariable** to retrieve the value of `LOG_PATH`.

    The robot dynamically stores the log files as per the value in the `LOG_PATH` variable.

3.  In production, simply update the environment variable setup to:

    -   `ENV_MODE = Production`
    -   `LOG_PATH = C:\RPA\Prod\Logs`
    ![SetEnvironmentVariable with production environment details.](../image/set-env-var-prod-rpa.png)

    The robot now logs to the production folder automatically, because it reads the `LOG_PATH` value from the environment variable.


**Parent Topic:**[Environment](../concept/environment-utility.md)

