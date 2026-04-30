---
title: Import an S/MIME key pair
description: Import an S/MIME key pair consisting of the private key and certificate to sign outbound emails or decrypt emails.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up S/MIME, Email encryption, Email Administration, Notifications, Configure core features, Administer]
---

# Import an S/MIME key pair

Import an S/MIME key pair consisting of the private key and certificate to sign outbound emails or decrypt emails.

## Before you begin

Role required: email\_account\_admin and sn\_kmf.cryptographic\_manager

Upload the private-public key pair corresponding to the instance email account.

You must have the key alias.

**Note:** When you create a PKCS12 file, ensure that it's created with a key alias.

Make sure the file format is PKCS \#12.

## About this task

This video shows you how to perform the following procedure.This video shows how to import an S/MIME key pair

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Email Accounts**.

2.  Select the email account.

    **Note:** The keypair is associated with the email address and not the email account.

3.  Select the **Import SMIME Key Pair** related link.

4.  Select the **Crypto Specifications** tab and select the key alias.

    The algorithm definition screen is displayed.

5.  Complete the Algorithm Definition form.

<table id="table_ud5_2zr_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Crypto module

</td><td>

Read only. Name of the selected cryptographic module displays.

</td></tr><tr><td>

Crypto purpose

</td><td>

SMIME Crypto Purpose

</td></tr><tr><td>

Algorithm

</td><td>

Type of algorithm used to accomplish the crypto purpose. The algorithm also controls the key origin. Adjusts automatically based on the selected crypto purpose.

</td></tr><tr><td>

Enroll module for resource exchange

</td><td>

Allows clones or backups to get their own unique keys.**Note:** Do not check the box.

</td></tr></tbody>
</table>6.  Select **Next**.

7.  In the **Lifecycle Definition** screen, select a Key Lifecycle from the Applies to column.

<table id="table_smt_wcs_g5b"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

Selected key that the lifecycle applies to.

</td></tr><tr><td>

For field

</td><td>

Control for the key that the lifecycle applies to.

</td></tr><tr><td>

Type

</td><td>

Select if the valuation for the key lifecycle is a relative value or an absolute value or none. Relative value depends on other data entries in the system, such as key generation, activation, and deactivation.

 Absolute value is an exact value, such as a date.

</td></tr><tr><td>

Lifecycle default

</td><td>

Read only. Displays a value if set.

</td></tr><tr><td>

Order

</td><td>

Enter the sequence in which to process the key lifecycle state for the crypto specification.

</td></tr><tr><td>

Relative duration

</td><td>

Number of years, months, or days the key is valid.

</td></tr><tr><td>

Relative duration type

</td><td>

Duration of the lifecycle: Years, Months, or Days.

</td></tr><tr><td>

Relative operation

</td><td>

**Before** or **After**.

</td></tr><tr><td>

Relative to

</td><td>

Field the duration is relative to. Displays if a relative duration or operation is selected.

</td></tr></tbody>
</table>8.  Select **Update**.

9.  Select **Next**.

10. In the Key Origin screen, in the **Origin** field select **Import from PKCS12** and enter the key alias in the **Key Alias** field.

11. Select **Next**.

12. In the Key Creation screen, select **Import Key**.

13. In the Import Keystore/Certificate dialog box, provide the keystore password and import the keystore/certificate.

    1.  Provide the password in the **Enter Keystore Password** field.

    2.  In the **Import Keystore/Certificate** field, select **Browse** and select the certificate to be imported.

    3.  Select **OK**.

14. Select the **Module Keys** tab to view the keys.

    Secure information for the keys will be stored on the Module Keys tab along with the private key and public key. The **Key lifecycle state** is set to **Active**.


**Parent Topic:**[Setting up S/MIME for email](../concept/smime-for-email-signing-and-encryption.md)

**Related topics**  


[Upload a CA certificate](upload-ca-certificate.md)

[Upload an email certificate](upload-email-certificate.md)

[Enable S/MIME](../concept/enable-smime-for-outbound-and-inbound.md)

