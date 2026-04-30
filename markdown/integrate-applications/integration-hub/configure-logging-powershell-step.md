---
title: Configure logging for the PowerShell step
description: Add log messages to the scripts in your PowerShell step. Use log levels for improved logging and debugging.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [PowerShell step, Integration steps, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configure logging for the PowerShell step

Add log messages to the scripts in your PowerShell step. Use log levels for improved logging and debugging.

## Before you begin

To add log messages to your script, you will need to use the Write-SNCLog function. This function is defined in the IH\\Logging.psm1 module. Use PSScript.ps1 to import this module so inline scripts have access to Write-SNCLog. For more information, see [MID Server PowerShell files](https://www.servicenow.com/docs/access?context=mid-server-powershell-files&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  Set **mid.property.powershell.log\_info** to **true**.

    This property enables or disables logging. For more information, see [PowerShell log property](https://www.servicenow.com/docs/access?context=powershell-log-property&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

3.  Set **mid.property.powershell.ih.log\_level** to the desired log level.

    The log level specifies the threshold required to log a message. Messages are logged at the specified level or higher. For example, if this property is set to WARN, then messages with a level of WARN or ERROR are logged. Messages with a level of INFO, DEBUG, or TRACE are not logged. The levels, listed from low to high, are:

    -   TRACE
    -   DEBUG
    -   INFO
    -   WARN
    -   ERROR
    The default value is INFO.

4.  Configure a system property so that you can view the logs in the instance.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer** &gt; **Properties**.

    2.  Find **Specify the log level of system log entries to replicate to the flow log. The system only replicates log entries of the specified level or higher** and set it to **INFO** or **DEBUG**.

    After the you build and execute the PowerShell script, the logs are available in the MID agent log. Configuring this property also enables you to view them directly in the instance.

    This step sets the **com.glide.hub.flow\_engine.listener\_trace.threshold** property. It replicates the logs to the Flow engine log entries \[sys\_flow\_log\] table.

5.  In your PowerShell script, add log messages and levels with the Write-SNCLog function.

<table id="table_pxf_3lj_dtb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Write-SNCLog function

</td><td>

Log a message for the PowerShell step. Write-SNCLog has two parameters, **-Level** and **-Message**. Both parameters are required, but the parameter names are not. If the names are omitted, the position is used to determine the level and message. Examples: -   `Write-SNCLog -Level WARN -Message "log warning"`
-   `Write-SNCLog WARN "log warning"`
Both of these examples log `WARN: log warning`.

</td></tr><tr><td>

**-Level** parameter

</td><td>

Specify the level for the log message. Valid values are:-   ERROR
-   WARN
-   INFO
-   DEBUG
-   TRACE
This parameter is required.

</td></tr><tr><td>

**-Message** parameter

</td><td>

Specify the message to log. Entered as a string. This parameter is required.

</td></tr></tbody>
</table>6.  Continue building your action or flow, then test and run it.


## What to do next

The new logs are available in the MID agent log and can be downloaded from the MID Server. For more information, see [Download the MID Server files](https://www.servicenow.com/docs/access?context=t_DownloadMIDServerFiles&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

If you set the system property to view the logs in the instance, you can see them in the **Flow engine log entries** tab of the Flow engine context record. For more information, see [Flow execution details](https://www.servicenow.com/docs/access?context=flow-execution-details&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Parent Topic:**[PowerShell step](../../flow-designer/reference/powershell-step-action-designer.md)

**Related topics**  


[Test a credential for the PowerShell step](test-credential-powershell.md)

