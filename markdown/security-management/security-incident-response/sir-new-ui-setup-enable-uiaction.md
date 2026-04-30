---
title: Enable UI Actions
description: Before you configure any UI Actions, you must perform certain steps to enable them so that they are available for configuration in the Security Analyst Workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Additional Security Analyst Workspace configuration, Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Enable UI Actions

Before you configure any UI Actions, you must perform certain steps to enable them so that they are available for configuration in the Security Analyst Workspace.

**Note:** To modify the UI actions, log in as a user with the following roles:

-   ui\_action\_admin
-   ui\_page\_admin
-   web\_service\_admin

There are two types of UI actions that can be configured for the Security Analyst Workspace:

-   Dialog Based UI Action
-   Server-side UI Action

**Dialog Based UI Action**

To enable dialog-based UI actions in the Security Analyst Workspace, make the following changes to the UI pages associated with the respective standard UI Actions.

1.  **HTML section**: Modify the HTML section to include the `react` input tag. The `react` input tag value is used in the client script section to identify if the UI Page has been launched from the Security Analyst Workspace. An example is shown below:

    `<input id="react" name="react" type="hidden" value="${JS,HTML:sysparm_react}" />`

2.  **Client script**: Additional logic needs to be written in the client script when the `react` flag is true. This is needed to handle the **Submit** and **Cancel** button events shown as part of the dialog window.
    1.  onCancel \(\) event handler needs to dispatch the ‘SIR\_WORKBENCH\_POPUP\_CANCEL’ event from the Security Analyst Workspace
    2.  onSubmit \(\) event handler needs to dispatch the ‘SIR\_WORKBENCH\_POPUP\_SUBMIT’ event from the Security Analyst Workspace
3.  The execution of the processing script is skipped from the Security Analyst Workspace context as the ‘onSubmit’ action has been modified to return false when the `react` input tag value is true. The logic of the processing script needs to be handled either via a client callable script \(invoked via GlideAjax API\) or REST resource endpoint.

Refer the following sample UI pages for more details:

-   Related List UI action example: Publish to watchlist \(UI page name: publish\_to\_watchlist\)
-   Form UI action example: Create Problem \(UI page name: create\_prb\_change\_inc\)

**Server side UI Action**

To enable server side UI actions, you must do the following:

The logic of the standard UI action script must be handled as part of a scripted REST resource.

Refer to the following sample Form UI actions for more details:

-   Create Outage
-   Cancel

