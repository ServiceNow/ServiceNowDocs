---
title: Report vaccination status to your organization
description: Provide your organization with information about whether you received a vaccine and the date that you received it.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Report vaccination status to your organization

Provide your organization with information about whether you received a vaccine and the date that you received it.

## Before you begin

Before you can submit your vaccination status, you must respond to the vaccine privacy consent.

**Note:** Vaccine admins can report a user's vaccination status for them, however, the admin must first respond to the vaccine privacy consent.

Role required: sn\_imt\_core.privacy\_consent\_user

## About this task

You can report your vaccination status to meet the requirements of your organization. Along with the fillable form, you may include any attachments that may be necessary, such as a SMART health card, Centers for Disease Control and Prevention \(CDC\) Vaccination Card, or any other form of verification that your organization may require.

**Note:** For automatic vaccine validation, your organization must configure their instances to support the SMART health card or CDC Vaccination Card attachment types.

|Validator Service|Attachment Type|
|-----------------|---------------|
|The CommonTrust Network|SMART health card|
|Azure Form Recognizer service|CDC Vaccination Card|

## Procedure

1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Report vaccination**.

    **Note:** To report your or another user's vaccination status in the Now Mobile app, navigate to **Health** &gt; **Follow These Safety Practices** &gt; **Report Vaccination**.

2.  Determine the user you are submitting vaccination status for.

    -   If you are a Vaccine admin, submit your vaccination status or another user's status by selecting the user you are submitting information for, and complete the Report Vaccination form.
    -   If you are not an admin, complete the Report Vaccination form.
3.  On the form, fill in the fields.

<table id="table_ygw_1sb_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Do you want to add vaccine dose information?

</td><td>

The vaccine dose information that you want to provide.

 -   Selecting **Yes** reveals the fields required to submit vaccine dose or booster information.
-   Selecting **No** confirms that you do not have vaccine doses or boosters to add.
-   Selecting **Prefer not to say** confirms that you do not want to share your vaccine dose or booster information.


</td></tr><tr><td>

Vaccine

</td><td>

The type of vaccine or booster that you received. If you select a vaccine that requires more than one dose, such as **Covid-19 2 dose unknown manufacturer**, or you want to submit multiple different vaccines, you can select how many doses you want to report in the **How many doses do you wish to report?** field.**Note:** The **Vaccine** field appears only when **Yes** is selected as the answer to **Have you been vaccinated?**. Additional **Vaccine** fields appear if you are reporting more than one dose.

</td></tr><tr><td>

How many doses do you wish to report?

</td><td>

The number of doses that you are reporting.

 If you select more than one dose, additional **Vaccine** and **Date administered** fields appear for each dose. For example, you can report multiple doses for the same vaccine, multiple vaccines, or a booster with your vaccine doses.

</td></tr><tr><td>

Date administered

</td><td>

The date that you received your dose. If you are reporting more than one dose, add the date administered for each dose or booster \(**Second date administered**, **Third date administered**, or **Fourth date administered**\).

 The date that you received your first dose.

</td></tr><tr><td>

Attachment type

</td><td>

The type of attachment that you are submitting if it is required by a validator service to automatically review your vaccinations. For example, a SMART health cardor CDC Vaccination Card can be used to automatically validate vaccine responses if enabled by your organization.**Note:** **Attachment type** is not a required field for all attachments. You can submit images or other documentation that might require manual review.

</td></tr></tbody>
</table>4.  Add attachments, such as a SMART health card or an image of supporting documentation, by selecting **Add attachments**.

    For more information on supported formats, see [Document Viewer](https://www.servicenow.com/docs/access?context=Documentviewer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    **Note:** If you are adding an attachment required by a validator service, ensure that you've selected the correct **Attachment type**.

5.  Click **Submit**.

    -   If you are a Vaccine admin, you are returned to an empty Report Vaccination form to submit another vaccination.
    -   If you are a user, you are returned to the health and safety status page.

## What to do next

Your organization might require that you be vaccinated before returning to the site. To check your progress on all site entry requirements, see [View your health and safety status](../../employee-readiness-core/task/view-health-safety-status.md).

**Note:** You are not considered fully vaccinated until 14 days after receiving your vaccination \(single-dose vaccine\) or your final dose \(multi-dose vaccine\).

Depending on your organization's requirements, if your vaccine has a vaccine booster available, you might not be considered fully vaccinated until you report receiving your booster.

**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

