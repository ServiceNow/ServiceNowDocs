---
title: Create a QR code for mobile login
description: Create and use a QR code containing JSON to provide a method for your users to log in with pre-defined parameters.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Create a QR code for mobile login

Create and use a QR code containing JSON to provide a method for your users to log in with pre-defined parameters.

## Before you begin

Role required: none

## Procedure

1.  Use a text editor to create JSON using the following parameters.

    |Parameter|Definition|
    |---------|----------|
    |InstanceUrl|The URL for your instance. For example, `https://example.service-now.com`|
    |Name|The name of your instance. For example, `Example`.|

    The JSON consists of parameters and values, separated by comas, and enclosed in curly braces. Each parameter is separated from its value by a colon, and each parameter and value is enclosed in double quotes, as shown in these examples. The image shows how the instance appears in instance selection screen for the app.

    ```
    
    {
     "InstanceUrl":"https://example.service-now.com",
     "Name":"Example"
    }
    ```

    ![Instance and nickname in the ServiceNow Agent app.](../image/instance-name-example.png)

    This second example includes only the `InstanceUrl` value, which is also valid.

    ```
    {
    "InstanceUrl":"https://example.service-now.com"
    }
    ```

    **Important:**

    -   ServiceNow instances do not provide a method to create JSON files. You can create these files using your text editor of choice.
    -   Parameters are not supported for the Android OS. To use a QR code for Android, create a QR code containing only the URL for the instance as text rather than JSON. For example, `https://example.service-now.com`.
2.  Use a QR code generator of your choice to encode this JSON or text into a QR code.

    **Note:** ServiceNow instances do not provide a method to create QR codes, however there are many online resources you can use to create QR codes using the JSON created in the previous steps.

3.  Use your QR code to access the mobile app. For steps to use a QR code with the app, see [Add a ServiceNow instance to ServiceNow mobile apps](login-end-user.md).


**Parent Topic:**[Mobile authentication](../concept/mobile-authentication.md)

