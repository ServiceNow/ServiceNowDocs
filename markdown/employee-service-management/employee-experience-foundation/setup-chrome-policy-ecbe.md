---
title: Set up browser policies
description: Set up the browser policies to enable access to the Browser Extension for Employee Center within the supported browsers.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Browser Extension for Employee Center, Setup task management, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Set up browser policies

Set up the browser policies to enable access to the Browser Extension for Employee Center within the supported browsers.

## Before you begin

Role required: none

**Note:** The enterprise administrator must set up the browser policies.

## About this task

The Browser Extension for Employee Center can be accessed through Google Chrome and Microsoft Edge browsers.

**Note:** The administrator is responsible for setting up the browser policies depending on the supported browser in use.

The browser settings and policy page might look different for different browsers.

## Procedure

1.  Configure the Browser Extension for Employee Center in either of the supported web browsers.

    -   For more information on setting up the Browser Extension for Employee Center in Google Chrome, see [https://support.google.com/chrome/a/answer/14749672?hl=e](https://support.google.com/chrome/a/answer/14749672?hl=e).
    -   For more information on setting the Browser Extension for Employee Center in Microsoft Edge, see [https://learn.microsoft.com/en-us/deployedge/configure-microsoft-edge](https://learn.microsoft.com/en-us/deployedge/configure-microsoft-edge).

        The following is a sample of the JSON file that you must fill to see the policies on the browser.

        ```json
        {
          "Instance": "",
          "Browser extension portal": "",
          "Employee portal": "",
          "Extension title": "",
          "Extension icon path": "",
          "Enable notifications": false,
          "Enable context menu": false,
          "Open search in browser extension": false,
          "Allowed sites": [],
          "Context menu title for search": "",
          "Context menu title for search in portal": "",
          "Empty State title": "",
          "Empty State Header Logo": ""
        }
        ```

2.  In the **ServiceNow Employee Center Browser Extension** policy, fill in the fields.

3.  Enter the following field values to set up Browser Extension for your web browser.

<table id="table_pct_sf5_vfc"><thead><tr><th>

Field

</th><th>

Values

</th></tr></thead><tbody><tr><td>

Allowed sites

</td><td>

Examples: &lt;concur, workday&gt;

</td></tr><tr><td>

Browser extension portal

</td><td>

ecbe

</td></tr><tr><td>

Context menu title for search

</td><td>

Open search in browser extension

</td></tr><tr><td>

Context menu title for search in portal

</td><td>

Open search in employee portal

</td></tr><tr><td>

Employee portal

</td><td>

esc

</td></tr><tr><td>

Empty state action label

</td><td>

Open Employee Hub

</td></tr><tr><td>

Empty state message

</td><td>

&lt;Empty state message for your organization&gt;

</td></tr><tr><td>

Empty state title

</td><td>

&lt;Visit Employee hub&gt;

</td></tr><tr><td>

Enable context menu

</td><td>

true

</td></tr><tr><td>

Enable notifications

</td><td>

true**Note:** Enable this setting to get Chrome browser notifications along with the notifications in your Browser Extension.

</td></tr><tr><td>

Instance

</td><td>

&lt;servicenow.com&gt;

</td></tr><tr><td>

Open search in browser extension

</td><td>

true**Note:** Enabled this context search option to open it in the Browser Extension.

</td></tr><tr><td>

Open search in Employee Portal

</td><td>

true**Note:** Enabled this context search option to open it in the Employee Center portal.

</td></tr></tbody>
</table>    If you try to access the Browser Extension from a website where it's not configured, a link takes you back to the Employee Center portal.


