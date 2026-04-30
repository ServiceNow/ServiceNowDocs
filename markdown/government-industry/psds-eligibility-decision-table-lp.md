---
title: Create a Pre-eligibility Decision Table in License and Permit Playbook
description: The License and Permit Playbook incorporates the use of pre-eligibility criteria, a series of questions that may be posed to an applicant to determine whether they are eligible to apply for a license/permit. This aims to deflect applications in which the applicant is not eligible to obtain a license/permit.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 3
breadcrumb: [Configure decision tables for License and Permit Playbook, License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Create a Pre-eligibility Decision Table in License and Permit Playbook

The License and Permit Playbook incorporates the use of pre-eligibility criteria, a series of questions that may be posed to an applicant to determine whether they are eligible to apply for a license/permit. This aims to deflect applications in which the applicant is not eligible to obtain a license/permit.

## Before you begin

Role required: admin

## About this task

Pre-eligibility criteria is established by performing the following activities:

-   Configuring a new pre-eligibility Decision Table.
-   Update the Public Sector Digital Services Pre-eligibility Configuration decision table

## Procedure

1.  To configure a new pre-eligibility Decision Table, Navigate to **All** &gt; **Workflow Studio**.

2.  Select **New**.

3.  Select **Decision Table**.

4.  On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Decision Table|Drivers License Pre-eligibility|
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

8.  Repeat steps 6-7 for all pre-eligibility questions that will appear on the first activity of the playbook.

9.  Select **Add condition column**.

10. On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Condition Column Label|applicant\_over\_age\_18|
    |Input|applicant\_over\_age\_18|
    |Default Operator|is|

11. Select **Done**.

12. Select the field below the newly created condition column, and enter the value **Yes** or **No** depending on the expected response for eligibility.

13. Select the ![Plus icon.](../image/psdsplusiconlp.png) icon and select **Add condition column**.

14. Repeat steps 10-13 for all input values that determine the eligibility.

15. Select the ![Plus icon.](../image/psdsplusiconlp.png) icon and select **Add result column**.

16. On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Result Column Label|Eligibility|
    |Result Type|True/False|

17. Select **Done**.

18. Update the Eligibility result field to be True if all conditions are met, and select **OK**.

19. Select **Save**.

20. Select **Publish**.

21. Select **Publish**.

    The status of your decision table should be set to **Active**.

22. To update the Public Sector Digital Services pre-eligibility configuration decision table, navigate to **All** &gt; **Workflow Studio**.

23. Select **Decision tables**.

24. Select **Public Sector Digital Services Pre-eligibility Configuration**.

25. Select **Create Draft**.

26. Select the ![Plus icon.](../image/psdsplusiconlp.png) icon to add a new decision row.

27. On the form, fill in the fields with the following information:

    |Field|Entry|Description|
    |-----|-----|-----------|
    |Table|**sn\_gsm\_drivers\_license\_case** \(or the name of the extended L&amp;P Table\)|The column name \(not the column label\) for the associated pre eligibility question that exists on the license and permit case table or extended table.|
    |Product Model|Drivers License|Product model for the particular license/permit.|
    |Description|Confirm the applicant’s eligibility by answering the questions below.|The description that displays at the top of the pre-eligibility activity in the playbook.|
    |Form Header| |Shows a form header above the eligibility questions.|
    |Error Header|Not eligible|Error header in the first playbook activity that stating that the applicant is not eligible after clicking “Start Application”.|
    |Error Message|Each license/permit has certain criteria that must be met to apply. Review your answers to ensure accuracy.|Error message in the first playbook activity that stating that the applicant is not eligible after clicking “Start Application”.|
    |Help URL|Link to a ServiceNow® Page|Presents a **Learn more** link within the error message if the applicant is found to be ineligible. The value in this field will be a link to a ServiceNow® page.|
    |Eligibility|Drivers License Pre-Eligibility|The eligibility decision table created in the previous section for this particular product model.|

28. Select Save.

29. Select Publish.

30. Select Publish.

    The status of your decision table should be set to **Active**.


