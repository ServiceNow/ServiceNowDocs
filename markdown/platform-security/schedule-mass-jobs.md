---
title: Schedule mass encryption, decryption, and rekeying jobs
description: Schedule encryption, decryption, and rekeying jobs to run at a time that is best for your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Encrypting fields and attachments, Using Field Encryption, Field Encryption, Encryption]
---

# Schedule mass encryption, decryption, and rekeying jobs

Schedule encryption, decryption, and rekeying jobs to run at a time that is best for your instance.

## Before you begin

Encryption, decryption, and rekeying jobs can be time and resource intensive, so consider scheduling at non-peak hours. Also ensure that the user scheduling the job has the appropriate access for each job.

Role required: sn\_kmf.cryptographic\_manager

## About this task

Mass encryption and decryption is also available from the Encrypted Field Configurations form. See [Run mass encryption or decryption](mass-enc-dec.md) for instructions.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Security Jobs**.

2.  Click **New**.

3.  Complete the scheduling form.

<table id="table_cg5_rjh_5jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the encryption, decryption, or re-keying job.

</td></tr><tr><td>

Type

</td><td>

Job type:-   **Key Migration Context to Module:** Mass migration of Encryption Context keys to Encryption Modules, including creation of Module Access Policies records for access controls on the Encryption Modules
-   **Data Migration Context to Module**: Migrates data encrypted by Encryption Contexts to Encryption Modules
-   **Mass Decryption Attachment**:Decrypts all encrypted attachments in records for a single table you define in the **Table** field.
-   **Mass Encryption Attachment**: Encrypts all attachments in records for a single table you define in the **Table** field.
-   **Mass Encryption**: Encrypts any pre-existing value in the defined column/field used in the Field Encryption Configuration
-   **Mass Decryption Module**: Decrypts any pre-existing value in the defined column/field used in the Field Encryption Configuration with Single Module.
-   **Mass Decryption Multi Module**: Decrypts any pre-existing value in the defined column/field used in the Field Encryption Configuration with Multiple Module.
-   **Mass Rekeying**: Re-encrypts any pre-existing value in the defined column/field used in the Field Encryption Configuration using the current active key for the module.
-   **Migrate Attachment Context to Module**: Encrypts any pre-existing attachment on the table defined in the Field Encryption Configuration. Any attachment previously encrypted with a context is re-encrypted with the module.


</td></tr><tr><td>

State

</td><td>

The initial job state is New. After the job has been executed as scheduled, the state will update accordingly.

</td></tr><tr><td>

Time window start

</td><td>

Start time for the job in 24-hour format.

</td></tr><tr><td>

Time window end

</td><td>

End time for the job in 24-hour format.

</td></tr><tr><td>

Table

</td><td>

Table to be encrypted or decrypted.

</td></tr><tr><td>

Field

</td><td>

Field to be encrypted or decrypted.

</td></tr><tr><td>

Summary

</td><td>

Job status information when the job is running, has completed, or has errors.

</td></tr></tbody>
</table>    **Note:** Because of system overhead, you should schedule mass encryption, decryption, and rekeying jobs to run at non-peak hours. The ServiceNow AI Platform runs the job between the **Time window start** and **Time window end**. If the job is not complete in one processing window, it continues during the next specified processing window until all processing is complete.

4.  Click **Submit**.

5.  After you schedule a job, you can do the following.

    -   Click **Cancel Job** to cancel a running job.
    -   Click **Start** to start a job immediately.
    -   Click **Update** to save any changes you make to the job schedule.
    -   Click **Delete** to delete the scheduled job.

**Parent Topic:**[Encrypting fields and attachments](../concept/field-encryption-key-management.md)

