---
title: Create credentials and test credential encryption
description: Create a credential to authenticate into a third-party system.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Create credentials and test credential encryption

Create a credential to authenticate into a third-party system.

## Before you begin

Role required: admin, KMF\_admin, sn\_secrets.secret\_manager, and sn\_kmf.cryptographic\_manager

**Important:** The logged in user of the MID Server also is required to have the following roles: admin, KMF\_admin, sn\_secrets.secret\_manager, and sn\_kmf.cryptographic\_manager.

## Procedure

1.  Navigate to the **SSH credentials** list by entering `ssh_credentials.list` in the navigation filter.

2.  Select **New** to create an **SSH credential** record.

3.  In the form, fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Name|Enter a name for your credentials record. This name can be any value you want.|
    |Applies to|Select **Specific MID Servers**|
    |MID Servers|Select your MID Server.|
    |User name|Enter the user name.|
    |Password|Enter the password related to the user in the **User name** field.|

4.  Select the lock icon \(![lock button](../../key-management-framework/image/lock-icon.png)\) next to the **Credential alias** field.

5.  Select the reference icon \(![reference button](../images/magnifying_glass.png)\) to open the **Connection &amp; credential aliases** list.

6.  Select **New** to create a **Connection &amp; credential alias** record.

7.  Enter a name in the **Name** field.

8.  Select **Credential** in the **Type** field.

9.  Select **Submit**.

    You’re returned to the **SSH Credentials** record. In the next steps, you test that the credential is encrypted.

10. Select and hold \(or right-click\) the form header and select **Show XML**.

11. Find the `<password>` XML tag within the XML.

12. Copy the sys\_id within this `<password>` tag to your clipboard.

    The sys\_id is a 32 character code representing the symmetric key that is being used to encrypt this credential. The encrypted password that you entered into the SSH Credentials table is to the right of the two sets of boxes on this same line.

    ![XML from the SSH credentials record, with the sys_id highlighted](../images/client-side-5.png)

13. Navigate to the **Module keys** list by entering `sys_kmf_module_key.list` in the navigation filter.

14. Filter the list for records where the **Sys ID** field matches the sys\_id you copied in step 12, and select **Run**.

    ![List filter to match the copied sys_id](../images/client-side-6.png)

    Your search should return a single **Module key** record. This record shows you that you have successfully created, and are using, a symmetric key.

15. Navigate to the **Wrapped module keys** list by entering `sys_kmf_wrapped_module_key.list` in the navigation filter.

16. Filter the list for records where the **Crypto module** field matches the cryptographic module you created in the earlier steps, and select **Run**.

    Your search should return a single **Wrapped module key** record. From this list you can verify the following:

    -   The **Wrapped key material** column shows that the symmetric key within the Crypto Module \(that is being used to encrypt the SSH credential\) is encrypted by the public key that you uploaded to the Identity Group.
    -   The **Wrapped key sys id** field shows that it's the key \(the Crypto Module symmetric key\) that is being encrypted by the **Wrapping key sys id** \(the Public Key uploaded to the Identity Group\).
    If the preceding fields aren't on your list by default, you can add them to the list by selecting the **Personalize list** icon \(![Personalize list button](../images/gear-icon.png)\).

    **Note:** Your instance executes a clean-up job every 10 minutes, which removes orphaned keys and helps prevent unassociated key proliferation after you update your credentials.


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

