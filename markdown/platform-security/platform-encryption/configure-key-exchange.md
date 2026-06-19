---
title: Configure Key Exchange
description: Key Management Framework \(KMF\) generates automatic key exchange requests for supported cryptographic modules during the fresh installation or upgrade of the instance, and manages the data encryption key locally for the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/configure-key-exchange.html
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 3
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Configure Key Exchange

Key Management Framework \(KMF\) generates automatic key exchange requests for supported cryptographic modules during the fresh installation or upgrade of the instance, and manages the data encryption key locally for the instance.

## Before you begin

A cryptographic module with a key must be created in both the target and source instances before using Key Exchange.

Role required: sn\_kmf.cryptographic\_manager

## About this task

Key Exchange requests are initiated from the target instance.

Automatic Key Exchange is active by default when cloning an instance, where the property is cloned to the target instance. Along with KMF, configure system properties to manage how keys are handled during an instance clone:

-   **Turn off automatic key exchange:** Set the **glide\_encryption.auto\_key\_exchange.enabled** property to **false** for recurring clone requests.
-   **Send auto key exchange requests**: Set this property to **true**.

**Important:** The base system property is set to **true** by default, meaning that automatic key exchange is activated when cloning an instance. This value must be set to **false** if you're using the [Rekey ciphertext with Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/rekey-keyexchange.md) or the recurring Key Exchange functionality. See [Recurring Key Exchange walkthrough](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/key-exchange-walkthrough.md) for additional details.

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

The keys from the crypto specification in a crypto module define the keys to clone. For both one-time and recurring clone requests, your instance automatically creates a **Resource Exchange** module access policy. You don't need to configure a policy manually.**Note:** Select the lookup using list icon \(\[Omitted image "IconUI15GlobalTextSearch.png"\] Alt text: Lookup using list icon.\) to browse the available cryptographic specifications.

</td></tr><tr><td>

Enable Rekeying after Key Imported

</td><td>

Option to enable auto rekeying.

</td></tr></tbody>
</table>3.  Select **Submit**.

    If successful, a confirmation displays at the top of the form. The Requests table is updated with an entry of **Request Pending** in both the source instance and in the target instance. Open the Request Record to view the status of the request, the Imported Key Count, and the Total Key Count on the target or source host.

    \[Omitted image "resource-exchange-requests-table.png"\] Alt text: Shows the request status for Requests.

4.  In the source instance, approve the pending request to complete the exchange.

    The approval process depends on the exchange frequency you selected.

    -   **One Time Clone or Recurring Clone**

        The module access policy on the source instance auto-approves the request at clone time. No manual action is required.

    -   **Adhoc**

        Manually approve each pending request in the source instance:

        1.  Log in to the source instance and navigate to **All** &gt; **Key Management** &gt; **Resource Exchange Requests**.
        2.  Open a request with a status of **Request Pending**.
        3.  Change the **Status** field to **Request Approved**.
        4.  Select **Update Request**.

            **Important:** Select **Update Request**, not the standard **Update** button. Using the standard Update button does not complete the approval.

        5.  Repeat for each remaining **Request Pending** entry.
        **Note:** Not all crypto specifications requested may exist in the source instance. Requests for specifications not found in the source instance do not require approval.

    \[Omitted image "request-record.png"\] Alt text: Request Approved appears in the Status field on the Request record.


## Result

After a key exchange is attempted, your non-production instance updates the **protected.script.values.kmf.rekeyed** system property. This property is visible in the System Properties \[sys\_properties\] table after a key exchange is attempted. If the encryption using the exchanged key is successful, this property has a value of **true**. Otherwise, the property has a value of **false**. If the value is false, the instance will attempt to encrypt again the next day.

**Parent Topic:**[Key Management Framework Resource Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/resource-exchange.md)

