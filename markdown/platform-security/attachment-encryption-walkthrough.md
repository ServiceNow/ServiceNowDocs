---
title: Attachment encryption walkthrough
description: This walkthrough shows you how to encrypt an attachment in your instance using Column Level Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Column Level Encryption examples, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Attachment encryption walkthrough

This walkthrough shows you how to encrypt an attachment in your instance using Column Level Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.

## Before you begin

**Note:** This procedure only applies to Column Level Encryption Enterprise functionality. See [Activate Field Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Column Level Encryption Enterprise.

Role required: kmf cryptographic manager

## About this task

This walkthrough starts with an instance where you have already created and uploaded your customer-supplied cryptographic key. You could use the key, but this example uses a customer-supplied key.

Upload confidential attachments in your instance and limit access from certain users. Use Encrypted Field Configuration to specify which authorized personnel can access sensitive data.

We show you how to encrypt attachments to only be visible to users who are granted access, or be visible to all users that are not restricted from viewing the data. In this example, we restrict a certain role from being able to access an attachment in the **Incidents** module.

**Note:** Although you can use multiple modules with Column Level Encryption Enterprise, attachment encryption must use single modules.

## Procedure

1.  Make sure that Column Level Encryption Enterprise is enabled.

2.  Create a cryptographic module.

    See [Create cryptographic module for Field Encryption](create-PE-cryptographic-module.md) for more information.

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

    Establish a Module Access Policy to assign access to the cryptographic module. Refer to [Create a module access policy](create-module-access-policy.md) for additional information.

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


**Parent Topic:**[Column Level Encryption examples](../concept/kmf-walkthrough-tutorials-2.md)

