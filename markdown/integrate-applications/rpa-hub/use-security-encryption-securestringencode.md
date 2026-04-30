---
title: Use the SecureStringEncode component
description: Encode a string to secure it by using the Secure String Encode component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Encryption components, Security, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the SecureStringEncode component

Encode a string to secure it by using the Secure String Encode component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Secure String Encode component. For more information about these properties, see [Properties of the Encryption components](../reference/properties-security-encryption-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Security** &gt; **Encryption**.

2.  Drag the Secure String Encode component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  In the Secure String Encode component, enter the string that you want to encode in the **Text** field or pass the string through the Data In port.

5.  Connect the data and control ports of the Secure String Encode component to the corresponding ports of the other components.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Text\)|Passes the string that you want to encode from a previously executed component.|Yes|
    |Data Out|Returns the encoded, secure string.|Yes|
    |Control In|Passes the control from a previously executed component.|Yes|
    |Control Out|Passes the control to the next component.|No|

6.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Encryption components](../concept/encryption-components.md)

