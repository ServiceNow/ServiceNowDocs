---
title: Key management operations
description: The Key Management Operations submodule provides access to view and manage all encryption keys used with ServiceNow Cloud Encryption.Rotate the active Cloud Encryption ServiceNow managed key.Follow these steps to prepare your customer managed key for upload to your instance.Switch between customer-managed key or a ServiceNow managed keys for use in ServiceNow Cloud Encryption.Rotate your customer managed key to your instance after you’ve wrapped your customer managed key for Cloud Encryption.Use your customer managed key for ServiceNow Cloud Encryption.Switch from a customer managed key back to a managed key for ServiceNow Cloud Encryption.Set a schedule for automatic rotation of your ServiceNow managed keys. This process automatically retires an encryption key and replaces the old key with a newly generated cryptographic key. If you're using a customer managed key, this schedule can provide a reminder to rotate your custom keys manually.After the customer managed key withdrawal functionality is activated, a withdrawal operation becomes available in the Key Management Operations page. Withdraw key and quorum approval operations can also be managed.After a key withdrawal operation has completed, your customer managed key must be resupplied into your instance.
locale: en-US
release: australia
product: Cloud Encryption
classification: cloud-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Cloud Encryption with Key Management, Encryption]
---

# Key management operations

The Key Management Operations submodule provides access to view and manage all encryption keys used with ServiceNow Cloud Encryption.

Getting started with Cloud Encryption

## Key life cycle states

There’s only one active key in the system at any given time. When selecting a key, you access the activity for the selected key, such as which keys were rotated or withdrawn and the corresponding timestamp.

The key life-cycle state updates according to the key management operation performed.

![Shows updated key lifecycle states.](../image/key-mgmt-operations-key-states.png)

