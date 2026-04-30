---
title: Run secrets management security jobs
description: Schedule a secrets management job to perform encryption tasks on secrets fields on your instance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Secrets management dashboard, Secrets Management, Platform Security]
---

# Run secrets management security jobs

Schedule a secrets management job to perform encryption tasks on secrets fields on your instance.

## Before you begin

Role required: sn\_kmf.admin, security\_admin, and sn\_secrets.admin

To perform these steps, you must elevate to the security\_admin role. For details on this process see, [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md)

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Security Jobs** &gt; **Create New**.

2.  At the **What type of Security Job would you like to create?** prompt, select **Secrets Management Job**.

3.  On the form, fill in the fields.

<table id="table_u5r_zjn_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the security job

</td></tr><tr><td>

State

</td><td>

The initial job state is New. After the job has been executed as scheduled, the state will update accordingly

</td></tr><tr><td>

Time window start

</td><td>

Start time for the job in 24-hour format. The job begins execution at the chosen time.

</td></tr><tr><td>

Time window end

</td><td>

End time for the job in 24-hour format. If the job isn’t finished by this time, it continues during the next specified processing window until the job is complete.

</td></tr><tr><td>

Enforcement Level

</td><td>

Whether the job affects all tables, or a selection of specific tables or fields. Select from-   All Tables
-   Specific Tables
-   Specific Fields
-   Specific Packages
 **Warning:** Selecting the **All Tables** option may affect instance performance. Consider scheduling at non-peak hours.

</td></tr><tr><td>

Packages

</td><td>

The packages to include in this job. Encryption is applied to selected packages. This option displays only when the **Enforcement Level** field is set to **Specific Packages**

</td></tr><tr><td>

Tables

</td><td>

The tables to include in this job. Encryption is applied to all applicable fields within the selected tables. This option displays only when **Enforcement Level** is set to **Specific Tables**

</td></tr><tr><td>

Fields

</td><td>

The tables to include in this job. Encryption is applied to all selected fields. This option displays only when **Enforcement Level** is set to **Specific Fields**

</td></tr><tr><td>

Job Mode

</td><td>

Select from-   **Password2 to Secrets Management**

Encrypt all password2 fields within your secrets groups using the cryptographic modules defined each group's module access policy.

-   **Secrets Management to Password2**

Re-Encrypt data in your secrets groups using password2 encryption. For details on this encryption type see [Password2 encryption with KMF](../../key-management-framework/concept/password-2way-encrypted-fields.md).

-   **Secret Group Enforcement**

Queries all data that should match the group selected in the **Secret Group** field. If all the data found by the query is already in the group, the job makes no changes. If the query finds data that is not yet in the group, the job re-encrypts this data within the Secret Group.

**Note:** If the data found in this query is already encrypted and your instances can't decrypt that data, it isn’t encrypted and added to the secrets group.

</td></tr><tr><td>

Secret Group

</td><td>

Secret group containing the secrets to encrypt. This field is only available when **Secret Group** is selected in the **Job Mode** field.

</td></tr><tr><td>

Force rekeying data

</td><td>

 

</td></tr><tr><td>

Summary

</td><td>

Displays information about the job progress. Summary also displays records that couldn’t be encrypted by the job.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

The job queries all data that should match the selected secret group. If all the data found by the query is already in the group, the job makes no changes. If the query finds data that is not yet in the group, the job re-encrypts this data within the Secret Group. \(If the instance can decrypt it, which may not be the case for client side-encrypted secrets\).

**Parent Topic:**[Secrets management dashboard](../concept/secrets-dashboard.md)

