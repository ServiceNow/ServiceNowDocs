---
title: Create an MCP app
description: Build, register, and display user interfaces along with your tool's logic with MCP apps. This allows you to implement and manage interactive interfaces for your tools that can be displayed by MCP clients.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-an-mcp-app.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 1
keywords: [MCP apps]
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Create an MCP app

Build, register, and display user interfaces along with your tool's logic with MCP apps. This allows you to implement and manage interactive interfaces for your tools that can be displayed by MCP clients.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin \(for configuration\)

## About this task

Create an MCP app and enable MCP tools to deliver interactive user interfaces to hosts. It defines how tools declare UI resources, that hosts render securely in iframes, and how the two communicate.

Create tools as the pre-step before MCP tools creations, so that you can choose one of the created apps while using the tool.

**Note:** The minimum version required is: Zurich patch 9 and Australia patch 2.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the Configuration tab, select **Apps**.

3.  View the tools created from various categories, and their associated attributes.

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

Permissions

</td><td>

Access granted to different browsers and devices needed to create the app. The options are microphone, camera, geolocation and clipboard.

</td></tr></tbody>
</table>5.  Select **Add reference** to add references to the HTML files that will be used to style, script or define the logic your app.

6.  Add details in the form:

    \[Omitted image "mcp-server-apps-ref.png"\] Alt text: Add a reference

    1.  Declare the link to the external connection or resources to be referred.

    2.  Select **Type** of the reference.

    3.  Add link to the **Library**.

7.  Add link to the HTML file containing the interactive interface in 'Attachments'.


## What to do next

Create an MCP tool and add one of these apps, created to render an interactive user experience displayed by the MCP client.

**Parent Topic:**[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-mcp-server-console.md)

