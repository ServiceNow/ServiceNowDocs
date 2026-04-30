---
title: Security controls
description: Configure security controls to restrict copy/paste, enforce PIN, or block attachment functionality.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Security practices, Device security, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# Security controls

Configure security controls to restrict copy/paste, enforce PIN, or block attachment functionality.

## Restrict copy/paste

Copy/paste restrictions are defined in the system properties \[sys\_properties\] table. There are two applicable security properties.

glide.sg.clear\_pasteboard\_when\_background: Clears the copy/paste clipboard when a ServiceNow app enters the background. For more information on clearing the clipboard, see [Configure clear clipboard](additional-mobile-configuration.md).

## Require an app PIN

Require users to enter a six digit PIN each time they sign in from their mobile device, or when an app has been inactive for five minutes. Requiring an app PIN is controlled by the **glide.sg.require\_mobile\_application\_pin** system property. For more information on requiring an app PIN, see [Require an app PIN](additional-mobile-configuration.md).

## Disabling attachments on a mobile device

Use an ACL to block specific access on mobile. Use the [isMobile](https://developer.servicenow.com/app.do#!/api_doc?v=kingston&id=r_ScopedGS-isMobile) method to check if a request comes from a mobile device. For example, you could add an ACL for the attachment \[sys\_attachment\] table where the read and write scripted ACLs includes the following check. You can also add this code to any existing ACLs you have for the attachment table. If have multiple attachment ACLs, all of the need to have **Admin override** option unchecked.

```
if( gs.isMobile() ){
     answer = false;
}
```

**Note:** You need elevated privileges to create ACLs.

## Enable the blur app option

Blur a mobile app when not in focus on a mobile device using the following system property in the system properties \[sys\_properties\] table.

**glide.sg.blur\_ui\_when\_backgrounded**

**Important:**

-   The **glide.sg.blur\_ui\_when\_backgrounded** system property is supported on both iOS and Android devices.
-   By default, the value for this property is set to `false`, which turns it off.
-   For Android devices, when this property is enabled by setting the value to `true`, the following restrictions apply:

    -   The screen share feature isn't supported and the shared app screen appears black.
    -   Users are prevented from taking screenshots.
    These restrictions don't apply to iOS devices when the **glide.sg.blur\_ui\_when\_backgrounded** property is enabled.


For more information, see [Configure the blur app option](additional-mobile-configuration.md)

## Block rooted and jailbroken devices

To improve security on your mobile device, block the logging in of mobile apps when a rooted or jailbroken device is used. Use the following security property:

**glide.sg.allow\_rooted\_jailbroken\_devices system**

For more information, see [Configure the status for rooted and jailbroken devices](../task/configure-rooted-jailbroken-devices.md).

## Penetration testing

ServiceNow engages a third party to perform penetration testing of a mobile app. This typically happens annually but sometimes occurs more frequently. The results of these tests are available to customers on CORE. Customers can test the mobile application in conjunction with a pen test of their instance per the process outlined in [KB0538598](https://support.servicenow.com/kb_view.do?sysparm_article=KB0538598).

**Parent Topic:**[Mobile security practices](sg-mobile-security-practices.md)

