---
title: Troubleshoot a trace connection
description: Identify why a trace connection is not collecting data by reviewing its execution log and error messages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-troubleshoot-trace-connection.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring trace connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Troubleshoot a trace connection

Identify why a trace connection is not collecting data by reviewing its execution log and error messages.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

Each trace connection record shows an execution log with the result of every collection attempt. When a connection shows an **Error** execution status, you can select the connection to view the log and read the error message.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Traces**.

2.  Select the **Established** sub-tab.

    Each connection card shows its **State** and **Processing state**. A **Processing state** of **Error** indicates that the last collection attempt did not complete successfully.

3.  Select the connection you want to investigate.

4.  In the **Execution logs** section, review the log entries.

    Each log entry shows the following information.

    |Field|Description|
    |-----|-----------|
    |**Start time**|Date and time the collection attempt began.|
    |**End time**|Date and time the collection attempt ended.|
    |**Traces collected**|Number of traces collected during the attempt.|
    |**Execution status**|Result of the collection attempt. A status of **Success** means traces were collected. A status of **Error** means the attempt failed.|
    |**Error message**|Details about a failed collection attempt. Review this message to identify the cause of the error.|


## Result

You have reviewed the execution log and identified the cause of the collection error. Common causes include invalid or expired credentials, an inactive or unvalidated MID Server, and incorrect region or resource ID values.

## What to do next

To update the connection configuration, see [Edit a trace connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-edit-trace-connection.md).

**Parent Topic:**[Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md)

