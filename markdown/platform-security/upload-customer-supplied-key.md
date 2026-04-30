---
title: Configure and upload your customer supplied key
description: You can use your own customer-supplied key instead of using the ServiceNow system-generated keys.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using customer supplied keys with Column Level Encryption Enterprise, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Configure and upload your customer supplied key

You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.

## Before you begin

Roles required: security\_admin, sn\_kmf.cryptographic\_manager

If you’re NOT supplying your own keys, you don’t need to perform this procedure. To create a cryptographic module with ServiceNow® keys, go to [Create a cryptographic module](create-cryptographic-module.md) or [Create cryptographic module for Column Level Encryption](create-PE-cryptographic-module.md).

**Note:** This procedure only applies to Column Level Encryption Enterprise functionality. See [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md) for more information.

**Important:** You can’t revoke a customer supplied key.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Settings** and verify that **Customer Supplied Keys** is selected.

    ![Field Encryption Settings Key Source selection form.](../image/fieldencryptionsettingsbyok2.png "Key source selection")

2.  Select **Submit**.

3.  Return to **System Security** &gt; **Field Encryption Modules** &gt; **** &gt; **Create New**.

    ![Column Level Encryption create crypto module form.](../image/pe-cryptomodule.png "Create new cryptographic module")

4.  Complete the Cryptographic Module form as follows:

<table id="table_tqb_5rv_rnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Module Name

</td><td>

Enter a name for the module.

</td></tr><tr><td>

Crypto spec template

</td><td>

The default cryptographic template is selected.

</td></tr><tr><td>

Name

</td><td>

Auto-populates based on the module name and prepends the name with the scope to ensure which application is being applied. In this case, the global scope is applied.

</td></tr><tr><td>

Crypto module lifecycle state

</td><td>

Select **Published** to activate the crypto module.

</td></tr><tr><td>

Parent crypto module

</td><td>

The parent module **column\_level\_encryption** is selected automatically when using customer-supplied keys and encryption modules.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  Select the newly created cryptographic module from the table.

    In the **Crypto Specifications** related list, select the auto-generated key alias with the AES 256 CFB algorithm.

    The system populates the Crypto purpose and the Algorithm for Column Level Encryption automatically and jumps to the **Key Origin** stage.

7.  Notice that **Upload customer supplied key** is the **Origin** and the **Key alias** is already populated.

    ![Crypto specification key origin of CSK](../image/origin-csk.png "Key origin")

8.  Select **Next** to move to the **Key Creation** stage.

    There are two links:

    -   **Download wrapping key** downloads the key in a zip file containing an import token and a public key certificate, `.PEM` file. Use the import token to verify successful key wrapping according to security specification for the instance. Use the public key certificate `.PEM` file to wrap your customer supplied key securely before uploading it along with the token.
    -   **Upload customer supplied key** opens the file browser to select the token and the encrypted key that you wrapped.
    ![](../image/key-creation-links2.png "Key creation upload links")

9.  Select **Download wrapping key** to save the token.

    Save the token to the same destination location as the key is saved on your system. Don’t rename the downloaded token.

10. Run the BYOK command on a terminal to wrap the key.

    For more information, refer to [Wrap your customer-supplied key](../../encryption/task/wrap-customer-supplied-key.md).

11. Select **Upload customer supplied key**.

12. Select **Browse** to select the two files, the wrapped key and the token file.

    The Attachments window displays the two files.

    ![Attachment upload window.](../image/wrapped-key-attachments.png "Wrapped key attachments upload")

    Select a file to remove and reupload, if necessary.

13. Select **OK**.

    You're returned to the Cryptographic Module screen. A confirmation message displays for a successful upload of the customer key. The key is also listed in the Module Keys related list.

    ![Module Keys table with customer-supplied key uploaded.](../image/uploaded-key.png "Confirmation of key upload")


## What to do next

Now that you have finished configuring your cryptographic module with your customer-supplied key, move on to [Create a module access policy](create-module-access-policy.md)

**Parent Topic:**[Using customer supplied keys with Column Level Encryption Enterprise](../../encryption/concept/csk-landing.md)

