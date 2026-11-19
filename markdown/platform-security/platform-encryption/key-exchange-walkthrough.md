---
title: Recurring Key Exchange walkthrough
description: Use this walkthrough to set up a recurring key exchange in your instance using Resource Exchange.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/key-exchange-walkthrough.html
release: brazil
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Recurring Key Exchange walkthrough

Use this walkthrough to set up a recurring key exchange in your instance using Resource Exchange.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## About this task

This example shows you how a target instance requests keys from a host instance.

-   Before you can perform this procedure, you must clone an instance. For more information, see the System clone documentation for your instance.
-   **Automatic Key Exchange**: The base system property **glide\_encryption.auto\_key\_exchange.enabled** is **true** by default, meaning that automatic is activated when cloning an instance. The property is cloned over to the target instance.
-   Turn off automatic by setting the property to **false**.

## Procedure

1.  On the source instance, create or access a crypto module using column\_level\_encryption.

    Verify that keys have been generated in the module, then set up the encrypted field configurations for Key Exchange ciphertext encryption. See [Create a cryptographic specification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/create-crypto-spec.md) and [Generate a ServiceNow cryptographic key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/generate_sn_key.md) for details.

    **Note:** The instance automatically creates a module access policy when the clone request runs.

2.  On the source instance and on the cloned target instance, select **Enroll module for resource exchange** on the Algorithm Definition form for the crypto specification.

    The module must be enrolled on both instances before you create a resource exchange request. \[Omitted image "resource\_exchange.png"\] Alt text: Algorithm Definition form with the Enroll module for resource exchange check box highlighted.

3.  From the cloned instance, navigate to **Key Management** &gt; **Resource Exchange Requests** &gt; **New**.

4.  Complete the form and select **Recurring Clone** as the Exchange Frequency.

5.  From the target instance of the clone, navigate to **Key Management** &gt; **Resource Exchange Requests**.

    The request from the host instance is displayed in the table.

    \[Omitted image "view-key-exchange.png"\] Alt text: Requests page with pending requests on Target.

    **Warning:** For both one-time and recurring clone requests, the instance creates a module access policy automatically. You don’t need to configure a policy manually. At clone time, this policy on the source instance auto-approves the request and sends keys to the newly cloned target.

    \[Omitted image "module-access-policy-RE-auto.png"\] Alt text: Shows the module access policy is auto-generated.

    In the Requests form, the status updates to **Request Approved** and the **Imported Key Count** field appears on the record.

    \[Omitted image "request-approved.png"\] Alt text: Request screen shows number of imported and exported key counts.

6.  Return to the host instance.

7.  View the Request record to see the number of exported keys.

8.  View the Module Access Policy record to see that the **Type** is Resource Exchange.

    \[Omitted image "source-success.png"\] Alt text: Shows module access policy of type Resource Exchange.

    **Note:** Resource Exchange enables rekeying of ciphertext on the target instance.


## Result

After a key exchange is attempted, your non-production instance updates the **protected.script.values.kmf.rekeyed** system property. This property is visible in the System Properties \[sys\_properties\] table. If the encryption using the exchanged key is successful, this property has a value of **true**. Otherwise, the property has a value of **false**. If the value is false, the instance attempts to encrypt again the next day.

**Parent Topic:**[Key Management Framework Resource Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/resource-exchange.md)

