---
title: Create an MCP app
description: Model Context Protocol apps is an extension that enable you to deliver interactive experience through the MCP tools by building, registering, and serving UI alongside their tool logic. Implement and manage interactive interfaces for your tools, designed for display by MCP clients.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-an-mcp-app.html
release: zurich
topic_type: task
last_updated: "2026-06-17"
reading_time_minutes: 1
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Create an MCP app

Model Context Protocol apps is an extension that enable you to deliver interactive experience through the MCP tools by building, registering, and serving UI alongside their tool logic. Implement and manage interactive interfaces for your tools, designed for display by MCP clients.

## Before you begin

Role required: admin

## About this task

Create an MCP app and enable MCP servers to deliver interactive user interfaces to hosts. It defines how servers declare UI resources, that hosts render securely in iframes, and how the two communicate.

**Note:** The minimum version required is: Zurich patch 9 and Australia patch 2.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console** &gt; ****.

2.  From the Configuration tab, select **Apps**.

3.  View and manage the tools created from various categories, and their associated attributes.

4.  Select **Create app**.

    \[Omitted image "mcp-server-create-apps.png"\] Alt text: Create MCP apps

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

An internal name for the app.

</td></tr><tr><td>

Name

</td><td>

The name of the app generated automatically based on the label you enter.

</td></tr><tr><td>

Description

</td><td>

The description of what the app intends to do. This input is exposed to AI clients and used to determine when to use this app.

**Note:** Admins must add specific and action-oriented description as the AI clients access it to decide when to call the app.

</td></tr><tr><td>

Permission

</td><td>

Access granted to the microphone and camera among other tools needed to create the app.

</td></tr><tr><td>

References

</td><td>

References to the HTML files that will be used to style, script or define the logic your app.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configuring-mcp-server-console.md)

