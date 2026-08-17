---
title: Connect ServiceNow® AI Experience Lab for VS Code extension to an instance
description: Connect the ServiceNow® AI Experience Lab for VS Code extension to your ServiceNow instance to access instance files, deploy changes, and preview your work.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [ServiceNow AI Experience Lab for VS Code, VS Code, instance connection, authentication]
---

# Connect ServiceNow® AI Experience Lab for VS Code extension to an instance

Connect the ServiceNow® AI Experience Lab for VS Code extension to your ServiceNow instance to access instance files, deploy changes, and preview your work.

## Before you begin

Role required: none

The ServiceNow® AI Experience Lab for VS Code extension requires the following:

<table id="table_imf_rfb_dkc"><thead><tr><th>

Application

</th><th>

Version

</th><th>

Resources for more information

</th></tr></thead><tbody><tr><td>

Visual Studio Code

</td><td>

1.97 later

</td><td>

[Visual Studio Code updates](https://code.visualstudio.com/updates/v1_132)

</td></tr><tr><td>

Node.js

</td><td>

24 or later

</td><td>

[Node.js](https://nodejs.org/en/download)

</td></tr><tr><td>

pnpm

</td><td>

10 or later

</td><td>

[pnpm](https://pnpm.io/installation)

</td></tr><tr><td>

ServiceNow SDK

</td><td>

4.10 or later

</td><td>

[ServiceNow SDK](https://www.npmjs.com/package/@servicenow/sdk)

</td></tr><tr><td>

ServiceNow instance

</td><td>

-   Australia Patch 5 or later
-   Zurich Patch 12 or later

</td><td>

[Prepare your upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/rn-prepare-landing-page.md)

</td></tr></tbody>
</table>## Procedure

1.  Add a new instance.

    -   From the home screen, select **Add a new instance**.
    -   From the command palette, select **Add a new instance**.
2.  In the authentication type field, select either **Basic** or **OAuth** to match your instance configuration.

3.  In the instance URL field, enter the URL for your instance, including the protocol.

    For example, `https://<instance-name>.service-now.com`.

4.  Enter your instance username and password.

    For OAuth authentication, complete the additional authentication steps in the browser window that opens.

5.  In the instance alias field, enter a name for your instance.


## Result

If your instance is connected successfully, a notification in Visual Studio Code indicates that your instance has been added and lists the instance name.

