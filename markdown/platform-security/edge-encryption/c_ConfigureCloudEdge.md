---
title: Encrypt fields using encryption configurations
description: Encrypt fields by creating encryption configurations.Select the fields to be encrypted and identify the encryption type.Select service catalog variables to be encrypted and identify the encryption type.After configuring a field or a table's attachments to be encrypted, you can stop encryption by deactivating the encryption configuration. After deactivating encryption, you can run a Decryption job for fields or an Attachment Decryption job for attachments to remove the encrypted data from the instance.You can schedule a job to find and encrypt any unencrypted data in a specified field, using the default encryption key configured for the field. If you do not create an encryption job after configuring a field for encryption, only new values are encrypted.You can schedule a job to decrypt data in an encrypted field, to store clear data in the instance.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Encrypt fields using encryption configurations

Encrypt fields by creating encryption configurations.

To configure Edge Encryption, you must be connected to the instance through the proxy. Test all changes on a non-production instance before applying them to the production instance.

## Define encryption keys

After setting up one or more proxies and configuring a default encryption key, the instance verifies that the keys are available to all proxies. You can’t make an encryption key the default key unless all proxies have the key. After a default key is defined, you can create encryption configurations.

## Assign fields and attachments to be encrypted

Assigning fields and attachments to be encrypted means assigning an encryption type to the field or attachment. Before marking a field as encrypted, evaluate these issues.

-   Determine what system features might be impacted.
-   Examine all scripts for use of the field.
-   Make any desired adjustments to the field size. After a field has been configured for encryption, the field size can’t be changed.

Marking a field to be encrypted expands the field size to store the encrypted data. The process of expanding the field size can take a long time, depending on the number of records in the table.

## API support

Column Level Encryption updates the `setDisplayValue()` and `setValue()` APIs so they can insert encrypted data for encrypted fields. It also enables `getDisplayValue()` and `getValue()` to return cleartext values.

The following script illustrates these API changes when the Incident short description is encrypted:

```

var gr = new GlideRecord('incident'); //creates a new incident
gr.setValue('short_description','test123'); //sets the value to test123
var sys_ID = gr.insert(); //inserts the record in the Incident table.
gs.info(gr.getValue('short_description')); //displays the unencrypted value

```

When using `getValue()` to get encrypted text, your script no longer returns the ciphertext. Your script returns the plaintext, assuming that the user has access to the cryptographic module. `getValue()` returns the ciphertext if the user doesn’t have access to the cryptographic module.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

## Create a field encryption configuration

Select the fields to be encrypted and identify the encryption type.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Encryption Configurations** &gt; **Create New**.

2.  Complete the form.

<table id="table_nb5_jkf_4r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table that contains the field to be encrypted.

</td></tr><tr><td>

Type

</td><td>

Whether to encrypt a table column or attachments for the table. Select **Column**.

</td></tr><tr><td>

Column

</td><td>

The field to be encrypted. Appears only when the **Type** is **Column**.Only String, Date, Date/Time, Journal, Journal Input, and URL fields are supported.

-   **String and URL fields**: You can add an encryption configuration to either a parent table or a child table.
-   **Date and Date/Time fields**: You can add an encryption configuration to a parent table only. You cannot add a new encryption configuration to a child table.
**Note:** Depending on the number of records affected by the Date and Date/Time fields you are encrypting, it may take up to a few minutes to create the encryption configuration. Make sure that you create the encryption configuration for Date and Date/Time fields when transaction volume on the instance is low.

</td></tr><tr><td>

Encryption type

</td><td>

The encryption type to use.

</td></tr></tbody>
</table>    **Note:** A specific table and field combination can have only one active configuration at a time.

3.  Click **Submit**.


### What to do next

