---
title: Configure a default MID Server for each application
description: You can configure a default MID Server that an application can use if all other possible MID Servers are unavailable. You can narrow down the list of applications that are included in the definition of ALL.You can narrow down the list of applications that are included in the definition of ALL.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MID Server selection, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure a default MID Server for each application

You can configure a default MID Server that an application can use if all other possible MID Servers are unavailable. You can narrow down the list of applications that are included in the definition of ALL.

## Before you begin

Role required: agent\_admin or admin

<table id="table_vdg_ns4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

Applications are only available when their respective plugins are activated.

The default MID Server is used when applications fail to find a suitable MID Server that matches configured criteria during auto-select. The default MID Server for the **ALL** application is used if the default MID Server for the specific application is not available. Some applications also offer a property to set the default MID Server.

**Important:** If you configure a MID Server for ALL IP ranges \(type **Include**\) and also create an IP range of type: **Exclude** for the same MID Server, the system ignores the excluded IP range for that MID Server.

The default MID Server does not need to meet any criteria \(application, IP range, behavior, or capability\) to be used. Specifying a default MID Server is optional, and you can use a MID Server as the default for more than one application.

<table id="table_ltp_4qz_5w"><thead><tr><th>

Application

</th><th>

Additional notes

</th></tr></thead><tbody><tr><td>

Discovery

</td><td>

Discovery attempts to use the default MID Server when the Discovery schedule specifies **Auto-Select MID Server** and Discovery cannot find any MID Servers with the correct application and IP range.

</td></tr><tr><td>

Orchestration

</td><td>

Orchestration attempts to use the default MID Server when it cannot find any MID Servers with the capabilities that you define in the Orchestration activity. You can also specify a default MID Server. The value in that property automatically synchronizes with the default MID Server you select in the Orchestration application.

</td></tr><tr><td>

Alert aggregation and RCA

</td><td>

Not applicable. The MID Server is selected if it has the RCA capability. Route to right MID by domain.

</td></tr><tr><td>

Service Mapping

</td><td>

If there are no MID Servers with matching application, capability, or IP range, Service Mapping uses the default MID Server.

</td></tr><tr><td>

Event Management

</td><td>

You can specify a default MID Server for Event Management using the mid.server.connector\_default system property. Event Management does not use the default MID Server in the application record.

</td></tr><tr><td>

Cloud Management

</td><td>

N/A

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Applications**.

    The list of installed applications that can use MID Servers appears.

2.  Click the name of an installed application.

3.  Select a MID Server from the list in the **Default MID Server** field.

4.  To select additional MID Servers for this application, click **Edit** in the **MID Servers** related list and select alternate MID Servers that this application is allowed to use.

5.  Click **Update**.


**Parent Topic:**[MID Server selection](../concept/c_MIDServerSelector.md)

## Select applications to include in the definition of ALL for a MID Server

You can narrow down the list of applications that are included in the definition of ALL.

### Before you begin

Role required: agent\_admin or admin

### About this task

You can specify the ALL application for a MID Server, which means that the MID Server is allowed to work with any of the applications that require MID Servers, such as Discovery, Event Management, Service Mapping, and so on. But you might not want all applications to be included in the definition of ALL. For example, you might want to exclude Service Mapping from the ALL definition if you already have a dedicated MID Server to work with Service Mapping.

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Applications**.

    The list of installed applications that can use MID Servers appear.

2.  If you do not see the **Included in application ALL** column, you can personalize the list and add it.

    ![Included in application ALL](../image/includedInAllApplications.png "Included in application ALL")

3.  For each application, double-click the value in the **Included in application ALL** column.

4.  Change the value to **true** \(to include\) or **false** \(to exclude\).


