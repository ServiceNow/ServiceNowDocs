---
title: Configure the connection to a credential store for the Password Reset processes
description: You create a Password Reset credential store record to configure access to your credential store server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/password-reset/t\_CreateACredentialStore.html
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Credential stores for Password Reset, Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the connection to a credential store for the Password Reset processes

You create a Password Reset credential store record to configure access to your credential store server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.

## Before you begin

Role required: password\_reset\_admin

## About this task

-   For an AD credential store, skip this procedure and instead follow the instructions in [Integrate Password Reset with your Active Directory service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_ConPassResetActiveDir.md). The Password Reset Windows Application supports only AD credential stores.
-   Configuration for multiple connections using a child alias. You can configure a connection credential alias with multiple child connections and map the child connection to a password reset credential store. The connections are used during the run time in the password reset flows. With this configuration password reset flows can support multiple Active Directory server credentials in Workflow Studio.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Credential Stores**.

2.  Select the following sample credential store.

    **Local ServiceNow Instance** credential store

3.  Enter a unique and meaningful **Name** and **Description**, and then on the Password Reset Credential Store form, fill in the fields.

    For information about the fields on the Password Reset Credential Store form, see [Password Reset Credential Store form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/password-reset-credential-store-form.md).

4.  Click **Submit**.

5.  If you use the Local ServiceNow Instance credential store and you selected the **Enforce history policy** check box, then follow these steps:

    1.  Open the Password Reset process that is associated with the credential store: **Password Reset** &gt; **Processes**.

    2.  On the **Password Reset Details** tab of the Password Reset Process form, clear the **Auto-generate password** check box and then save the process definition.

6.  Select [Enable password policies on your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/enable-password-policies.md)

7.  [Test the connection to the credential store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/test-cxn-to-credential-store.md).


**Parent Topic:**[Credential stores for Password Reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/c_CredentialStores.md)

**Related topics**  


[Configure the required strength for passwords](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/config-pwd-strength-rqmts.md)

