---
title: Check compatibility of Subflow or Action
description: After establishing the ACL, publish the component and check the compatibility staging table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/check-compatibility-of-subflow.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Reference, MCP Server Console, Enable AI experiences]
---

# Check compatibility of Subflow or Action

After establishing the ACL, publish the component and check the compatibility staging table.

## Before you begin

Role required: admin

## Procedure

1.  Go to Workflow Studio and publish the Subflow.

    You can also run a full compatibility scan via the scheduled job.

2.  Open the compatibility staging table for the relevant Subflow.

3.  Locate your component by name or sort by updated date.

4.  Verify all the three compatibility columns: security\_compatible = true, data\_compatible = true, execution\_compatible = true.

    The overall status should read as compatible. If security\_compatible is false, the other columns will show N/A \(not applicable\). The system uses a fail-fast approach, fix security first, then re-check.

5.  Republish the component after making ACL changes for re-evaluation.

    Once marked as compatible, the component can be added to an MCP server as a tool.


## What to do next

Subflows must be activated for AI use in Flow Designer to be available as MCP tools. Open the subflow, go to Manage Security, enable Callable by Client API, and add a Client Callable Flow Object ACL with execute permission. Skipping this step will prevent the subflow from appearing in the tool creation list.

**Parent Topic:**[MCP Server Console reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/mcp-server-console-reference.md)

