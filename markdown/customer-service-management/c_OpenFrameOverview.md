---
title: OpenFrame overview
description: OpenFrame provides a communication frame that customer service agents use to place and receive customer calls.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating with Computer Telephony Integration \(CTI\), Integrating Customer Service Management with other applications, Customer Service Management]
---

# OpenFrame overview

OpenFrame provides a communication frame that customer service agents use to place and receive customer calls.

## OpenFrame user roles

The OpenFrame window is available to agents who belong to one of the user groups specified in the OpenFrame configuration, and with any of the following roles:

-   sn\_openframe\_user
-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   admin

## About OpenFrame

Use OpenFrame to integrate telephony systems into the ServiceNow AI Platform®. Use the OpenFrame API to communicate between the ServiceNow AI Platform and the domain opened in the OpenFrame window.

OpenFrame includes these components:

-   TopFrame, a ServiceNow application.
-   OpenFrame API, which gets sourced from the partner application. This API communicates with TopFrame and controls the OpenFrame visual features.

    The location of the API is `https://[servicenow instance]/scripts/openframe/1.0.5/openFrameAPI.min.js`. This minified version includes other needed libraries and should be used for integration.

    For API reference, you can use the un-minified version: `https://[servicenow instance]/scripts/openframe/1.0.5/openFrameAPI.js`. This version cannot be used directly for integration purposes.


**Note:**

-   To stay current with reference to the OpenFrame library, use the following resource URI: `https://[servicenow instance]/scripts/openframe/latest/openFrameAPI.min.js`.
-   To integrate softphone into the ServiceNow AI Platform using OpenFrame, add the third-party URLs of telephony services in the following property: **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist**. For more information see, [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), and Enable URL allow list for cross-origin iframe communication in Instance Security Hardening Settings.

## Using the OpenFrame window

OpenFrame provides support for embedded and contextual phone conversations, including:

-   Context identification: incoming calls maximize the OpenFrame window and display details about the caller, including the account, contact or consumer name, and phone number.
-   Links to forms: use the openFrameAPI \(openServiceNowForm\) to create links to forms. When an incoming call is received, an agent can click the account, contact, consumer, or case number in the OpenFrame window to open the corresponding record.
    -   In Agent Workspace, records open in either a primary tab or a sub-tab depending on the tab configuration.
    -   In the platform interface, records open in TopFrame \(i.e., the current page\).
-   Click-to-call capability: click phone number fields to make a call.
    -   In Agent Workspace, agents can click phone number fields on forms and in the Customer 360 ribbon component to make a call.
    -   In the platform interface, agents can click the phone icon next to the **Contact** or **Consumer** fields.
        -   If a contact or consumer has one phone number, the call is placed to that number.
        -   If a contact or consumer has more than one phone number, a dialog box displays the available numbers. Click a number to place the call.
-   OpenFrame window actions:

<table id="table_vmn_cvx_jhb"><thead><tr><th>

User action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open the window

</td><td>

In Agent Workspace, click the phone icon:

-   In the navigation bar.
-   Next to the **Contact** or **Consumer** fields on the Case form.
 In the platform interface, click the phone icon:

-   In the banner frame.
-   Next to the **Contact** or **Consumer** fields on the Case form.
 With the admin role, you can configure the phone icon. For more information, see [CTI integration with the Case form](c_CTIIntegrationWithTheCaseForm.md#).

</td></tr><tr><td>

Hide the window

</td><td>

Click the **X** in the OpenFrame window header. **Note:** The OpenFrame window remains on top of other forms or pages until hidden.

</td></tr><tr><td>

Expand or collapse the window

</td><td>

Click the **+ / –** buttons in the OpenFrame window header \(if **Enable collapsed view** is set to **True** in the OpenFrame configuration\).**Note:** When collapsed, agents can still access call control actions.

</td></tr><tr><td>

Move the window

</td><td>

Click and drag the OpenFrame window header.

</td></tr></tbody>
</table>
## Using OpenFrame in Agent Workspace

In Agent Workspace, you can integrate OpenFrame with the Interaction Management System \(IMS\) and interaction records. This allows agents to manage the phone interaction life cycle. For more information, see Integration with Interaction Management System \(IMS\).

## Creating an OpenFrame configuration

With the admin role, you can create or modify an OpenFrame configuration. This configuration stores information about the OpenFrame window settings, including:

-   The window height and width.
-   The icon, title, and subtitle displayed in the window header.
-   Users and groups that have access to the window.

**Related topics**  


[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

