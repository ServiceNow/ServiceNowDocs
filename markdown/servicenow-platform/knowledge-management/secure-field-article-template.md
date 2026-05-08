---
title: Restrict access to fields in an article template
description: Use encryption modules to set field-level security in article templates and display the fields based on role permissions.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure knowledge article templates, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Restrict access to fields in an article template

Use encryption modules to set field-level security in article templates and display the fields based on role permissions.

## Before you begin

Role required: security\_admin

**Note:** Use Knowledge blocks to restrict the content within the same field. For more information, see [Knowledge blocks](../concept/knowledge-blocks.md).

## Procedure

1.  Create an encryption module for the article template field to be encrypted.

    See Create a cryptographic module for details.

2.  Associate the article template field with the encryption module.

    See Encrypting fields and attachments for details.

    1.  Navigate to **System Security** &gt; **Field Encryption** &gt; **Encryption Field Configurations** and click **New**.

    2.  On the form, fill in the fields.

<table id="table_y2h_dg2_gkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table associated with the article template fields. For example, for the How to article template fields, select **How To \[kb\_template\_how\_to\]**.

</td></tr><tr><td>

Column

</td><td>

Article template field to be encrypted. Only String, Date, Date/Time, and URL fields are supported.-   **String and URL fields**: You can add a new encryption configuration to either a parent table or a child table.
-   **Date and Date/Time fields**: You can create encrypted field configurations to encrypt existing Date and Date/Time fields. You can add a new encryption configuration to a parent table only. You cannot add a new encryption configuration to a child table.

**Note:** Depending on the number of records affected by the Date and Date/Time fields you are encrypting, it may take up to a few minutes to create the encryption configuration. Make sure that you create the encryption configuration for Date and Date/Time fields when transaction volume on the instance is low.

</td></tr><tr><td>

Encryption module

</td><td>

Encryption module you created for the article template field.

</td></tr><tr><td>

Method

</td><td>

-   **Single Encryption Module**: Enables data to be encrypted with a single encryption module only. The field is encrypted with the encryption module defined in the **Encryption module** field. Users that do not have the encryption module cannot view or update field values.
-   **Multiple Encryption Module**: Enables data to be encrypted with more than one encryption module. The field is encrypted by the encryption context of the first user to enter data. If the user has multiple encryption modules, the context defined in the encryption module selector is used. Because the encryption module is set on a per record basis, fields in a list can have different encryption modules. However, within a single record, the field can be encrypted by only one module.

**Note:** Mass encryption is not available when using the **Multiple Encryption module** method.

 After a configuration is created using the single encryption module method, you can update the record to use multiple encryption modules. However, you cannot change a field using multiple encryption modules to use a single encryption module.

</td></tr></tbody>
</table>    3.  Click **Submit**.

3.  Define role permissions for the encrypted field.

    1.  Navigate to **User Administration** &gt; **Roles**.

    2.  In the **Name** column, click the link to the role you want to allow to view this field.

    3.  In the **Encrypted context** field, search for and select the name of the encryption context for the article template field to apply for the selected role.

        **Note:** You may need to configure the Role form to add the **Encrypted context** field.

    4.  Click **Update**.


## Result

Depending on their role permissions defined for the encrypted field, users can view the field on the article template.

**Parent Topic:**[Configure knowledge article templates](../concept/configure-knowledge-article-templates.md)

**Related topics**  


[bundle-psec.field-encryption]

