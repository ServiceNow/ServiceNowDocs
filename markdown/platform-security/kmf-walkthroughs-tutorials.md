---
title: Column Level Encryption Enterprise examples
description: These examples walk you through the encryption of fields and attachments using customer-supplied keys.This walkthrough shows you how to encrypt a field in your instance using Column Level Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.This walkthrough shows you how to encrypt an attachment in your instance using Column Level Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Column Level Encryption Enterprise examples

These examples walk you through the encryption of fields and attachments using customer-supplied keys.

**Parent Topic:**[Using Column Level Encryption](../../encryption/concept/using-column-level-encryption.md)

## Column Level Encryption Enterprise walkthrough

This walkthrough shows you how to encrypt a field in your instance using Column Level Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.

### Before you begin

**Note:** This procedure only applies to Column Level Encryption Enterprise functionality. See [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Column Level Encryption Enterprise.

Role required: admin or security\_admin

**Note:** security\_admin is a privileged role, for details on using privileged roles, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md)

### About this task

This walkthrough starts with an instance where you have already created and uploaded your personal cryptographic key. You could use the ServiceNow key, but this example uses a customer-supplied key.

After the key has been stored in a cryptographic module, you can start configuring fields in your instance, such as salary or social security numbers that have limited access from certain users. In the Encrypted Field Configuration, specify which authorized personnel can access sensitive data.

This task demonstrates two scenarios. One example encrypts the **Short Description** field in an Incident for users who are not authorized to view the sensitive data.

