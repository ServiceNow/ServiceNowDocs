---
title: Use the Unprotect component
description: Decrypt an encrypted string using the Unprotect component in the RPA Desktop Design Studio. You can use the component on strings encrypted by the ProtectData or any other application as part of a Workflow. The Unprotect component returns the decrypted string or data.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [DPAPI, Security, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Unprotect component

Decrypt an encrypted string using the Unprotect component in the RPA Desktop Design Studio. You can use the component on strings encrypted by the ProtectData or any other application as part of a Workflow. The Unprotect component returns the decrypted string or data.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Unprotect component. For more information about these properties, see [Properties of the DPAPI components](../reference/properties-of-dpapi-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Security** &gt; **DPAPI**.

2.  Drag the Unprotect component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Unprotect component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(EncryptedText\)

</td><td>

Passes the encrypted string from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data In \(Optional Entropy\)

</td><td>

If the string is protected by entropy, you need to enter the entropy details to enable the component to access the data. Passes the entropy details from a previously executed component.

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

Returns the decrypted string.

</td><td>

YesTo view the output, right-click the **Return** field and click **Preview Data**.

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

