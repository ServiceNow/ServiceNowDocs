---
title: Integrate McAfee disk encryption with the Password Reset Windows Application
description: You use ePolicy Orchestrator \(ePO\) to enable McAfee MDE 7.2 on a Windows desktop computer to support the Password Reset Windows Application.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate McAfee disk encryption with the Password Reset Windows Application

You use ePolicy Orchestrator \(ePO\) to enable McAfee MDE 7.2 on a Windows desktop computer to support the Password Reset Windows Application.

## Before you begin

-   Role required: password\_reset\_admin

-   Required: MDE version 7.2x

## Procedure

1.  Log in to ePO.

2.  On the Policy Catalog, select **Product** &gt; **Drive Encryption 7.2.0** and select **Category** &gt; **Product Settings**

    ![Category Product Settings](../image/epo-policy-catalog.png)

3.  Click the **Name** of your policy catalog \(**My Default** in the example\).

4.  On the **Log On** tab, select the **V7.2 Onwards** tab and then select the **Allow integrated third-party credential providers ...** check box.

    ![Allow integrated third-party credential providers](../image/epo-log-on-tab.png)

5.  Click **Save** and then log out of ePO.

6.  On the end-user computer, create the following registry keys \(client-side ePO setting\):

    ```
    
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\McAfee EndPoint Encryption\IntegratedCredentialProviders\{0780AF60-65C2-4718-942D-E0C56E89EF9B}] 
    "Vendor"="ServiceNow, Inc" 
    "Product"="ServiceNow PasswordReset WinApp" 
    "Version"="<PasswordReset WinApp version>" (for example, "Version"="4.5") 
    "BuiltAgainst"="<MDE version>" (for example, "BuiltAgainst"="7.2.3.28")
    
    ```

7.  Restart the computer.


**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

