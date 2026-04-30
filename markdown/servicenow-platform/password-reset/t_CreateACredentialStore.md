---
title: Configure the connection to a credential store for the Password Reset processes
description: You create a Password Reset credential store record to configure access to your credential store server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Credential stores for Password Reset, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the connection to a credential store for the Password Reset processes

You create a Password Reset credential store record to configure access to your credential store server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.

## Before you begin

Role required: none

## About this task

-   For an AD credential store, skip this procedure and instead follow the instructions in [Integrate Password Reset with your Active Directory service](t_ConPassResetActiveDir.md). The Password Reset Windows Application supports only AD credential stores.
-   Configuration for multiple connections using a child alias. You can configure a connection credential alias with multiple child connections and map the child connection to a password reset credential store. The connections are used during the run time in the password reset flows. With this configuration password reset flows can support multiple Active Directory server credentials in Workflow Studio.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Credential Stores**.

2.  Select the following sample credential store.

    **Local ServiceNow Instance** credential store

3.  Enter a unique and meaningful **Name** and **Description**, and then on the Password Reset Credential Store form, fill in the fields.

    For information about the fields on the Password Reset Credential Store form, see [Password Reset Credential Store form](../reference/password-reset-credential-store-form.md).

4.  Click **Submit**.

5.  If you use the Local ServiceNow Instance credential store and you selected the **Enforce history policy** check box, then follow these steps:

    1.  Open the Password Reset process that is associated with the credential store: **Password Reset** &gt; **Processes**.

    2.  On the **Password Reset Details** tab of the Password Reset Process form, clear the **Auto-generate password** check box and then save the process definition.

6.  Select [Enable password policies on your instance](https://www.servicenow.com/docs/access?context=enable-password-policies&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

7.  [Test the connection to the credential store](test-cxn-to-credential-store.md).


**Parent Topic:**[Credential stores for Password Reset](../concept/c_CredentialStores.md)

**Related topics**  


[Configure the required strength for passwords](config-pwd-strength-rqmts.md)

