---
title: Basic authentication credentials
description: The basic authentication credential type manages access to store basic authentication credentials.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create and test your credentials, Getting started with credentials, Connections and Credentials, Access Management]
---

# Basic authentication credentials

The basic authentication credential type manages access to store basic authentication credentials.

These fields are available in the Credentials form for basic authentication.

<table><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential. For example, you might call it **Basic Authentication**.

</td></tr><tr><td>

User Name

</td><td>

Enter the user name.

</td></tr><tr><td>

Password

</td><td>

Enter the password.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for these credentials in the [CyberArk](../concept/c_CyberArkCredStorageIntegrate.md) external credential storage system. The credential ID may be used as a safe override when multiple safes are in use. By default, the syntax in the **Credential ID** field is this: **&lt;safe name&gt;:&lt;Credential ID&gt;**. If the safe name is omitted, there must be a safe name defined in the `config.xml` file. To change the separator character from the default colon to another character, override the value with the optional [**ext.cred.safe\_name**](../task/t_ConfigureTheMIDServerForCyberArk.md) parameter. The **Credential ID** field has a limit of 40 characters.This field is only visible when the **External storage** check box is selected.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. Currently, the only supported external storage system is CyberArk.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>