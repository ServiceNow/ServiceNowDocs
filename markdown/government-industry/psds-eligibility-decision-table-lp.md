---
title: Create a Pre-Eligibility Decision Table in License and Permit Playbook
description: The License and Permit Playbook incorporates the use of pre-eligibility criteria, a series of questions that may be posed to an applicant to determine whether they are eligible to apply for a license/permit. This aims to deflect applications in which the applicant is not eligible to obtain a license/permit.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure decision tables for License and Permit Playbook, License and Permit Playbook, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Create a Pre-Eligibility Decision Table in License and Permit Playbook

The License and Permit Playbook incorporates the use of pre-eligibility criteria, a series of questions that may be posed to an applicant to determine whether they are eligible to apply for a license/permit. This aims to deflect applications in which the applicant is not eligible to obtain a license/permit.

## About this task

The Pre-Eligibility Configuration decision table is used to map pre-eligibility questions to a license/permit type.

## Before you begin

Role required: admin

## About this task

Pre-eligibility criteria is established by performing the following activities:

-   Configuring a new pre-eligibility decision table
-   Update the Public Sector Digital Services Pre-Eligibility Configuration decision table

## Procedure

1.  To configure a new pre-eligibility decision table, Navigate to **All** &gt; **Workflow Studio**.

2.  Select **New**.

3.  Select **Decision Table**.

4.  On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Decision Table|Drivers License Pre-Eligibility|
    |Application|License and Permit Playbook|
    |Accessible from|All Application Scopes|
    |Draft Authoring|Selected|

5.  Select **Build decision table**.

6.  Select **Add an input**.

7.  On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Label|applicant\_over\_age\_18|
    |Type|String|

8.  Repeat steps 6-7 for all pre-eligibility questions that you wish to configure to appear on the first activity of the playbook.

9.  Select **Add condition column**.

    Condition columns are conditions that are compared against the input values to determine the results of a decision table.

10. On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Condition Column Label|applicant\_over\_age\_18|
    |Input|applicant\_over\_age\_18|
    |Default Operator|**is**|

    **Note:**

    By default, the operator is set to **is**, meaning an equal comparison of the values provided by the end user against the inputs configured in step 12 below. Other operators can be used depending on how the eligibility will be determined against the given input.

11. Select **Done**.

12. Select the field below the newly created condition column, and enter the value **Yes** or **No** depending on the expected response for eligibility.

13. Select the ![Plus icon.](../image/psdsplusiconlp.png) icon and select **Add condition column**.

14. Repeat steps 10-13 for all input values that determine an applicant's eligibility.

15. Select the ![Plus icon.](../image/psdsplusiconlp.png) icon and select **Add result column**.

16. On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Result Column Label|Eligibility|
    |Result Type|True/False|

17. Select **Done**.

18. Set the Eligibility result field to be **True** if all conditions are met, and select **OK**.

19. Select **Save**, then select **Publish**.

20. Select **Publish** in the prompt.

    The status of your decision table should now be set to **Active**.

21. To update the Public Sector Digital Services pre-eligibility configuration decision table, navigate to **All** &gt; **Workflow Studio**.

22. Select **Decision tables** &gt; **Public Sector Digital Services Pre-Eligibility Configuration**.

23. Select **Create Draft** to edit the table.

24. Select the ![Plus icon.](../image/psdsplusiconlp.png) icon to add a new decision row.

    This decision row maps the extended License &amp; Permit case table with its corresponding Product Model, as well as the eligibility decision table that was created above.

25. On the form, fill in the fields with the following information:

    |Field|Entry|Description|
    |-----|-----|-----------|
    |Table|**sn\_gsm\_drivers\_license\_case** \(or the name of the License &amp; Permit Table that was extended from the base case\)|The column name \(not the column label\) for the associated pre eligibility question that exists on the license and permit case table or extended table.|
    |Product Model|Drivers License|Product model for the particular license/permit.|
    |Description|Confirm the applicant’s eligibility by answering the questions below.|The description that displays at the top of the pre-eligibility activity in the playbook.|
    |Form Header| |Shows a form header above the eligibility questions. Leave this field empty.|
    |Error Header|Not eligible|Error header in the first playbook activity stating that the applicant is not eligible after clicking “Start Application”.|
    |Error Message|Each license/permit has certain criteria that must be met to apply. Review your answers to ensure accuracy.|Error message in the first playbook activity stating that the applicant is not eligible after clicking “Start Application”.|
    |Help URL|Link to a ServiceNow® Page|Presents a **Learn more** link within the error message if the applicant is found to be ineligible. The value in this field will be a link to a ServiceNow® page.|
    |Eligibility|Drivers License Pre-Eligibility|The eligibility decision table created in the previous section for this particular product model. For example, Drivers License Pre-Eligibility.|

26. Select **Save**, then select **Publish**.

27. Select **Publish** in the prompt.

    The status of your decision table should be set to **Active**.


