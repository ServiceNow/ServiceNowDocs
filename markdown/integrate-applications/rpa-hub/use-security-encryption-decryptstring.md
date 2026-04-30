---
title: Use the DecryptString component
description: Decrypt an encrypted string by providing the encryption key using the Decrypt String component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Encryption components, Security, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the DecryptString component

Decrypt an encrypted string by providing the encryption key using the Decrypt String component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Decrypt String component. For more information about these properties, see [Properties of the Encryption components](../reference/properties-security-encryption-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Security** &gt; **Encryption**.

2.  Drag the Decrypt String component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Decrypt String component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Text\)

</td><td>

Passes the encrypted string that you want to decrypt from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(encryptionKey\)

</td><td>

Passes the encryption key used to encrypt the string you want to decrypt from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data Out

</td><td>

Returns the decrypted string.

</td><td>

No. Connecting the port is optional.To view the output, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Passes the control from a previously executed component.

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

