---
title: Anonymization of encrypted columns
description: When creating data privacy policies, you may include columns that are also protected by Column Level Encryption \(CLE\). How you handle those columns depends on your organization’s compliance requirements.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Data anonymization, Data privacy, Data Privacy, Platform Privacy]
---

# Anonymization of encrypted columns

When creating data privacy policies, you may include columns that are also protected by Column Level Encryption \(CLE\). How you handle those columns depends on your organization’s compliance requirements.

If you consider encryption sufficient protection for the data, you can configure the policy to take no action on those columns. If your requirements demand that the data itself be anonymized—for example, to fulfill a data subject erasure request—the system supports running anonymization directly on encrypted columns.

When anonymization runs on a CLE-encrypted column, the system decrypts the data, applies the anonymization technique, and re-encrypts the result before storing it in the database. This process requires specific prerequisites to be in place and explicit admin consent before a job can run.

## Prerequisites

Before you can run an anonymization job on CLE-encrypted columns, the following must be true:

-   The **Data Privacy Store** application is installed.
-   The **Field Encryption Starter** plugin is active.
-   The glide property `dp.job.enable_map_creation` is set to `true`. Only users with the `sn_kmf.admin` or `sn_kmf.cryptographic_manager` role can modify this property.

If any of these conditions are not met, the system will display an error message identifying the missing item. You will not be able to activate a policy, create a job, or schedule a job until all prerequisites are satisfied. These validations occur at policy creation, job creation, and job scheduling.

**Note:**

Anonymization of encrypted columns is not supported when an active row encryption configuration exists on the same column. If a policy includes a CLE-encrypted column that also has an active encrypted row configuration, the system will block policy activation and job scheduling and display a message identifying the conflict.

## Admin consent

Because anonymizing an encrypted column removes the encryption protection from that data, the system requires explicit in-product consent from a Data Privacy Admin before a job can execute.

When you run a data privacy job that includes encrypted columns, a prompt will appear asking you to click **OK** to acknowledge that the job will conflict with the existing encryption on those columns. The acknowledgement is recorded at the job level and includes a list of which encrypted columns were processed.

If you do not wish to anonymize the encrypted data, you can instead select the **No Action** anonymization technique when creating the policy. This allows the job to run without altering the encrypted columns.

## How anonymization works on encrypted columns

When a job runs on a CLE-encrypted column, the system:

-   Decrypts the data using the cryptographic modules associated with the column.
-   Applies the configured anonymization technique.
-   Re-encrypts the result and stores it in the database.

After anonymization, the data remains visible to users who had access to it before the job ran. Anonymization is supported for columns encrypted using the multi-module method and for hierarchical table configurations.

**Journal fields:**CLE-encrypted journal fields are also supported. After anonymization, journal fields remain encrypted.

**Rollback:**If a job is rolled back, encrypted data remains encrypted. Decrypting the data after rollback will return the original plain-text values.

## Error handling

If decryption or encryption fails for any column during a job, an error is logged. Only one error is logged per table-column combination to avoid duplicate entries.

