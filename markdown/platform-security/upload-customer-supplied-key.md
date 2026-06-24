---
title: Configure and upload your customer supplied key
description: You can use your own customer-supplied key instead of using the ServiceNow system-generated keys.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/upload-customer-supplied-key.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using customer supplied keys with Field Encryption Enterprise, Using Field Encryption, Field Encryption, Encryption]
---

# Configure and upload your customer supplied key

You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.

## Before you begin

Roles required: security\_admin, sn\_kmf.cryptographic\_manager

If you’re NOT supplying your own keys, you don’t need to perform this procedure. To create a cryptographic module with ServiceNow® keys, go to [Create a cryptographic module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/create-cryptographic-module.md) or [Create cryptographic module for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/create-PE-cryptographic-module.md).

**Note:** This procedure only applies to Field Encryption Enterprise functionality. See [Activate Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/activate-platform-encryption.md) for more information.

**Important:** You can’t revoke a customer supplied key.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Settings** and verify that **Customer Supplied Keys** is selected.

    \[Omitted image "fieldencryptionsettingsbyok2.png"\] Alt text: Field Encryption Settings Key Source selection form.

2.  Select **Submit**.

3.  Return to **System Security** &gt; **Field Encryption Modules** &gt; **** &gt; **Create New**.

    \[Omitted image "pe-cryptomodule.png"\] Alt text: Field Encryption create crypto module form.

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

    The system populates the Crypto purpose and the Algorithm for Field Encryption automatically and jumps to the **Key Origin** stage.

7.  Notice that **Upload customer supplied key** is the **Origin** and the **Key alias** is already populated.

    \[Omitted image "origin-csk.png"\] Alt text: Crypto specification key origin of CSK

8.  Select **Next** to move to the **Key Creation** stage.

    There are two links:

    -   **Download wrapping key** downloads the key in a zip file containing an import token and a public key certificate, `.PEM` file. Use the import token to verify successful key wrapping according to security specification for the instance. Use the public key certificate `.PEM` file to wrap your customer supplied key securely before uploading it along with the token.
    -   **Upload customer supplied key** opens the file browser to select the token and the encrypted key that you wrapped.
    \[Omitted image "key-creation-links2.png"\] Alt text:

9.  Select **Download wrapping key** to save the token.

    Save the token to the same destination location as the key is saved on your system. Don’t rename the downloaded token.

10. Run the BYOK command on a terminal to wrap the key.

    For more information, refer to [Wrap your customer-supplied key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/wrap-customer-supplied-key.md).

11. Select **Upload customer supplied key**.

12. Select **Browse** to select the two files, the wrapped key and the token file.

    The Attachments window displays the two files.

    \[Omitted image "wrapped-key-attachments.png"\] Alt text: Attachment upload window.

    Select a file to remove and reupload, if necessary.

13. Select **OK**.

    You're returned to the Cryptographic Module screen. A confirmation message displays for a successful upload of the customer key. The key is also listed in the Module Keys related list.

    \[Omitted image "uploaded-key.png"\] Alt text: Module Keys table with customer-supplied key uploaded.


## What to do next

Now that you have finished configuring your cryptographic module with your customer-supplied key, move on to [Create a module access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/create-module-access-policy.md)

**Parent Topic:**[Using customer supplied keys with Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/csk-landing.md)

**Parent Topic:**[Using customer supplied keys with Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/csk-landing-2.md)

