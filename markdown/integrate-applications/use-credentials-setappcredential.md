---
title: Use the SetApplicationCredential component
description: Set or update the login credentials in RPA Hub applications by using the SetApplicationCredential component.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Credentials, RPA Hub, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the SetApplicationCredential component

Set or update the login credentials in RPA Hub applications by using the SetApplicationCredential component.

## Before you begin

In RPA Desktop Design Studio, assign your automation to a bot process by selecting **Assign bot process** option from the **Design** tab. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Role required: none

## About this task

The SetApplicationCredential component can be used when the automation involves an application that requires the login credentials to be periodically updated, or when the login credentials must be changed for any other reason. This component updates the credentials in RPA Hub.

You can configure the properties for the SetApplicationCredential component. For more information about these properties, see [Properties of the Credentials components](../reference/credentials-properties.md).

If the application credential record has the **External Credential** check box enabled, then this SetApplicationCredential component does not set the credentials and displays an error. For more information about the application credential settings, see [Create an application credential in RPA Hub](../../rpa-hub/task/create-application-credential.md).

## Procedure

1.  In the Toolbox pane, navigate to **RPA Hub** &gt; **Credentials**.

2.  Drag the SetApplicationCredential component to the Design surface.

3.  Confirm the configuration of the component's input fields.

    For more information, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SetApplicationCredential component to the corresponding ports of the other components as described in the following table.

    |Port|Description|Port type|Data type|Required|
    |----|-----------|---------|---------|--------|
    |Name|Receives the name of the business application that is associated with the bot process|Data In|String|Yes|
    |Password|Receives the password that is needed to log in to the business application|Data In|String|Yes|
    |Return|Returns True if the credentials are set successfully or False if setting the credentials failed|Data Out|Boolean|Yes|

5.  To test the component, on the **Design** tab, select **Run**.


**Parent Topic:**[Credentials](../concept/credentials.md)

