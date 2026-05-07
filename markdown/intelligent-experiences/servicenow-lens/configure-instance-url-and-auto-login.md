---
title: Set up auto-login for ServiceNow AI Lens
description: Pre-configure your organization's ServiceNow instance URL so that it appears ready-filled when users launch the ServiceNow AI Lens desktop application, and enable auto-login so that users can skip signing in on subsequent launches.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-04-08"
reading_time_minutes: 1
keywords: [AI Lens, instance URL, auto-login, app-config.json, lens\_enable\_auto\_login]
breadcrumb: [Configure, ServiceNow AI Lens, Enable AI experiences]
---

# Set up auto-login for ServiceNow AI Lens

Pre-configure your organization's ServiceNow® instance URL so that it appears ready-filled when users launch the ServiceNow AI Lens desktop application, and enable auto-login so that users can skip signing in on subsequent launches.

## Before you begin

Role required: admin

ServiceNow AI Lens must be installed on the user's machine. For more information, see [Download the ServiceNow AI Lens installer](download-sn-lens-msi.md).

## Procedure

1.  On the user's machine, open the `app-config.json` file from the following location depending on the operating system:

    -   **Windows:** `<username>\AppData\Roaming\servicenow-lens\app-config.json`
    -   **Mac:** `/Users/<username>/Library/Application Support/servicenow-lens/app-config.json`
    **Note:** The folders in the file path may be hidden by default. Unhide them before navigating to the `app-config.json` file.

2.  In the `app-config.json` file, enter your organization's ServiceNow® instance URL as the value for the `instanceUrl` field.

    ```
    
    
    {
      "instanceUrl": "https://<your-instance>.service-now.com"
    }
                        
    ```

    **Note:**

    -   The `app-config.json` file is unique to each user on the machine. If ServiceNow AI Lens is installed for all users, the administrator must update the `instanceUrl` field in each user's `app-config.json` file individually. If it is installed for a specific user only, that user can update their own `app-config.json` file.
    -   If you change the instance URL on the login screen and successfully sign in, AI Lens saves the new URL. The next time you launch ServiceNow AI Lens, the updated URL appears in the `instanceUrl` field.
3.  To enable auto-login, perform the following steps.

    1.  Navigate to **All** &gt; **System Definition** &gt; **All Properties**.

        **Tip:** If your instance can't navigate to **All Properties**, in the search field, enter `sys_properties.list` and press **Enter**.

    2.  Search for `sn_app_lens_core.lens_enable_auto_login` property.

    3.  In the **value** field, set the value to **true**, and select **Update**.

        ![Auto-login property value.](../image/lens-auto-login-property-value.png "Auto-login property value")

        **Note:** When this property is enabled, ServiceNow AI Lens automatically signs in users on subsequent launches without showing the login screen. If a user signs out or their sign-in expires, the login screen reappears with the instance URL already filled in. If you manually update the `app-config.json` file after your first login, you will be prompted to sign in again.


