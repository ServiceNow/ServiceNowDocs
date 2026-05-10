---
title: Configure and upload your customer supplied key
description: You can use your own customer-supplied key instead of using the ServiceNow system-generated keys.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using customer-supplied keys with Field Encryption Enterprise, Using Field Encryption, Field Encryption, Encryption]
---

# Configure and upload your customer supplied key

You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.

## Before you begin

Role required: security\_admin  and sn\_kmf.cryptographic\_manager  or sn\_kmf.admin

If you’re NOT supplying your own keys, you don’t need to perform this procedure. To create a cryptographic module with ServiceNow® keys, go to [Create a cryptographic module](create-cryptographic-module.md) or [Create cryptographic module for Field Encryption](create-PE-cryptographic-module.md).

**Note:** This procedure only applies to Field Encryption Enterprise functionality. See [Activate Field Encryption](../../now-platform-encryption/task/activate-platform-encryption.md) for more information.

**Important:** You can’t revoke a customer supplied key.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience**.

2.  Select **View module details** on the Field Encryption module.

3.  Select **Encryption Keys** and **Select and Continue** for the **Bring-your-own Key** option.

4.  Select **Download wrapping key** and **Next**.

5.  Follow the required online steps and select the **I completed the online steps** box followed by **Done and continue to the next step**.

6.  Upload the wrapped encryption key and the import token downloaded with the wrapped key, enter a name for the encryption key, and select **Complete provisioning**.


## What to do next

Now that you have finished configuring your cryptographic module with your customer-supplied key, move on to [Create a module access policy](create-module-access-policy.md)

**Parent Topic:**[Using customer-supplied keys with Field Encryption Enterprise](../../encryption/concept/csk-landing.md)

**Parent Topic:**[Using customer supplied keys with Column Level Encryption Enterprise](../../encryption/concept/csk-landing-2.md)

