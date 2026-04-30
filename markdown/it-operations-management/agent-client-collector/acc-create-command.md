---
title: Create an Agent Client Collector Security Incident Response command
description: Define a command or command string to be executed on a machine referenced by a security incident. Commands are listed by operating system. For example, a ps command on a Windows OS retrieves the status of active Windows OS processes in the system.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Security Incident Response, Agent Client Collector, IT Operations Management]
---

# Create an Agent Client Collector Security Incident Response command

Define a command or command string to be executed on a machine referenced by a security incident. Commands are listed by operating system. For example, a `ps` command on a Windows OS retrieves the status of active Windows OS processes in the system.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector SIR Integration** &gt; **ACC Integration Commands**.

2.  Select **New**.

    The **ACC Integration Commands - New Record** page appears.

3.  Configure the fields on the page.

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the command.|
    |Operating System|The CI's operating system supported by the Agent Client Collector.|
    |Command|The actual command or command string to be executed.|

4.  To validate that the command you are writing works, select **Test Command**.

    The **Test Command** page appears.

    |Field|Description|
    |-----|-----------|
    |Agent|The specific end-point where the command is run.|

5.  Enter the specific end-point Agent where the result of the test is displayed.

    -   ![successful](../image/acc-create-command-ok.png) If it was successful
    -   ![large](../image/acc-create-command-large.png) too large of an output
    -   ![error](../image/acc-create-command-error.png) or an Error occurred with the error message displayed to the sn\_si.admin.
6.  Select **Submit**


**Parent Topic:**[Agent Client Collector Security Incident Response](../concept/acc-security-incident-response.md)

