---
title: Create vaccination programs
description: Create vaccination programs to track and manage vaccinations.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create vaccination programs

Create vaccination programs to track and manage vaccinations.

## Before you begin

Role required: sn\_vaccine\_sm.manager

## About this task

To manage flu or infectious diseases, such as COVID-19 vaccinations, use the provided Flu vaccination or Covid-19 Vaccination programs. To manage any other vaccinations, create a program.

The flu and Covid-19 Vaccination programs include predefined vaccine methods, but you must add centers and phases to the programs.

## Procedure

1.  Navigate to **All** &gt; **Vaccine Administration** &gt; **Administration** &gt; **Programs** and click **New**.

2.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the vaccination program.

</td></tr><tr><td>

Catalog item

</td><td>

Schedule vaccine appointment

</td></tr><tr><td>

Description

</td><td>

Description of the program.

</td></tr><tr><td>

Active

</td><td>

Option to activate the program for use. This field is automatically set to **Active**.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  In the Centers related list, add the locations where the vaccine will be administered.

    -   To create a new center with a location and a stockroom, click **New**.
    -   To add existing centers to the program, click **Edit**.

        **Note:**

        If necessary, you can also remove the existing centers from the program. When you remove an existing center from the program, no more appointments can be booked for that center. However, there will be no changes to the pre-booked appointments.

    For each location center, you can specify the appointment schedule configuration, as well as configure the scheduling based on available inventory. For details, see:

    -   [Configure advanced appointment scheduling for a center](configure-location-level-weekly-schedule-config.md)
    -   [Configure inventory-based scheduling for a center](configure-scheduling-by-inventory.md)
5.  In the Phases related list, define the phases for when the vaccine will be administered.

    1.  Enter a name for the phase.

        For example, `Phase 1`.

    2.  Select the start and end dates for the phase.

    3.  Add conditions to the eligibility criteria to define who receives the vaccine during this phase.

        For example, Phase 1 could be limited to people in the senior age group.

6.  In the Methods related list, add each version of the vaccine that is available through the vaccination program.

    1.  Click **New**.

    2.  Enter a name for the vaccine method.

    3.  In the **Applicable to** field, add filter conditions to define who can receive the vaccine method.

        For example, the vaccination may only be suitable for specific age groups, or it may only be provided at specific centers.

    4.  Click **Save**.

7.  In the Dosages related list, create a dosage record for each required dose.

    1.  Click **New**.

    2.  On the form, fill in the fields.

<table id="table_kyw_2j2_34b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the dose. For example, `First dose`.

</td></tr><tr><td>

After

</td><td>

The dose that must be administered before this dose. If this dose is the first dose, don't select a value for this field.

</td></tr><tr><td>

Lead time

</td><td>

The minimum number of days that this dose can be administered after receiving the preceding dose. If this dose is the first dose, don't select a value for this field. This field appears only when a value is selected from the **After** field.

</td></tr><tr><td>

Max time

</td><td>

The maximum number of days that this dose can be administered after receiving the preceding dose. If this dose is the first dose, don't select a value for this field. This field appears only when a value is selected from the **After** field.

**Note:** Max time should be greater than lead time.

</td></tr><tr><td>

Order

</td><td>

The order of the dose. For example, `100` for a first dose and `200` for a second dose.

</td></tr><tr><td>

Method

</td><td>

The vaccine method for the dose. This field is automatically set.

</td></tr><tr><td>

Vaccine

</td><td>

The vaccine model for the dose.

</td></tr><tr><td>

Eligibility Criteria

</td><td>

Configure the eligibility criteria that users must meet to be eligible for a specified dose. For example, a dosage may only be suitable for specific age groups.

</td></tr></tbody>
</table>    3.  Click **Submit**.

        **Note:** If you want to create your own record producer or an alternative to "Schedule your vaccination", don’t update the catalog item of the program with the new record producer at this stage. "Schedule your vaccination" is the user-facing record producer which enables users to schedule vaccines in the Patient Portal. The catalog item should always remain "Schedule vaccine appointment" even when you create a non-OOTB program. For more information, see the Schedule and manage your vaccinations section of [Use the Patient Portal to register for a vaccination program](../concept/hcls-vam-user-experience.md).


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

