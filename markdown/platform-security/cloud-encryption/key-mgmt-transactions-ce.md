---
title: Key management transactions
description: The Key Management Transactions submodule displays all transactions that have occurred for the keys in your ServiceNow instance.
locale: en-US
release: zurich
product: Cloud Encryption
classification: cloud-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Encryption with Key Management, Encryption]
---

# Key management transactions

The Key Management Transactions submodule displays all transactions that have occurred for the keys in your ServiceNow instance.

-   A key transaction is defined by the following:
    -   composed of several request steps.
    -   A single Request ID is shared across all request steps.
    -   The initial step, request sequence 0, of a transaction provides the current state of the overall transaction.

        As seen in the image below, the initial step 0 has an overall Request Status of Completed.

-   The following can be identified for the transaction by the individual request step:
    -   The order of each step in a transaction can be identified by the sequence number for the step.
    -   The status of each transaction is visible through the status of the request step.
    -   If any steps beyond the initial step fail, the overall transaction has a status of Failed. If all steps are completed, the transaction status is also completed.

The following screen is a sample of the type of information that displays with a ServiceNow key rotation.

![Displays the key management transactions upon rotation.](../image/key-mgmt-transactions.png)

The following table displays the field information available on the Key Managements Transactions page.

<table id="table_isl_mc5_crb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request ID

</td><td>

Unique system-generated Id for the action being performed One request ID is shared across all request steps.

</td></tr><tr><td>

Request action

</td><td>

Displays the action for the key operation being performed.

</td></tr><tr><td>

Request status

</td><td>

-   Processing: A request has been entered but hasn’t yet been completed.
-   Completed: The request has been completed successfully.
-   Failed: An issue occurred and the process hasn’t been completed.

**Note:** Contact Customer Service and Support and provide the request number where the failure occurred.


</td></tr><tr><td>

Key alias

</td><td>

Alphanumeric entry.

</td></tr><tr><td>

Key life-cycle state

</td><td>

See [Key Management Framework key life-cycle states](../../key-management-framework/reference/key-life-cycle-states.md) for definitions.

</td></tr><tr><td>

Origin

</td><td>

-   ServiceNow key
-   Customer-managed key

</td></tr><tr><td>

Key version

</td><td>

When a key rotates, the version number increments.

</td></tr><tr><td>

Request sequence

</td><td>

Displays the order in which a request is being processed in the system.

</td></tr><tr><td>

Request step

</td><td>

Displays whether a step is being processed in the system during key rotation. The quantity and content of the steps vary based on the type of key operation performed.1.  request\_preparation: Creates a request to trigger and the wrapping and rotation.
2.  request\_integrity\_check: Validates that the request is legitimate and secure.
3.  request\_validation: Validates that there’s a request in progress, only one rotate request can be processed at a time.
4.  attachment\_process: Extracts the wrapped key material from the attachment. \(Additional step when rotating a Customer Managed key.\)
5.  hsm\_&lt;key type&gt;\_upload: Uploads the wrapped key material to the HSM, KeySecure.
6.  key\_metadata\_rotate: Generates the new key metadata.
7.  post\_rotate\_request: Sends a request to perform the key rotation.
8.  post\_rotate\_response: Response to perform the key rotation based on the request from the customer instance.

 **Note:** Provide the request step to Customer Service and Support to analyze the status progression in case a request step doesn’t complete.

</td></tr><tr><td>

Request step status

</td><td>

-   Completed: Rotation is successful.
-   Failed: Rotation isn’t successful.

**Note:** Provide the request step to Customer Service and Support to analyze the status progression in case a request step doesn’t complete.


</td></tr></tbody>
</table>**Parent Topic:**[Cloud Encryption with Key Management](../concept/dare-overview.md)