Attachments can also be encrypted and only visible to users who are granted access, or is visible to all users that are not restricted from viewing the data. See [Attachment encryption walkthrough](kmf-walkthroughs-tutorials.md#) to encrypt an attachment.

### Procedure

1.  Make sure that Column Level Encryption Enterprise is enabled.

2.  Create a cryptographic module for column\_level\_encryption.

    See [Create cryptographic module for Column Level Encryption](../task/create-PE-cryptographic-module.md) [Create a cryptographic module](../task/create-cryptographic-module.md) for more information.

3.  Navigate to **System Security** &gt; **Encrypted Field Configurations**.

4.  Click **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|**Column** is required to use your personal key.|
    |Table|Table that stores the sensitive information. For this example, select **Incident \[incident\]**.|
    |Column|Column, or specific information, that represents the sensitive date to be encrypted. For this example, select **short\_description**.|
    |Active|Option to mark **Active** to use the field configuration.|
    |Algorithm Equality Preserving|The option is automatically selected.|
    |Crypto module|Module that you created to use with the personal key.|
    |Method|The **Single Module** option is used to apply the policies for one module. **Multiple Modules** is used to apply the policies across multiple modules.|

    ![Shows a completed Encrypted Field Configuration.](../image/cleexample.png "Encryption field configuration example")

6.  Click **Submit**.

    Establish a Module Access Policy to assign access to the cryptographic module. See [Create a module access policy](../task/create-module-access-policy.md) for additional information.

7.  Navigate to **Key Management** &gt; **Module Access Policies** &gt; **** &gt; **Create New** &gt; **.**

8.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Policy name|Name for the policy, such, as `short description`.|
    |Crypto module|Crypto module that you created to encrypt your key.|
    |Type|Type of access designation for the crypto policy. Use **Role** to grant access to the encrypted field to only those users that have the assigned role.|
    |Target Role|The role that has access to the encrypted field. For this example, select **Admin**.|
    |Active|Option to activate the Module Access Policy.|
    |Result|The **Track**option enables the access to the field for the selected role. \(To restrict access to that field for the selected role, select **Reject** or**Strict Reject**.\)|

    ![Shows the completed module access policy form.](../image/moduleaccesspolicyexample.png "Module access policy example")

9.  Click **Submit**.

10. As a user with the sn\_kmf.admin role, navigate to **Incident** &gt; **New**.

    ![Shows the visible Short description data.](../image/seeshortdescriptionasadmin.png "Example of encrypted field visible")

    You can now view the Short description field based on the module access policy configuration.

    **Note:** The sn\_kmf.admin role was granted user access to the encrypted field, Short description, by setting the module access policy to **Track**. Notice the lock icon \(![Lock icon.](../image/lock-icon.png)\) under the field name indicating that the field is an encrypted field.

    You can now access the **Incidents** module as an end user to test the encrypted field configuration.

11. Log in as a user to be restricted from viewing the encrypted data in the configured field.

    ![Shows no value in the Short description after encryption.](../image/encryptedfieldleveldata.png "Encrypted field level data")

    When you access the incident number, the data in the Short description will not be visible.


### Result

You have successfully used your symmetric key to control access to a specific field using Column Level Encryption Enterprise.

## Attachment encryption walkthrough

This walkthrough shows you how to encrypt an attachment in your instance using Column Level Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.

### Before you begin

**Note:** This procedure only applies to Column Level Encryption Enterprise functionality. See [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Column Level Encryption Enterprise.

Role required: kmf cryptographic manager

### About this task

This walkthrough starts with an instance where you have already created and uploaded your customer-supplied cryptographic key. You could use the key, but this example uses a customer-supplied key.

Upload confidential attachments in your instance and limit access from certain users. Use Encrypted Field Configuration to specify which authorized personnel can access sensitive data.

We show you how to encrypt attachments to only be visible to users who are granted access, or be visible to all users that are not restricted from viewing the data. In this example, we restrict a certain role from being able to access an attachment in the **Incidents** module.

**Note:** Although you can use multiple modules with Column Level Encryption Enterprise, attachment encryption must use single modules.

### Procedure

1.  Make sure that Column Level Encryption Enterprise is enabled.

2.  Create a cryptographic module.

    See [Create cryptographic module for Column Level Encryption](../task/create-PE-cryptographic-module.md) for more information.

3.  Navigate to **System Security** &gt; **Encrypted Field Configurations**.

4.  Click **New**.

5.  Complete the form:

    |Field|Description|
    |-----|-----------|
    |Type|Select **Attachment** to use your personal key for encrypting an attachment from the selected **Table** For this example, select **Incident**.|
    |Table|Select the table to access the sensitive information. For this example, select **Incident \[incident\]**.|
    |Active|Mark **Active** to be able to use the field configuration.|
    |Algorithm Equality Preserving|When selecting Column Level Encryption Enterprise, this field is visible based on the table selected.|
    |Crypto module|Select the module that you created to use with the personal key.|
    |Method|The **Single Module** option is used to apply the policies for one module. **Multiple Modules** is used to apply the policies across multiple modules.|

    ![Encrypted Field Configuration table](../image/attachment-fields.png "Encrypted Field Configuration table")

6.  Click **Submit**.

    Establish a Module Access Policy to assign access to the cryptographic module. Refer to [Create a module access policy](../task/create-module-access-policy.md) for additional information.

7.  Navigate to **Key Management** &gt; **Module Access Policies** &gt; **All**.

8.  Click **New**.

9.  Complete the form:

    |Field|Description|
    |-----|-----------|
    |Policy name|Enter a name for the policy, such, as "Attachment policy."|
    |Crypto module|Select the crypto module that you created to encrypt your key.|
    |Type|Select **Role** to restrict access to the encrypted field from users with the assigned role.|
    |Target Role|Select the role that will not have access to the encrypted field. For this example, select **itil**.|
    |Active|Select this check box to be able to use the Module Access Policy.|
    |Result|Select **Strict Reject** to control the access to the attachment from the selected role. \(To grant access for the selected role, select **Track**.\)|

    ![Module Access Policy form](../image/attachment-access-policy.png "Module Access Policy form")

10. Click **Submit**.

11. As admin or as a person that created the incident, navigate to **Incidents** and add an attachment to **Activities** on the **Notes** related list.

    ![Attachment available per role](../image/attachment-viewed-in-notes.png "Attachment available per role")

12. Log in as a user that restricted from accessing the encrypted attachment.

13. Open the incident and scroll to the **Activities:** section.

    The link to open the attachment is not accessible for users with the restricted role.

14. You have now successfully used your customer-supplied key to control access to a specific attachment using Column Level Encryption Enterprise.


