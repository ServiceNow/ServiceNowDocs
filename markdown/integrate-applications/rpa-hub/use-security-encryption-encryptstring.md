---
title: Use the EncryptString component
description: Encrypt a string by providing the encryption key with the EncryptString component in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Encryption components, Security, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the EncryptString component

Encrypt a string by providing the encryption key with the EncryptString component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Encrypt String component. For more information about these properties, see [Properties of the Encryption components](../reference/properties-security-encryption-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Security** &gt; **Encryption**.

2.  Drag the Encrypt String component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Encrypt String component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Text\)

</td><td>

Passes the string that you want to encrypt from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(EncryptionKey\)

</td><td>

Passes the encryption key from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the encrypted string.

</td><td>

No. Connecting the port is optional.To view the output, right-click the **Return** field and click **Preview Data**.

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


**Parent Topic:**[Encryption components](../concept/encryption-components.md)

