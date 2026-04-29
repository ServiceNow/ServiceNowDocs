---
title: Update the ServiceNow SDK version for an application in the ServiceNow IDE
description: Configure which version of the ServiceNow SDK an application uses from the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Update the ServiceNow SDK version for an application in the ServiceNow IDE

Configure which version of the ServiceNow SDK an application uses from the ServiceNow IDE.

## Before you begin

Role required: admin

## About this task

From the ServiceNow IDE, you can configure which version of the ServiceNow SDK, including the ServiceNow Fluent APIs, an application uses beginning with ServiceNow SDK version 3.0.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace with an application.

3.  From the Activity Bar, select the File Explorer view \(![File Explorer](../image/servicenow-ide-file-explorer-icon.png)\).

4.  Open the `package.json` file for the application.

5.  In the `devDependencies` field, update the versions of the `@servicenow/sdk` and `@servicenow/eslint-plugin-sdk-app-plugin` packages to 3.0.0 or later.

    For example:

    ```json
    "devDependencies": {
            "@servicenow/sdk": "3.0.0",
            "@servicenow/glide": "26.0.1",
            "eslint": "8.50.0",
            "@servicenow/eslint-plugin-sdk-app-plugin": "3.0.0"
    }
    ```

6.  Save your changes.

7.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
8.  Enter `Package Manager: Install Dependencies` and press Enter.

    The dependencies are updated in the `node_modules` directory.


## Result

You can use the latest version of the ServiceNow SDK application packaging service and ServiceNow Fluent APIs in your application.

**Parent Topic:**[Configuring the ServiceNow IDE](../concept/configuring-servicenow-ide.md)

