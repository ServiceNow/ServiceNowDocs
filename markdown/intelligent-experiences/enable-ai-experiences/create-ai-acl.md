---
title: Create AI ACL
description: Create the necessary AI Access Control List \(ACL\) for the component to be called externally.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/create-ai-acl.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Reference, MCP Server Console, Enable AI experiences]
---

# Create AI ACL

Create the necessary AI Access Control List \(ACL\) for the component to be called externally.

## Before you begin

Role required: admin

**Note:** An AI ACL is essential for ensuring security compatibility of the component, regardless of data types or execution logic. This approach embraces a proactive deny-by-default model.

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


**Parent Topic:**[MCP Server Console reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/mcp-server-console-reference.md)

