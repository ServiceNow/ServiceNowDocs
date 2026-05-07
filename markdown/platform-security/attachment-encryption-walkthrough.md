---
title: Attachment encryption walkthrough
description: This walkthrough shows you how to encrypt an attachment in your instance using Field Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Column Level Encryption Enterprise examples, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Attachment encryption walkthrough

This walkthrough shows you how to encrypt an attachment in your instance using Field Encryption Enterprise with the Key Management Framework \(KMF\). It also shows you how to use your own key.

## Before you begin

**Note:** This procedure only applies to Field Encryption Enterprise functionality. See [Activate Field Encryption](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Field Encryption Enterprise.

Role required: sn\_kmf.cryptographic\_manager

## About this task

This walkthrough starts with an instance where you have already created and uploaded your customer-supplied cryptographic key. You could use the key, but this example uses a customer-supplied key.

Upload confidential attachments in your instance and limit access from certain users. Use Encrypted Field Configuration to specify which authorized personnel can access sensitive data.

We show you how to encrypt attachments to only be visible to users who are granted access, or be visible to all users that are not restricted from viewing the data. In this example, we restrict a certain role from being able to access an attachment in the **Incidents** module.

**Note:** Although you can use multiple modules with Field Encryption Enterprise, attachment encryption must use single modules.

## Procedure

1.  Make sure that Field Encryption Enterprise is enabled.

2.  Create a cryptographic module.

    See [Create cryptographic module for Field Encryption](create-PE-cryptographic-module.md) for more information.

3.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience**.

4.  Select **View module details** from the Field Encryption overview to open the module record you want to configure.

5.  Select **Encrypted Fields** and **Configure**.

6.  Complete the form:

<table id="table_rj3_tsn_tnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select the table to access the sensitive information. For this example, select **Incident \[incident\]**.

</td></tr><tr><td>

Type

</td><td>

Select **Attachment** to use your personal key for encrypting an attachment from the selected **Table** For this example, select **Incident**.

</td></tr><tr><td>

Active

</td><td>

Mark **Active** to be able to use the field configuration.**Important:** When active, your instance is actively encrypting new data in the selected fields or attachments. Users won’t have access to this data unless they have permission via an associated Module Access Policy. Don’t select if the field isn’t ready to begin encrypting and enforcing Module Access Policies.

To verify historical data is encrypted after an Encrypted Field Configuration is active, you’ll need to run a Mass Encryption Job on the column. For details, see “Schedule Mass Encryption, Decryption, or Rekeying”.

</td></tr><tr><td>

Encrypt by default

</td><td>

When selected, records that don’t match row conditions will be encrypted using the Field Encryption module selected in the field below.

 When not selected, these records will not be encrypted.

</td></tr><tr><td>

Field Encryption module

</td><td>

The field encryption module used by this encrypted field configuration.

</td></tr><tr><td>

Column

</td><td>

If you have chosen Column in the Type field, select the fields to be encrypted.**Note:** If the field you want to encrypt is not available, it isn’t a supported type. The supported field types are:

-   Date
-   Date/Time
-   URL
-   HTML
-   Journal
-   Translated
-   Email
-   Phone


</td></tr><tr><td>

Algorithm Equality Preserving

</td><td>

When selecting Field Encryption Enterprise, this field is visible based on the table selected. Displays whether Equality Preserving is enabled in the field encryption module selected in the Crypto Module field.

</td></tr><tr><td>

Method

</td><td>

The **Single Module** option is used to apply the policies for one module. **Multiple Modules** is used to apply the policies across multiple modules.

</td></tr></tbody>
</table>7.  Select **Save**.

    Establish a Module Access Policy \(MAP\) to assign access to the cryptographic module. Refer to [Create a module access policy](create-module-access-policy.md) for additional information.

8.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience** &gt; **Configurations** &gt; **Access Policies**.

9.  Click **Create new**.

10. Select the Field Encryption \(FE\) module.

11. Complete the form:

    |Field|Description|
    |-----|-----------|
    |Policy name|Enter a name for the policy, such, as "Attachment policy."|
    |Type|Select **Role** to restrict access to the encrypted field from users with the assigned role.|
    |Result|Select **Strict Reject** to control the access to the attachment from the selected role. \(To grant access for the selected role, select **Track**.\)|
    |Crypto module|Select the crypto module that you created to encrypt your key.|
    |Active|Select this check box to be able to use the Module Access Policy.|
    |Target Role|Select the role that will not have access to the encrypted field. For this example, select **itil**.|
    |Specify purpose|Optional. Enable to display the Crypto Spec field on the form. Enable this option to configure granular operations, such as some users being able to encrypt, but not decrypt.|
    |Application|The Application scope is auto-populated by your current scope.|

    ![Module Access Policy form](../image/attachment-access-policy.png "Module Access Policy form")

12. Click **Submit**.

13. As user with access to the encryption module, navigate to **Incidents** and add an attachment to the form.

    Once the attachment is uploaded, it will be available from the Activities screen.

14. Log in as a user that doesn't have access to the module.

15. Open the incident and scroll to the **Activities:** section.

    The link to open the attachment isn't visible for users that don't have access to the module.


## Result

You have successfully used your customer-supplied key to control access to a specific attachment using Field Encryption Enterprise.

**Parent Topic:**[Column Level Encryption Enterprise examples](../concept/kmf-walkthroughs-tutorials-2.md)

