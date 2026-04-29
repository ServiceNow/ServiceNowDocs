---
title: Rotate encryption keys
description: Perform encryption key rotation from the instance. Add a new key, change the default key assignment, and then schedule a mass key rotation or a single key rotation.Schedule a job to find data encrypted using a specified key alias and then re-encrypt the data with the current default encryption key. The data is decrypted before it is re-encrypted with the default key.Schedule a job to find data encrypted with any previous key, and then re-encrypt the data with the current default encryption keys. The data is decrypted before it is re-encrypted with the current default key.Schedule a job to find attachments encrypted using a specified key alias, and then re-encrypt the attachments with the current default encryption key. The attachment is decrypted before it is re-encrypted with the default key.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Rotate encryption keys

Perform encryption key rotation from the instance. Add a new key, change the default key assignment, and then schedule a mass key rotation or a single key rotation.

Before setting an encryption key as the default key, make the key available to each proxy. This ensures that the proxies have the key to encrypt data when the key is assigned as the default key. All proxies must have access to a key before that key can be assigned as the default key.

**Warning:** Before deleting a key from the proxy, set up and run a mass key rotation job to ensure that no data on the instance uses the key. If any information is still encrypted with that key, you cannot decrypt the information after you delete the key.

## Edge filtering and sorting behavior

Whenever you change default keys, be sure to perform a key rotation \(either mass or single key rotation\). Otherwise, you may receive unexpected results when sorting and filtering records. For example, consider the following scenario:

1.  You create encrypted records using one encryption key.
2.  You create a new key and set it as default.
3.  You create a new set of encrypted records using the new encryption key.

If you filter by any encrypted field when connected through the Edge proxy, all records may not be filtered out correctly, or records may appear unexpectedly. The filter works only for records encrypted using the current default key. The records encrypted using the previous default key still appear in the list view.

If you sort by any encrypted field when connected through the Edge proxy, you see two groups of records with the same human readable text in the encrypted field.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

## Schedule a single key rotation job

Schedule a job to find data encrypted using a specified key alias and then re-encrypt the data with the current default encryption key. The data is decrypted before it is re-encrypted with the default key.

### Before you begin

Role required: security\_admin

Before scheduling this job, update the default key in **Edge Encryption Configuration** &gt; **Encryption Key Configuration** &gt; **Set Default Keys**.

### Procedure

1.  Navigate to **Edge Encryption Configuration** &gt; **Maintenance** &gt; **Schedule Single Key Rotation**.

2.  Fill in the fields on the form as appropriate.

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

Select **Single Key Rotation**.

</td></tr><tr><td>

Key

</td><td>

Enter the key to be retired. Verify that this key is no longer the default key in **Edge Encryption Configuration** &gt; **Encryption Key Configuration** &gt; **Set Default Keys**.

</td></tr><tr><td>

Estimate record count

</td><td>

Total estimated number of records to process. Not available when running a single key rotation.

</td></tr><tr><td>

Process Historical Records

</td><td>

Select to process historical records in the Audit table if the field is audited. When encrypting historical records for a field in the Audit table, both new values and old values are encrypted. This field is read only and active.

 To learn more about audited fields, see [Auditing](../../time/concept/c_AuditedTables.md).

</td></tr><tr><td>

Estimate Maximum Audit Record Count

</td><td>

Estimated maximum number of audited records to process. Not available when running a single key rotation.

</td></tr><tr><td>

Active

</td><td>

Clear this check box if you want to deactivate this job.

</td></tr><tr><td>

Run

</td><td>

Select the period between job executions.

</td></tr><tr><td>

Starting

</td><td>

Enter the date and time to run the job for the first time.

</td></tr></tbody>
</table>3.  Click the menu icon in the form header and select **Save**.

    **Estimate Record Count** is not supported when processing audited fields.


## Schedule a mass key rotation job

Schedule a job to find data encrypted with any previous key, and then re-encrypt the data with the current default encryption keys. The data is decrypted before it is re-encrypted with the current default key.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Maintenance** &gt; **Schedule Mass Key Rotation**.

2.  Fill in the fields on the form as appropriate.

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

Select **Mass Key Rotation**.

</td></tr><tr><td>

Estimate record count

</td><td>

Total estimated number of records to process. Not available when running a mass key rotation.

</td></tr><tr><td>

Process Historical Records

</td><td>

Select to process historical records in the Audit table if the field is audited. When encrypting historical records for a field in the Audit table, both new values and old values are encrypted. This field is read only and active.

 To learn more about audited fields, see [Auditing](../../time/concept/c_AuditedTables.md).

</td></tr><tr><td>

Estimate Maximum Audit Record Count

</td><td>

Estimated maximum number of audited records to process. Not available when running a mass key rotation.

</td></tr><tr><td>

Active

</td><td>

Clear this check box to deactivate this job.

</td></tr><tr><td>

Run

</td><td>

Select the period between job executions.

</td></tr><tr><td>

Starting

</td><td>

Enter the date and time to run the job for the first time.

</td></tr></tbody>
</table>3.  Click the menu icon in the form header and select **Save**.

    **Estimate Record Count** is not supported when processing audited fields.


## Schedule an attachment key rotation job

Schedule a job to find attachments encrypted using a specified key alias, and then re-encrypt the attachments with the current default encryption key. The attachment is decrypted before it is re-encrypted with the default key.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Maintenance** &gt; **Schedule Attachment Key Rotation**.

2.  Fill in the fields on the form as appropriate.

    |Field|Value|
    |-----|-----|
    |Name|Enter a descriptive name.|
    |Job Type|Select **Attachment Key Rotation**.|
    |Active|Clear the check mark if you want to deactivate this job.|
    |Table|Select a table.|
    |Run|Select the period between job executions.|
    |Starting|Enter the date and time to run the job for the first time.|

3.  Click the menu icon in the form header and select **Save**.

4.  To see an estimated count of records to be updated, click **Estimated Record Count**.

5.  To run the job immediately, click **Execute Now**.


