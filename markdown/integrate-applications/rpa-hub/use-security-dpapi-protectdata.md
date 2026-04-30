---
title: Use the ProtectData component
description: Encrypt and save string data to a file with the ProtectData component in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [DPAPI, Security, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ProtectData component

Encrypt and save string data to a file with the ProtectData component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ProtectData component. For more information about these properties, see [Properties of the DPAPI components](../reference/properties-of-dpapi-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Security** &gt; **DPAPI**.

2.  Drag the ProtectData component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ProtectData component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Filename\)

</td><td>

Passes the name of the file to which the encrypted string is saved from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Data\)

</td><td>

Passes the data to be encrypted from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Optional Entropy\)

</td><td>

The optional entropy provides additional security to the encrypted data from risks that make applications running under the same user vulnerable. Passes the entropy from a previously executed component.

</td><td>

No. Connecting the port is optional.

</td></tr><tr><td>

Data In \(Scope\)

</td><td>

Passes the scope of protection from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out \(String\)

</td><td>

Returns the encrypted string.

</td><td>

No. Connecting the port is optional.To execute the component, right-click the ProtectData component bar and click **Run From Here**.

 To view the output, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Passes the control from a from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Passes the control to the next component.

</td><td>

No

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[DPAPI](../concept/dpapi.md)

