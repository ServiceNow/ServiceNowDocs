---
title: Use the GetTOTP component
description: Generate the Time-based One-time Password \(TOTP\) to access multi-factor authentication \(MFA\)-enabled applications in an automation by using the GetTOTP component in the RPA Desktop Design Studio application.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Token, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the GetTOTP component

Generate the Time-based One-time Password \(TOTP\) to access multi-factor authentication \(MFA\)-enabled applications in an automation by using the GetTOTP component in the RPA Desktop Design Studio application.

## Before you begin

-   Create an MFA authenticator record and map the TOTP authenticator to the robot credential. For more information on how to perform these tasks on RPA Hub, see [Create an MFA authenticator in RPA Hub](../../rpa-hub/task/create-mfa-authenticator-rpa.md) and [Create a TOTP authenticator in RPA Hub](../../rpa-hub/task/map-totp-credential-set-rpa.md). For more information on TOTP authentication in RPA Hub, see [TOTP authentication in RPA Hub](../../rpa-hub/concept/totp-authentication-rpa.md).
-   Connect to the required instance in RPA Desktop Design Studio and assign the bot process with the TOTP record to the automation. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

The TOTP record is created in RPA Hub and the record is associated to the robot credential. The GetTOTP component in RPA Desktop Design Studio has an **AuthenticatorName** parameter. The authenticator name that you provide from the component must be present in the TOTP record. If the authenticator is present, the TOTP is generated.

## Procedure

1.  Navigate to **Utilities** &gt; **Token** from the Toolbox pane in the **Design** tab.

2.  Drag the **GetTOTP** component to the Design surface.

3.  In the **AuthenticatorName** field of the component, enter the name of the authenticator.

    The name that you enter must match with the value in the **Authenticator** field of the TOTP record.

4.  To test the component, right-click the component and select **Run From Here**.

    You can also run the automation by selecting **Run** from the **Design** tab.

    When the component is successfully run, the output ports are populated in the connector as per the following table.

    |Port name|Port type|Port description|
    |---------|---------|----------------|
    |TOTP|Data Out|One-time password that is generated at that point of execution.|
    |ValidFor|Data Out|Time in seconds until the password is valid.|

5.  To test the component, right-click the component and select **Run From Here**.

    You can also run the automation by selecting **Run** from the **Design** tab.


**Parent Topic:**[Token](../concept/token-utilities.md)

