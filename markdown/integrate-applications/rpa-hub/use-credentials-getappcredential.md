---
title: Use the GetApplicationCredential component
description: When login credentials for an RPA Hub application are already set in RPA Hub, retrieve the credentials by using the GetApplicationCredential component.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Credentials, RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the GetApplicationCredential component

When login credentials for an RPA Hub application are already set in RPA Hub, retrieve the credentials by using the GetApplicationCredential component.

## Before you begin

In RPA Desktop Design Studio, assign your automation to a bot process by selecting **Assign bot process** option from the **Design** tab. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Role required: none

## About this task

The GetApplicationCredential component can be used when the automation involves an application that requires user authentication. When a user name and password for the application are stored in RPA Hub, GetApplicationCredential retrieves them.

You can configure the properties for the GetApplicationCredential component. For more information about these properties, see [Properties of the Credentials components](../reference/credentials-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **RPA Hub** &gt; **Credentials**.

2.  Drag the GetApplicationCredential component to the Design surface.

3.  Confirm the configuration of the component's input fields.

    For more information, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetApplicationCredential component to the corresponding ports of the other components as described in the following table.

    |Port|Description|Port type|Data type|Required|
    |----|-----------|---------|---------|--------|
    |Name|Receives the name of the business application that is associated with the bot process|Data In|String|Yes|
    |UserName|Returns the user name that is needed to log in to the business application|Data Out|String|Yes|
    |Password|Returns the password needed to log in to the business application|Data Out|SecureString|Yes|

5.  To test the component, on the **Design** tab, select **Run**.


**Parent Topic:**[Credentials](../concept/credentials.md)

