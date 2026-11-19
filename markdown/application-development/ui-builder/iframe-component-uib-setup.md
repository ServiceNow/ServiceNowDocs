---
title: iFrame component setup
description: The iFrame component provides an inline place for other features, apps, or components. You can also use the iFrame component to include external functions, such as a Wikipedia search.Configure the size and functionality of the iFrame component.Select event handlers to configure the actions \(events\) provided with the iFrame component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/iframe-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# iFrame component setup

The iFrame component provides an inline place for other features, apps, or components. You can also use the iFrame component to include external functions, such as a Wikipedia search.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your iFrame that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "iframe-content-tree.png"\] Alt text: UI Builder content tree with the iFrame component.

2.  Select the iFrame component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the iFrame label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## iFrame component properties

Configure the size and functionality of the iFrame component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_c5f_srz_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title \[title\]

</td><td>

Text describing the embedded content.Default: "**Wikipedia home page**"

</td></tr><tr><td>

Source \[src\]

</td><td>

Source of the embedded content. If using an external page, use the URL.Default: "**https://www.wikipedia.com**"

</td></tr><tr><td>

Width\[width\]

</td><td>

Width of the framed component.Default: **400** pixels

</td></tr><tr><td>

Height \[height\]

</td><td>

Height of the framed component.Default: **300** pixels

</td></tr><tr><td>

Allow\[allow\]

</td><td>

Specifies a permission policy for the iframe by defining what functionality can and can't be used by it.Avalable choices:

-   **accelerometer** \(controls access to information about the acceleration of the device through the accelerometer interface\)
-   **ambient-light-sensor** \(controls access to information about the amount of light in the environment around the device\)
-   **attribution-reporting** \(controls access to the attribution reporting API\)
-   **autoplay** \(controls whether the iframe can autoplay requested media\)
-   **bluetooth** \(controls access to bluetooth\)
-   **browsing-topics** \(controls access to the Topics API\)
-   **camera** \(controls access to use video input devices\)
-   **compute-pressure** \(controls access to the Compute Pressure API\)
-   **cross-origin-isolated** \(controls access to the APIs that require cross-origin isolation\)
-   **display-capture** \(controls access to the Screen Capture API `getDisplayMedia()` to capture the contents on the screen\)
-   **document-domain** \(controls access to set the `document.domain`\)
-   **encrypted-media** \(controls access to the Encrypted Media Extensions API \(EME\)\)
-   **fullscreen** \(controls access to use the `Element.requstFullscreen()`\)
-   **geolocation** \(controls access to the Geolocation interface\)
-   **gyroscope** \(controls access to information about the orientation of the device through the Gyroscope interface\)
-   **hid** \(controls access to the WebHID API to connect to uncommon or exotic human interface devices such as alternative keyboards or gamepads\)
-   **identity-credentials-get** \(controls access to the Federated Credential Management API \(FedCM\), and more specifically the `navigator.credentials.get()` method with an `identity` option\)
-   **idle-detection** \(controls access to detect when users are interacting with their devices, for example to report **available** or **away** status in chat applications\)
-   **local-fonts** \(controls access to data on the user's locally-installed fonts using the `Widow.queryLocalFonts()` method\)
-   **magnetometer** \(controls access to information about the orientation of the device through the Magnetometer interface\)
-   **microphone** \(controls whether the iframe can use audio input devices\)
-   **midi** \(controls access to the Web MIDI API\)
-   **opt-credentials** \(controls access to the WebOTP API to request a one-time password \(OTP\) from a specially-formatted SMS message sent by the app's server, using `navigator.credentials.get({otp: .......})`\)
-   **payment** \(controls access to the Payment Request API\)
-   **picture-in-picture** \(controls access to play a video in a Picture-in-Picture mode\)
-   **publickey-credentials-create** \(controls access to the Web Authentication API to create new WebAuthn credentials using `navigator.credentials.create( {publicKey] }`\)
-   **publickey-credentials-get** \(controls access to the Web Authentication API to retrieve public-key credentials using `navigator.credentials.get( {publicKey] }`\)
-   **screen-wait-lock** \(controls access to the Screen Wake Lock API to indicate that the device should not dim or turn off the screen\)
-   **serial** \(controls access to the Web Serial API to communicate with serial devices, either directly connected via a serial port, or via USB or Bluetooth devices emulating a serial port\)
-   **storage-access** \(controls access to the Storage Access API to request access to unpartitioned cookies\)
-   **usb** \(controls access to the WebUSB API\)
-   **web-share** \(controls access to the `Navigator.share()` method of the Web Share API to share text, links, images, and other content to arbitrary destinations of the user's choice\)
-   **window-management** \(controls access to the Window Management API to manage windows on multiple displays\)
-   **xr-spatial-tracking** \(controls access to the WebXR Device API\)

Default: **\{\\"accelerometer\\":true,\\"autoplay\\":true,\\"encrypted-media\\":true,\\"gyroscope\\":true,\\"picture-in-picture\\":true\}**

</td></tr><tr><td>

Disable sandbox \[disableSandbox\]

</td><td>

When **true**, lifts the following restrictions: allow-forms, allow-modals, allow-popups, allow-presentation, allow-same-origin, allow-scripts, allow-downloads. By default, only the allow-scripts restriction is removed.-   **allow-forms**
-   **allow-modals**
-   **allow-popups**
-   **allow-presentation**
-   **allow-same-origin**
-   **allow-scripts**
-   **allow-downloads**

Default: **False** - The sandbox is enabled and only lifts the allow-scripts option.

</td></tr><tr><td>

Allow top navigation\[allowTopNavigation\]

</td><td>

To enable **allow-top-navigation**, set to **true** when **disableSandbox** is **true**. **Warning:** This property may produce unexpected page redirects with root relative iframe src URLs.

Default: **False**.

</td></tr><tr><td>

Pass data into iframe \[data\]

</td><td>

Use to send messages to the iframed document; type can be object or string. Use targetOrigin \(below\) to securely ensure only the intended target \(iframed document\) receives the message.

</td></tr><tr><td>

Target origin \[targetOrigin\]

</td><td>

Included when the message is posted to the iframed document. Use targetOrigin to specify the required origin of the recipient window in order to receive the event. The targetOrigin must match exactly \(including scheme, hostname, and port\).Default: Uses the host from the src property

</td></tr></tbody>
</table>## iFrame component events

Select event handlers to configure the actions \(events\) provided with the iFrame component.

The Events tab shows the events used by the iFrame component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the iFrame actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|iFrame loaded|Dispatched when the iFrame is loaded. The payload contains a reference to the native iFrame's Window object.|
|iFrame message|Message dispatched from iFrame document.|

