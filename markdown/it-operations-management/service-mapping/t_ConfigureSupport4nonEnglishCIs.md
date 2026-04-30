---
title: Configure support for Windows servers with non-English OS
description: You can configure your ServiceNow AI Platform to support Windows servers that use non-English Windows operating system \(OS\).
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure support for Windows servers with non-English OS

You can configure your ServiceNow AI Platform to support Windows servers that use non-English Windows operating system \(OS\).

## Before you begin

You can perform this procedure only on the MID Servers that serve locations using non-English operating system. Alternatively, you can perform this configuration on all MID Servers in one go, even MID Servers that are used for locations using English operating systems.

Role required: mid\_server

## About this task

If your organization does not deploy Service Mapping, this configuration is not necessary.

Sometimes organizations choose to use operating systems in local languages. While having a localized operating system \(OS\) may be user-friendly, it poses a problem when it comes to automatically discovering Windows servers running the localized OS. During the discovery and mapping process Service Mapping sends discovery commands to Windows servers on your infrastructure via a MID Server. If a Windows server returns a message in a language other than English, Service Mapping does not recognize it as a valid response and the interaction fails.

If your organization uses non-English operating system for some of the Windows servers, you must perform this procedure to make sure that Service Mapping can access all Windows servers, not exclusively Windows servers using the English operating system. This configuration allows the MID Server, that is located between Service Mapping and Windows servers, to recognize a non-English response from a Windows server and to change the language of the CI operating system into English.

This configuration affects only the user for which you perform this procedure.

## Procedure

1.  Navigate to **All** &gt; **MID Servers** &gt; **Properties** in the **Modules** pane.

2.  Click **New**.

3.  In the **Name** field, enter `mid.servicewatch.wmi.mui`.

4.  In the **Value** field, enter `true`.

5.  In the **MID server** field, select the server to which you want to apply this change.

    |Option|Action|
    |------|------|
    |**To apply the change to all MID Servers in your organization**|Leave the MID Server field blank.|
    |**To apply the change to a specific MID Server**|Select the relevant MID Server from the list.|

6.  Click **Submit**.


**Related topics**  


[Resolve pattern-related mapping errors](t_TBSMapProcess.md)

[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