See [Rotate a ServiceNow managed key](key-mgmt-operations-ce.md#) or [Rotate a customer managed key](key-mgmt-operations-ce.md#) for details.

**Note:** The key rotation process may take up to 20 minutes to complete.

**Parent Topic:**[Cloud Encryption with Key Management](../concept/dare-overview.md)

## Rotate a ServiceNow managed key

Rotate the active Cloud Encryption ServiceNow managed key.

### Before you begin

Roles required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

**Important:** If you’re using customer-managed keys, see [Rotate a customer managed key](key-mgmt-operations-ce.md#).

### Procedure

1.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Key Management Operations**.

    The Cloud Encryption Key Metadata list loads. All keys used in your Instance are listed. Only one key can be active at a given time.

    If accessing the Cloud Encryption module for the first time, key entries will be available after an initial key rotation is performed. A ServiceNow managed key is the default in the system.

2.  Select the active key from the table.

    The Key Definition table displays with general information about your ServiceNow generated key.

3.  Select the **Rotate Key** button.

    A notification displays with the option to continue the key rotation or to cancel the operation.

4.  Select **OK** to rotate the key.

    A confirmation message displays at the top of the Key Definition page.

5.  Return to the Key Management Operations screen to refresh the Cloud Encryption Key Metadata table.

    Entries are listed for the current active key and the key that is being generated to rotate in place of the current active key. See [Key Management Framework key life-cycle states](../../key-management-framework/reference/key-life-cycle-states.md) for the different available states.

    The active key is listed with a key version of 0 and the generated key has a version of 1.

6.  Open the entry for the original key to view the Key Management Transactions.

    For more information, see [Key management transactions](key-mgmt-transactions-ce.md) for more information.

    The previously active key, version 0, updated to the key life cycle state of Rotated and the new key, version 1 is Active.


## Prepare your customer managed key

Follow these steps to prepare your customer managed key for upload to your instance.

### Before you begin

Roles required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

### About this task

For a customer managed key, you may use any cryptographic library or HSM to generate your key. This key must be an AES 256-bit key and be wrapped by a Cloud Encryption wrapping certificate with an RSAES\_OAEP\_SHA\_256 encryption schema.

**Note:**

If you choose to use the OpenSSL cryptographic tool to generate your key, the OpenSSL version must be version 1.1.1x or later.

If you’re creating and wrapping your customer-managed key using Windows, you must generate the wrapped key via Bash shell support applications such as Git Bash.

### Procedure

1.  Generate a random value to use as your AES-256 bit symmetric key using OpenSSL.

    For example, using openSSL you can generate this key with the `openssl rand 32` command.

    For compatibility, your symmetric key must have the following attributes:

<table id="table_ahl_zdp_tsb"><thead><tr><th>

Attribute

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Key type

</td><td>

Advanced Encryption Standard \(AES\) algorithm-based symmetric key.

</td></tr><tr><td>

Key size

</td><td>

256 bits \(32 bytes\)

</td></tr><tr><td>

Key wrapping requirement

</td><td>

-   RSA encryption algorithm
-   Optimal Asymmetric Encryption Padding \(OAEP\)
-   SHA-256 hash function \(RSAES\_OAEP\_SHA\_256\)
-   Encoded using Base64 algorithm


</td></tr></tbody>
</table>2.  Save the key to a file.

    For example, the openSSL command `openssl rand 32 > plaintext_key.bin` generates a 32-byte key and saves it to a file named `plaintext_key.bin`.

    **Important:** Save this file securely for future reference. This key is wrapped with the public key for upload.

3.  Extract the public key from the downloaded wrapping certificate file from your instance:

    ```
    openssl x509 -pubkey -noout -in wrapping_cert.pem > public_key.pem
    ```

    **Note:** Refer to for information to download the wrapping certificate.

4.  Wrap the generated key with the public key downloaded with the wrapping certificate using the RSAES\_OAEP\_SHA\_256 algorithm:

    ```
    cat plaintext_key.bin | openssl pkeyutl -encrypt -inkey public_key.pem -pubin -pkeyopt rsa_padding_mode:oaep -pkeyopt rsa_oaep_md:sha256 | openssl base64 -A -out wrapped_key.txt
    ```

    A file specified on this command contains a wrapped customer-managed key that can be provided to SN for the CMK process.


## Switch between ServiceNow and customer-managed keys

Switch between customer-managed key or a ServiceNow managed keys for use in ServiceNow Cloud Encryption.

By default, your instance is configured to use ServiceNow managed keys, and ServiceNow encryption key generation is active. However, administrators can choose to use customer-managed keys. They may also choose to return to ServiceNow managed keys.

## Rotate a customer managed key

Rotate your customer managed key to your instance after you’ve wrapped your customer managed key for Cloud Encryption.

### Before you begin

Roles required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

### Procedure

1.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Key Management Operations**.

    The **Cloud Encryption Key Metadata** list loads. All keys that have been used in your instance are listed.

2.  In the **Cloud Encryption Key Metadata** list, open the record for your active key.

    If you have multiple keys, select the key that has a **Key Lifecycle state** of `Active`. There’s only one active key on your instance.

3.  In the key definition record, select the **Rotate Key** button.

4.  In the **Upload Customer Managed key** window perform the listed steps.

    1.  Select **Download Wrapping Certificate**.

        The public\_certificate....zip downloads to your local machine and is used to wrap your customer managed key.

        **Warning:** Avoid potential certificate-related issues by downloading the wrapping certificate each time you rotate to or switch to a customer managed key.

    2.  Select **Browse** to upload your customer manged key, then locate and select your wrapped encryption key.

        To choose a different file, select the file and select **Remove**.

    3.  Close the Attachments window.

    4.  Select **OK** to upload your key.

        If the key is in the proper format, a confirmation message appears, otherwise an error message displays. The key file is attached to the Key Definition record.

        In the Key Management Transactions table, the certificate download and key upload steps are listed. See [Key management transactions](key-mgmt-transactions-ce.md) for details on the request steps.

5.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Key Management Operations** to see the list of keys.

    In the list of keys, you can see a new record for your customer managed key. This new key has a **Origin** value of **customer\_supplied** and is in the **Active** state. Your previous key has be in the **Rotated** state.


## Switch to a customer managed key

Use your customer managed key for ServiceNow Cloud Encryption.

### Before you begin

Role required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

To switch to a customer managed key, you must have a wrapped customer managed key ready to upload as part of these steps. For details on preparing this key for upload, see [Prepare your customer managed key](key-mgmt-operations-ce.md#). After uploading your key, this process will initiate a key rotation to your new key.

### Procedure

1.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Key Management Operations**.

2.  In the **Cloud Encryption Key Metadata** list, open the record for your active key.

    If you have multiple keys, select the key that has a **Key Lifecycle state** of `Active`. There’s only one active key on your instance.

3.  In the **Related Links** section of the form, select the **Switch To Customer Managed Key** link.

4.  In the **Switch to Customer Managed Key** dialog box, select the **Upload Managed Key** button.

5.  In the **Upload Customer Managed Key** dialog box, perform the listed steps.

    1.  Select **Download Wrapping Certificate**.

        **Warning:** Avoid potential certificate-related issues by downloading the wrapping certificate each time you rotate to or switch to a customer managed key.

    2.  Select **Browse**, and follow the prompts to select and upload your key from your device.

    3.  Select **Switch to Customer Managed Key**.

    A request is generated by the instance to switch to your customer managed key. In the current form, you can see that the **Key lifecycle state** of the originally active key has changed to **Rotated**.

6.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Key Management Operations** to see the list of keys.

    In the list of keys, you can see a new record for your customer managed key. This new key has a **Origin** value of **customer\_supplied** and is in the **Active** state.


### Result

Your instance now uses your customer managed key for ServiceNow Cloud Encryption.

**Important:** Ensure that a copy of your encryption key is always available in a secure location for key management operations. Without this key, your instance may be rendered inaccessible.

## Switch to a ServiceNow managed key

Switch from a customer managed key back to a managed key for ServiceNow Cloud Encryption.

### Before you begin

Role required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

### Procedure

1.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Key Management Operations**.

2.  In the **Cloud Encryption Key Metadata** list, open the record for your active key.

    If you have multiple keys, select the key that has a **Key Lifecycle state** of `Active`. There’s only one active key on your instance.

3.  In the **Related Links** section of the form, select the **Switch To ServiceNow Managed Key** link.

4.  In the **Switch to ServiceNow Managed Key** dialog box, select the **Switch to ServiceNow Managed Key** button.

    A request is generated by the instance to switch to a ServiceNow managed key. In the current form, you can see that the **Key lifecycle state** of the originally active key has changed to **Rotated**.

5.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Key Management Operations** to see the list of keys.

    In the list of keys, you can see a new record for a ServiceNow managed key is. This new key has a **Origin** value of **ServiceNow** and is in the **Active** state.


## Schedule key rotation

Set a schedule for automatic rotation of your ServiceNow managed keys. This process automatically retires an encryption key and replaces the old key with a newly generated cryptographic key. If you're using a customer managed key, this schedule can provide a reminder to rotate your custom keys manually.

### Before you begin

Role required: sn\_kmf.admin

### Procedure

1.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **Scheduled Key Rotation Settings**.

2.  Select the **Enable scheduled key rotation** check box.

3.  Fill in the remaining fields based on your business needs.

    |Field|Description|
    |-----|-----------|
    |Number of months between key rotations \(Maximum of 60 months\)|Number of months between key rotations. This value is `12` by default and can have a maximum of `60` months.|
    |Day of the week to perform key rotation|Day of the week the key rotation is performed.|
    |Time of day to perform key rotation|Time of day the key rotation is performed.|
    |Date and time of next key rotation|Date and time of the next scheduled key rotation. This value isn't editable directly, and is automatically calculated based on your choices.|
    |Number of days before key rotation to send reminder \(Maximum of 15 days\)|Number of days before the date of your key rotation that your instance sends notifications.|
    |Email notifications are sent to the following list of your approved security administrators|List of users who receive notifications for key rotation. The **System Administrator** is on this list by default.|

4.  Select **Submit**

    After selecting submit, you can see a notification at the top of the form. The notifications confirm your key rotation and notification schedule.

    **Warning:**

    Each scheduled key rotation has a unique signature, which ensures the integrity of a job and detect any unauthorized modification. The signature for a scheduled job is unique on each instance. Cloning a scheduled key rotation job from a source instance A to a target instance B, the scheduled job on the instance B will fail the signature validation. If this occurs, you can re-create the signature by de-selecting and then reselecting the **Enable scheduled key rotation** check box. For more details on this issue, see [KB1247113](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1247113).


## Withdraw a customer managed key

After the customer managed key withdrawal functionality is activated, a withdrawal operation becomes available in the Key Management Operations page. Withdraw key and quorum approval operations can also be managed.

### Before you begin

Roles required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

This section applies only if you've licensed Cloud Encryption Withdraw and Resupply, an optional add-on to Cloud Encryption.

### Procedure

1.  Navigate to **All** &gt; **Cloud Encryption Key Management** &gt; **** &gt; **Key Management Operations**.

2.  Select the active customer managed key from the table.

    The Key Definition table displays with general information about your customer key. A withdraw key function is now available.

3.  Select the **Withdraw Key** to trigger the withdrawal process.

    **Warning:**

    A Withdraw Key warning message displays. The withdrawal of the key triggers a shutdown of your instance until a restore operation is performed with the withdrawn key.

    **Danger**

    You can only perform a restore operation with the same key that was withdrawn. If you want to rotate to another key, you must do so after restoring the key that was withdrawn.

    If the withdrawn customer managed key isn’t restored within the time frame for which ServiceNow retains backups \(see the Backup and Restoration SOP \[Standard Operating Procedure\] for details\), your instance database backups will no longer be accessible. Backup data lost in this way isn’t recoverable.

4.  Select **OK** to withdraw the key.

    Select **Cancel** if there’s any doubt about the key withdrawal function.

    You’re returned to the Key Definition screen and a confirmation message displays.

5.  Refresh the Key Definition page to view the pending withdrawal request.

    ![Key management transaction](../image/process-key-withdrawal.png)

    If the Quorum Control Policy has been activated, the approval workflow must be completed successfully to complete the key withdrawal. See [Manage Quorum Control](quorum-ctrl-mgmt.md) for details.


## Resupply a customer managed key

After a key withdrawal operation has completed, your customer managed key must be resupplied into your instance.

### Before you begin

Role required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

**Note:** This section applies only if you've licensed Cloud Encryption Withdraw and Resupply.

### Procedure

1.  Go to Now Support and navigate to **Service Catalog** &gt; **Catalog** &gt; **Instance Management** &gt; **Instance Restore - Resupply Managed Key**.

2.  Click **Request**.

3.  In the **Instance Restore - Resupply Managed Key** window, select your instance in the **Select Instance** drop-down.

4.  Download the wrapping certificate by clicking on the **wrapping certificate** text.

    **Warning:** You must download a new wrapping certificate each time you rotate or upload a customer managed key.

5.  Prepare your key for upload.

    For details on this process, see [Prepare your customer managed key](key-mgmt-operations-ce.md#).

6.  In the **Step 4** section, click **Browse and upload** to upload your wrapped key from your local device.

    After your key is uploaded, you can see the key under **Uploaded below file successfully**. If you need to re-upload the key, click **Remove file** and upload your key again as described in previous steps.

7.  Click **Rotate key** to complete the re-supply.


