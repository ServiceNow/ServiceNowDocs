---
title: Submit JSA form
description: Employees can use the Submit JSA form to analyze their job safety at their point of work and create a JSA.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Submit JSA form

Employees can use the Submit JSA form to analyze their job safety at their point of work and create a JSA.

For more information on submitting a JSA, see [Submit a JSA from Employee Center](../task/hs-submit-jsa-emp-center.md).

<table id="table_hxh_43r_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Enter job details

</td></tr><tr><td>

Select job location

</td><td>

Job or task location where this job and the associated risks may arise or exists.

</td></tr><tr><td>

Enter job location manually

</td><td>

Job or task location. If your job location isn’t available in the system, enter it manually.

</td></tr><tr><td>

Enter a name of the JSA

</td><td>

Name of this JSA.

</td></tr><tr><td>

Select job

</td><td>

Job with pre-defined hazards and controls for your job type. If you select a job, all hazards and control measures for your job type are auto-populated from this pre-defined job.Only the active jobs from the Job \[sn\_hs\_rm\_job\] table are available in this list. For more information, see [Define a job in the job register](../task/hs-define-job-register.md).

</td></tr><tr><td>

Job start date and time

</td><td>

Date and time when your job starts.

</td></tr><tr><td>

JSA expiry date and time

</td><td>

Date and time when this JSA for your job expires.

</td></tr><tr><td class="sub-head" colspan="2">

Select hazards and control measures

</td></tr><tr><td>

Do you want to create a multi step job?

</td><td>

Option to indicate if this JSA is for a single-step or a multi-step job.If you selected a job in the **Select job** field, this field is automatically set depending on the type of the job you selected and is read-only.

</td></tr><tr><td>

Add job steps and their hazards and controls

</td><td>

Job steps and their associated hazards and control measures.This field appears only when it's a multi-step job and **Do you want to create a multi step job?** is set as **Yes**.

If you selected a multi-step job in the **Select job** field, all its job steps and their associated hazards and controls are auto-populated in this field.

-   However, you can add or remove job steps as required. To remove a job step that isn't relevant for your job, select the remove icon \(![Remove icon](../image/icon-remove.png)\) in the **Actions column**. To remove all job steps, select **Remove all**.
-   You can also add or remove hazards and controls for each job step. To review them, select the edit icon \(![Edit icon](../../customer-service-management/image/icon-pencil-ac.png)\) in the **Actions column** for the job step.

</td></tr><tr><td>

Add job step

</td><td>

Option to add a job step if it's a multi-step job.

</td></tr><tr><td>

Add hazards and controls

</td><td>

Hazards and the available control measures associated with a job.This field appears only when it's a single-step job and **Do you want to create a multi step job?** is set as **No**.

If you selected a single-step job in the **Select job** field, all hazards and control measures for your job type are auto-populated from this pre-defined job. However, you can add or remove them as required.

-   To remove a hazard and control that isn't relevant for your job, select the remove icon \(![Remove icon](../image/icon-remove.png)\) in the **Actions column**. To remove all of them, select **Remove all**.
-   To review and modify them, select the edit icon \(![Edit icon](../../customer-service-management/image/icon-pencil-ac.png)\) in the **Actions column**.

</td></tr><tr><td>

Add hazards

</td><td>

Potential hazards that may arise or exist for the job or job step. Select all potential hazards for your job type using the **Add job step** or **Add hazards and controls** button.If you selected a job in the **Select job** field, all hazards are auto-populated from this pre-defined job. However, you can add or remove hazards as required.

</td></tr><tr><td>

Add additional hazards

</td><td>

Any other hazards that are identified but not available in the **Add hazards** window. Enter it manually to add.​

</td></tr><tr><td>

Add control measures

</td><td>

Control measures that are available for the selected hazards. Select all controls that are in place in your organization.If you selected a job in the **Select job** field, all control measures are auto-populated from this pre-defined job. However, you can add or remove controls as required.

</td></tr><tr><td>

Add additional control measures

</td><td>

Any other control measures that should be in place and aren’t available in the **Add control measures** window. Enter it manually to add.

</td></tr><tr><td>

Links to useful documents

</td><td>

Documents links related to the job.This field appears only when you selected a job in the **Select job** field and that job has associated document links. The document links from the selected job are auto-populated in this field.

</td></tr><tr><td class="sub-head" colspan="2">

Add additional details

</td></tr><tr><td>

Select employee/workers who have been informed

</td><td>

Employees, contractors, and any other workers who've been informed about the risks and controls related to this job at your workplace.They are typically the people who can be impacted by this JSA and must be aware of it.

Add them with an acknowledgement using the **Add employee/workers** button.

**Note:**

-   The **Contractor** option in the **Person type** field appears only when the Health and Safety Contractor Management \(sn\_hs\_crm\) application is installed on your instance. For more information, see [Additional features in Health and Safety](../../ohs-incident-management/task/install-hs-incident-mgmt.md#table_ix1_bff_gxb).
-   For a contractor, the **Name** field only lists users who have the \[snc\_external\] role assigned to them and have their Health and Safety profile created. For more information, see [Assign Health and Safety profile to a user](../../ohs-incident-management/task/assign-hs-profile-user.md).

</td></tr><tr><td>

Add remarks

</td><td>

Any comments related to your job or this JSA.

</td></tr><tr><td>

Add attachments

</td><td>

Attachments such as image, video, or document related to this job or JSA.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Risk Management reference](../concept/hs-risk-mgmt-reference.md)

