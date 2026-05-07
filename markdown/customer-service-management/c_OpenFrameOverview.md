---
title: OpenFrame overview
description: OpenFrame provides a communication frame that customer service agents use to place and receive customer calls.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# OpenFrame overview

OpenFrame provides a communication frame that customer service agents use to place and receive customer calls.

## OpenFrame user roles

The OpenFrame window is available to agents who belong to one of the user groups specified in the OpenFrame configuration, and with any of the following roles:

-   sn\_openframe\_user
-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   sn\_openframe.admin

## About OpenFrame

Use OpenFrame to integrate telephony systems into the ServiceNow AI Platform®. Use the OpenFrame API to communicate between the ServiceNow AI Platform and the domain opened in the OpenFrame window.

OpenFrame includes these components:

-   TopFrame, a ServiceNow application.
-   OpenFrame API, which gets sourced from the partner application. This API communicates with TopFrame and controls the OpenFrame visual features.

    The location of the API is `https://[servicenow instance]/scripts/openframe/1.0.5/openFrameAPI.min.js`. This minified version includes other needed libraries and should be used for integration.

    For API reference, you can use the unminified version: `https://[servicenow instance]/scripts/openframe/1.0.5/openFrameAPI.js`. This version can’t be used directly for integration purposes.


**Note:**

-   To stay current with reference to the OpenFrame library, use the following resource URI: `https://[servicenow instance]/scripts/openframe/latest/openFrameAPI.min.js`.
-   To integrate softphone into the ServiceNow AI Platform using OpenFrame, add the third-party URLs of telephony services in the following property: **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist**. For more information see, [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US), and [Enable URL allow list for cross-origin iframe communication](https://www.servicenow.com/docs/access?context=sc-enable-url-allowlist-for-cross-origin-iframe-communication&version=australia&pubname=australia-platform-security&ft:locale=en-US) in Instance Security Hardening Settings.

## Using the OpenFrame window

OpenFrame provides support for embedded and contextual phone conversations, including:

-   Context identification: Incoming calls maximize the OpenFrame window and display details about the caller, including the account, contact or consumer name, and phone number.
-   Links to forms: Use the openFrameAPI \(openServiceNowForm\) to create links to forms. When an incoming call is received, an agent can select the account, contact, consumer, or case number in the OpenFrame window to open the corresponding record.
    -   In Agent Workspace, records open in either a primary tab or a subtab depending on the tab configuration.
    -   In the platform interface, records open in TopFrame \(that is, the current page\).
-   Select-to-call capability: Click phone number fields to make a call.
    -   In Agent Workspace, agents can select phone number fields on forms and in the Customer 360 ribbon component to make a call.
    -   In the platform interface, agents can select the phone icon next to the **Contact** or **Consumer** fields.
        -   If a contact or consumer has one phone number, the call is placed to that number.
        -   If a contact or consumer has more than one phone number, a dialog box displays the available numbers. Select a number to place the call.
-   OpenFrame window actions:

<table id="table_vmn_cvx_jhb"><thead><tr><th>

User action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open the window

</td><td>

In Agent Workspace, select the phone icon:

-   In the navigation bar.
-   Next to the **Contact** or **Consumer** fields on the Case form.
 In the platform interface, select the phone icon:

-   In the banner frame.
-   Next to the **Contact** or **Consumer** fields on the Case form.
 With the admin role, you can configure the phone icon. For more information, see [CTI integration with the Case form](c_CTIIntegrationWithTheCaseForm.md#).

</td></tr><tr><td>

Hide the window

</td><td>

Select the **X** in the OpenFrame window header. **Note:** The OpenFrame window remains on top of other forms or pages until hidden.

</td></tr><tr><td>

Expand or collapse the window

</td><td>

Select the **+ / –** buttons in the OpenFrame window header \(if **Enable collapsed view** is set to **True** in the OpenFrame configuration\).**Note:** When collapsed, agents can still access call control actions.

</td></tr><tr><td>

Move the window

</td><td>

Select and drag the OpenFrame window header.

</td></tr></tbody>
</table>
## Using OpenFrame in CSM Configurable Workspace

In the CSM Configurable Workspace, you can:

-   Integrate OpenFrame with the Interaction Management System \(IMS\) and interaction records. This enables agents to manage the phone interaction life cycle.
-   Use the native voice control capability from the Interaction Controls Component \(ICC\) plugin to integrate to the contact center voice channel. You must enable this in the CSM Configurable Workspace to manage the voice channel. For more information, see [Interaction Controls Component \(ICC\) for voice calls](contact-center-integration-with-icc.md) and [Interaction Controls Component \(ICC\) call features](interaction-controls-component-icc-call-interaction-features.md).

## Creating an OpenFrame configuration

With the admin role, you can create or modify an OpenFrame configuration. This configuration stores information about the OpenFrame window settings, including:

-   The window height and width.
-   The icon, title, and subtitle displayed in the window header.
-   Users and groups that have access to the window.

**Related topics**  


[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