After you add the encryption configuration record, you can create an encryption job to encrypt existing data. If you do not run an encryption job, Edge encrypts the existing data the next time the data changes. For details, see [Schedule an encryption job](c_ConfigureCloudEdge.md#).

## Create a variable encryption configuration

Select service catalog variables to be encrypted and identify the encryption type.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Variable Encryption Configuration**.

2.  In the **Edge Encryption Variable Configurations** list, click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Variable|The variable to be encrypted.|
    |Encryption type|The encryption type to use.|

4.  Click **Submit**.


### What to do next

After you add the encryption configuration record, you can create an encryption job to encrypt existing data. If you do not run an encryption job, Edge encrypts the existing data the next time the data changes. For details, see [Schedule an encryption job](c_ConfigureCloudEdge.md#).

## Deactivate an encryption configuration

After configuring a field or a table's attachments to be encrypted, you can stop encryption by deactivating the encryption configuration. After deactivating encryption, you can run a Decryption job for fields or an Attachment Decryption job for attachments to remove the encrypted data from the instance.

### Before you begin

Role required: security\_admin

### About this task

**Warning:** Deactivating an encryption configuration does not delete the encryption record and the encryption type cannot be changed.

### Procedure

1.  Navigate to **Edge Encryption Configuration** &gt; **Edge Encryption Configurations** &gt; **All**.

    The **Edge Encryption Configurations** list is shown.

2.  Click on the encryption configuration to be deactivated.

    The **Edge Encryption Configuration** form is shown.

3.  Click on the **Active** box.

    The **Active** box is clear.

4.  Click **Update**.

    The **Edge Encryption Configurations** list is shown.


### What to do next

You can run a Decryption or Attachment Decryption job to decrypt data on the instance. If you do not run a job, the encrypted data is decrypted the next time it is changed.

## Schedule an encryption job

You can schedule a job to find and encrypt any unencrypted data in a specified field, using the default encryption key configured for the field. If you do not create an encryption job after configuring a field for encryption, only new values are encrypted.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **Edge Encryption Configuration** &gt; **Encryption Configurations** &gt; **All** to create a job for a field or **Edge Encryption Configuration** &gt; **Variable Encryption Configuration** to create a job for a variable.

2.  Click the field that you want to schedule an encryption job for.

3.  Under **Related Links**, click **Schedule Mass Encryption Job**.

    The **Scheduled Encryption Job** form is shown with all fields populated. The bottom of the form shows records for any previous job executions.

4.  Fill in the fields on the form, as appropriate.

<table id="table_xss_4g2_zs"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name.

</td></tr><tr><td>

Active

</td><td>

Clear this check box if you want to deactivate this job.

</td></tr><tr><td>

Job Type

</td><td>

Select **Encryption**.

</td></tr><tr><td>

Table

</td><td>

Select a table.

</td></tr><tr><td>

Column

</td><td>

Select a column.

</td></tr><tr><td>

Estimated record count

</td><td>

Total estimated number of records to process. Populates after selecting **Estimate Record Count**.

</td></tr><tr><td>

Process Historical Records

</td><td>

Select to process historical records in the Audit table if the field is audited. When encrypting historical records for a field in the Audit table, both new values and old values are encrypted. To learn more about audited fields, see [Auditing](../../time/concept/c_AuditedTables.md).

</td></tr><tr><td>

Estimate Maximum Audit Record Count

</td><td>

Estimated maximum number of audited records to process. Populates after selecting **Estimate Record Count**. This field is only visible when **Process Historical Records** is selected. **Note:** The estimate may be larger than the actual number of records processed.

</td></tr><tr><td>

Run

</td><td>

Select the period between job executions.

</td></tr><tr><td>

Starting

</td><td>

Enter the date and time to run the job for the first time.

</td></tr></tbody>
</table>5.  Click the menu icon in the form header and select **Save**.

6.  To see an estimated count of records to be updated, click **Estimate Record Count**.

7.  To run the job immediately, click **Execute Now**.


## Schedule a decryption job

You can schedule a job to decrypt data in an encrypted field, to store clear data in the instance.

### Before you begin

**Note:** You must mark the encryption record for the field as inactive \(clear the **Active** box\) in order to run the decryption job.

Role required: security\_admin

### Procedure

1.  Navigate to **Edge Encryption Configuration** &gt; **Encryption Configurations** &gt; **All** to create a job for a field or **Edge Encryption Configuration** &gt; **Variable Encryption Configuration** to create a job for a variable.

2.  Click the field that you want to decrypt.

3.  Under **Related Links**, click **Schedule Mass Decryption Job**.

    The **Scheduled Encryption Job** form is shown with all fields populated. The bottom of the form shows records for previous job executions.

4.  Fill in the fields on the form, as appropriate.

<table id="table_xss_4g2_zs"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name.

</td></tr><tr><td>

Job Type

</td><td>

Select **Decryption**.

</td></tr><tr><td>

Active

</td><td>

Clear this check box if you want to deactivate this job.

</td></tr><tr><td>

Table

</td><td>

Select a table.

</td></tr><tr><td>

Column

</td><td>

Select a column.

</td></tr><tr><td>

Estimated record count

</td><td>

Total estimated number of records to process. Populates after selecting **Estimate Record Count**.

</td></tr><tr><td>

Process Historical Records

</td><td>

Select to process historical records in the Audit table if the field is audited. When encrypting historical records for a field in the Audit table, both new values and old values are encrypted. To learn more about audited fields, see [Auditing](../../time/concept/c_AuditedTables.md).

</td></tr><tr><td>

Estimate Maximum Audit Record Count

</td><td>

Estimated maximum number of audited records to process. Populates after selecting **Estimate Record Count**. This field is only visible when **Process Historical Records** is selected. **Note:** The estimate may be larger than the actual number of records processed.

</td></tr><tr><td>

Run

</td><td>

Select the period between job executions.

</td></tr><tr><td>

Starting

</td><td>

Enter the date and time to run the job for the first time.

</td></tr></tbody>
</table>5.  Click the menu icon in the form header and select **Save**.

6.  To see an estimated count of records to be updated, click **Estimate Record Count**.

7.  To run the job immediately, click **Execute Now**.


