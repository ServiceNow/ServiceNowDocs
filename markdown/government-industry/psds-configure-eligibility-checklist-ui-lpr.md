---
title: Configure Eligibility Checklist UI in License and Permit Playbook
description: Configure the eligibility checklist UI as a part of Record Generator in License and Permit Playbook.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Eligibility in License and Permit Playbook, License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure Eligibility Checklist UI in License and Permit Playbook

Configure the eligibility checklist UI as a part of Record Generator in License and Permit Playbook.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the **Checklist Template** table by clicking on the label link.

3.  Select **Show List** under **Related Links**.

4.  Select **New**.

5.  Create a Checklist Template record by filling in the fields.

6.  Select **Submit**.

7.  Right-click on the top menu bar of the new Checklist Template record, and in the context menu, select **Copy sys\_id**.

8.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

9.  Open the `sn_gsm_lic_prmt.GSMLicensePermitConfig` record, and locate the `getEligibilityChecklist` function.

10. Switch to the License and Permit Playbook application to edit the record, if prompted.

11. Add the logic after the `if`function.

    An example logic, placing within the quotes the table name and sys\_id numbers, respectively.

    ```
    } else if(tableName == "[table name]") {
    return "[sys_id]";
    ```

12. Select **Create implementation**.


## Result

The Eligibility Checklist now displays when you create a new License and Permit record in the first License and Permit Playbook activity​. See [Define Eligibility Questions in License and Permit Playbook](psds-define-eligibility-questions-lpr.md) to configure the criteria used to determine eligibility for the License or Permit.

