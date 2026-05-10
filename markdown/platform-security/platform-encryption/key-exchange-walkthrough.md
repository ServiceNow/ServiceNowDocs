---
title: Recurring Key Exchange walkthrough
description: Use this walkthrough to set up a recurring key exchange in your instance using and Resource Exchange.
locale: en-US
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Recurring Key Exchange walkthrough

Use this walkthrough to set up a recurring key exchange in your instance using and Resource Exchange.

## Before you begin

Roles required: sn\_kmf.cryptographic\_manager

## About this task

This example shows you how a target instance requests keys from a host instance.

-   Before you can perform this procedure, you must clone an instance. See [Instance Clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md) for more information.
-   **Automatic Key Exchange**: The base system property **glide\_encryption.auto\_key\_exchange.enabled** is **true** by default, meaning that automatic is activated when cloning an instance. The property is cloned over to the target instance.
-   Turn off automatic by setting the property to **false**.

## Procedure

1.  On the source instance, create a crypto module or access an existing crypto module using column\_level\_encryption and set up the encrypted field configurations for the ciphertext encryption for Key Exchange.

    See and for details.

    1.  Ensure that keys have been generated in the crypto module.

    **Note:** Your instance automatically creates a module access policy on the execution of the clone request.

2.  From the cloned instance, navigate to **Key Management** &gt; **Resource Exchange Requests** &gt; **New**.

3.  Complete the form and select **Recurring Clone** as the Exchange Frequency.

4.  From the target instance of the clone, navigate to **Key Management** &gt; **Resource Exchange Requests**.

    The request from the host instance is displayed in the table.

    ![Requests page with pending requests on Target.](../image/view-key-exchange.png)

    **Important:** For both one-time and recurring clone requests, your instance creates a module access policy automatically. You don’t need to configure a policy manually. At clone time, this policy on the source instance is invoked to auto-approve the request and send keys to the newly cloned target.

    ![Shows the module access policy is auto-generated.](../image/module-access-policy-RE-auto.png)

    In the Requests form, the status updates to **Request Approved** and the **Imported Key Count** field appears on the record.

    ![Request screen shows number of imported and exported key counts.](../image/request-approved.png)

    ![]()

5.  Return to the host instance.

6.  View the Request record to see the number of exported keys.

7.  View the Module Access Policy record to see that the **Type** is Resource Exchange.

    ![Shows module access policy of type Resource Exchange.](../image/source-success.png)

    **Note:** Resource Exchange also supports rekeying of ciphertext on the target instance. See for details.


## Result

After a key exchange is attempted, your non-production instance updates the **protected.script.values.kmf.rekeyed** system property. This property is visible in the System Properties \[sys\_properties\] table. If the encryption using the exchanged key is successful, this property has a value of **true**. Otherwise, the property has a value of **false**. If the value is false, your instance will attempt to encrypt again the next day.

**Parent Topic:**[Key Management Framework Resource Exchange](../reference/resource-exchange.md)

