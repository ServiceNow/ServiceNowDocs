---
title: Create an AI ACL for a Subflow or Action
description: Create the necessary AI Access Control List \(ACL\) for the component to be called externally.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-ai-acl.html
release: australia
topic_type: task
last_updated: "2026-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Create an AI ACL for a Subflow or Action

Create the necessary AI Access Control List \(ACL\) for the component to be called externally.

## Before you begin

Role required: admin

## About this task

AI ACLs are required for any Subflow or Action to be used as an MCP tool. An AI ACL is essential for ensuring security compatibility of the component, regardless of data types or execution logic. This approach embraces a proactive deny-by-default model. For more information, see the [Understanding invoke\_from\_ai ACL in ServiceNow](https://www.servicenow.com/community/developer-articles/understanding-invoke-from-ai-acl-in-servicenow-ai-agent-flow/ta-p/3519795) article in the ServiceNow Community.

## Procedure

1.  Navigate to navigation filter and enter **Access Control List**.

2.  Select **New**.

3.  Set the **type** to flow\_action.

4.  Set the **Operation** to 'Invoked from AI'.

    This is the critical distinction. A standard record ACL will not work.

5.  In the **Name**, paste the component’s internal name \(scope-qualified, e.g., global.get\_flow\_description\).

    You can find this by publishing the component first, then, checking the three-dot menu or the staging table.

6.  Under **Requires Role**, add sn\_mcp\_server.admin \(or the appropriate role for the MCP server user\).

7.  Submit the ACL.

    Confirm that a record-type ACL isn't created in error, instead of an AI ACL \(invoked from AI operation\). If the staging table still shows security\_compatible = false after publishing, verify the ACL type.


**Parent Topic:**[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-mcp-server-console.md)

