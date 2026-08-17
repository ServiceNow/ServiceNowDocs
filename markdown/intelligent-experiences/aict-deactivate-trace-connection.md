---
title: Deactivate a trace connection
description: Stop trace collection for an established connection without deleting it, so you can reactivate it later.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-deactivate-trace-connection.html
release: zurich
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring trace connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Deactivate a trace connection

Stop trace collection for an established connection without deleting it, so you can reactivate it later.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Traces**.

2.  On the **Established** sub-tab, select the connection you want to deactivate.

3.  Deactivate the connection using one of the following methods.

<table id="choicetable-deactivate"><thead><tr><th align="left" id="d35422e102">

Method

</th><th align="left" id="d35422e105">

Steps

</th></tr></thead><tbody><tr><td id="d35422e111">

**Actions menu**

</td><td>

1.  Select **Actions** &gt; **Deactivate**.
2.  In the confirmation dialog, select **Deactivate**.


</td></tr><tr><td id="d35422e139">

**Edit form**

</td><td>

1.  Select **Actions** &gt; **Edit**.
2.  Clear the **Active** option.
3.  Select **Save**.


</td></tr></tbody>
</table>
## Result

The connection remains on the **Established** sub-tab with a **State** of **Inactive**. Trace collection stops and no further observability metrics are generated from this connection until it is reactivated.

## What to do next

Reactivate the connection by editing the connection and select the **Active** option.

**Parent Topic:**[Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-trace-connections.md)

