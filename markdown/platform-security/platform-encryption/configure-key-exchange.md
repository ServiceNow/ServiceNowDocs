---
title: Configure Key Exchange
description: Key Management Framework \(KMF\) generates automatic key exchange requests for supported cryptographic modules during the fresh installation or upgrade of the instance. manages the data encryption key locally for the instance.
locale: en-US
release: yokohama
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Configure Key Exchange

Key Management Framework \(KMF\) generates automatic key exchange requests for supported cryptographic modules during the fresh installation or upgrade of the instance. manages the data encryption key locally for the instance.

## Before you begin

A cryptographic module with a key must be created in both the target and source instances before using Key Exchange.

Role required: sn\_kmf.cryptographic\_manager

## About this task

Key Exchange requests are initiated from the target instance.

Automatic Key Exchange is active by default when cloning an instance, where the property is cloned to the target instance. Along with KMF, configure system properties to manage how keys are handled during an instance clone:

-   **Turn off automatic key exchange:** Set the **glide\_encryption.auto\_key\_exchange.enabled** property to **false** for recurring clone requests.
-   **Send auto key exchange requests**: Set this property to **true**.

**Important:** The base system property is set to **true** by default, meaning that automatic key exchange is activated when cloning an instance. This value must be set to **false** if you're using the [Rekey ciphertext with Key Exchange](../reference/rekey-keyexchange.md) or the recurring Key Exchange functionality. See [Recurring Key Exchange walkthrough](key-exchange-walkthrough.md) for additional details.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Resource Exchange Requests** &gt; **New**.

2.  On the form, fill in the fields.

<table id="table_inh_bsr_b4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Exchange Frequency

</td><td>

-   **Adhoc**: Sends requests from the key target instance to the source instance. Enter the instance sys\_id and the Host information for the Source. Not supported with Rekey of Key Exchange.
-   **One Time Clone**: One-time exchange of the keys from the source crypto specifications to the target instance.
-   **Recurring Clone**: Exchange keys from the selected source crypto specifications to the target instance on a defined recurring clone.


</td></tr><tr><td>

&lt;Source or Target&gt; Instance sys\_id

</td><td>

-   **Adhoc**: Enter the sys\_id for the source instance to request the keys from.
-   **One Time Clone**, **Recurring Clone**: Enter the sys\_id for the target instance that sends the requests.

**Tip:** Enter `stats.do` in the application navigator to locate the instance ID.

</td></tr><tr><td>

&lt;Source or Target&gt; Instance Host

</td><td>

Enter the host location or name of the source or target instance.**Tip:** For example `instanceA.service-now.com`

</td></tr><tr><td>

Crypto Specifications

</td><td>

The keys from the crypto specification in a crypto module define the keys to clone. For both one-time and recurring clone requests, your instance automatically creates a **Resource Exchange** module access policy. You don’t need to configure a policy manually.**Note:** Select the lookup using list icon \(![Lookup using list icon.](../../navigation-and-ui/image/IconUI15GlobalTextSearch.png)\) to browse the available cryptographic specifications.

</td></tr><tr><td>

Enable Rekeying after Key Imported

</td><td>

Option to enable auto rekeying.

</td></tr></tbody>
</table>3.  Select **Submit**.

    If successful, a confirmation displays at the top of the form. The Requests table is updated with an entry of **Request Pending** in both the source instance and in the target instance. Open the Request Record to view the status of the request, the Imported Key Count, and the Total Key Count on the target or source host.

    ![Shows the request status for Requests.](../image/resource-exchange-requests-table.png)

4.  The pending request is accepted in the source instance to complete the exchange.

    At clone time, the module access policy on the source instance is invoked to auto-approve the request and send keys to the newly cloned target.

    ![Request Approved appears in the Status field on the Request record.](../image/request-record.png)


## Result

After a key exchange is attempted, your non-production instance updates the **protected.script.values.kmf.rekeyed** system property. This property is visible in the System Properties \[sys\_properties\] table after a key exchange is attempted. If the encryption using the exchanged key is successful, this property has a value of **true**. Otherwise, the property has a value of **false**. If the value is false, the instance will attempt to encrypt again the next day.

**Parent Topic:**[Key Management Framework Resource Exchange](../reference/resource-exchange.md)

