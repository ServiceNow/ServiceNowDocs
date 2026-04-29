---
title: Smart button functions
description: Use smart buttons to interact with native applications on your mobile device, such as your phone, map, or email applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Smart button functions

Use smart buttons to interact with native applications on your mobile device, such as your phone, map, or email applications.

## Smart buttons

![Smart button functions](../image/smart-button-function.png)

Use smart buttons to quickly perform actions you specify outside the app. These actions can include navigating to a location on a map, sending a text message or email to a contact, placing a phone call, or opening a URL in a browser. You can choose from any of the following options.

## Smart button types

<table id="table_lrd_51l_4gb"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Address

</td><td>

Use the **Address** smart button type to navigate to an address on your instance using your mobile devices navigation software.

 For example, you can configure a button to direct your field technician to their next work location.

</td></tr><tr><td>

Email

</td><td>

Use the **Email** smart button type to send an email. The recipient can be a static email address, or an email address stored on a table on your instance.

 For example, you can configure a button to send a email with a preset subject from within an incident record.

</td></tr><tr><td>

Phone

</td><td>

Use the **Phone** smart button type to place a call or send an SMS text message. As with email, the recipient can be a static, or a number stored on an instance record.

 For example, you can configure a button on an incident record to call your customer. You can configure your smart button to automatically use the phone number in your customer's user record.

</td></tr><tr><td>

URL

</td><td>

Use the **URL** smart button to navigate to a web address. For example, you can configure a button to open your company's website.

 URLs can be relative or external. Relative URLs display within the app, while external URLs open in the mobile device's default browser.

</td></tr></tbody>
</table>## Smart button context

Context determines whether a smart button uses information in a record, or static information you define when creating the smart button.

-   **Record Context**

    Use record context when you want to use information from the record where you have included your smart button. For example, you want to create a smart button to call the user listed in the **Caller** field of an incident. In this case you would select **Record** in the smart button's context field. The number used for the phone call is specified by selecting a table and field where the caller's phone number is stored. Using this method, the number called changes dynamically when accessing incidents with different callers.

-   **Global Context**

    Use global context when you want to create a button that does not depend on information in the record. For example, you want to create a smart button that calls your company's support number. This number remains the same no matter where the smart button is placed in your application. When creating a smart button with the global context, you have a **Phone Number** field where you can input the number.


For examples of configuring smart buttons, see [Configure a smart button](../task/sg-studio-config-smart-button.md).

## Smart button advanced configurations

Use advanced configurations to control when your button appears, based on conditions or roles. You may, for example want to hide an email button for records that have no email address, or display a URL link only to your admin users.

|Configuration|Description|
|-------------|-----------|
|Display Conditions|Conditions under which the smart button is visible.|
|Roles Permission|Roles that can see the smart button. If no roles are selected, the button is visible to all users.|

## Deep linking to third party applications

ServiceNow mobile supports deep linking to third party applications using the **URL** smart buttons. To make use of this feature, enter a properly formatted URI in the **URL** field. The format for a deep linking URI varies depending on the target app. For information on these URI formats, refer to deep linking documentation provided by the third party vendors.

Administrators can use the **glide.sg.allowed\_external\_deeplinks** property to define which third party apps. For details on this property, see [Configure which external apps are available for deep linking](../task/mobile-allow-deeplink.md).

