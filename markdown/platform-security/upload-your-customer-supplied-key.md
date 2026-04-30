---
title: Upload your customer-supplied key
description: Upload your wrapped symmetric data encryption key to your instance to begin using it work encryption.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-31"
reading_time_minutes: 1
breadcrumb: [Configure Customer-supplied keys for Field Encryption Enterprise, Configuring Field Encryption, Field Encryption, Encryption]
---

# Upload your customer-supplied key

Upload your wrapped symmetric data encryption key to your instance to begin using it work encryption.

## Before you begin

Role required: KMF Admin or KMF Cryptographic Manager

## About this task

**Note:** If you don't want to supply your own key, you can use the steps in [Configure Field Encryption modules](configure-fe-modules.md) to use a ServiceNow. You cannot revoke a customer supplied key.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Modules**.

2.  Open a field encryption module where you want to use your key.

3.  In the **Module** related list, open the cryptographic specific record by selecting the name under **Key alias**.

4.  Select the **Next** button until you reach the **Key Origin** section.

5.  Verify that the **Origin** field has a value of **Upload customer supplied key**.

    If it doesn’t, and you don’t can choose that value, please refer to steps 3–5 in [Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md).

6.  Confirm that you have a value in the **Key Alias** field.

7.  Select **Next**.

8.  Select the **Upload customer supplied key** link.

    This link should appear underneath the **Download wrapping key** link that you selected as part of wrapping your key.

9.  Select **Browse**, and select two files:

    1.  The wrapped\_key\_material file
    2.  The “import token” file
10. Select **OK**.


## Result

A confirmation message displays a successful upload of the customer-supplied key. The key is also listed in the **Module Keys** related list with an **Origin** of `customer-supplied key`.

Now that your encryption key is configured, you can begin to specify which fields and attachments are encrypted. For details, see [Configure encrypted field configurations for fields or attachments](configure-fe-fields-attachments.md).

**Parent Topic:**[Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md)

