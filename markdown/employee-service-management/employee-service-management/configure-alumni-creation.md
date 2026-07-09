---
title: Configure alumni creation
description: As an admin, use the various configurable methods to enable seamless employee-to-alumni transition.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Configure alumni creation

As an admin, use the various configurable methods to enable seamless employee-to-alumni transition.

## Before you begin

Role required: sn\_asc.admin

-   Review personal details - Enable offboarding employees to review and update their personal details to promote seamless communication.
-   Automated onboarding – Configuration to create alumni records automatically for employees who meet the specified criteria during the employee offboarding. For example, employees who are not in the active status and who’s employment end date was five days ago.
-   Admin import – Configuration to bulk upload alumni records through data imports.
-   Alumni Self-registration – Configuration to auto-approve or manually approve the alumni profiles created using self-registration on the alumni portal.

## Procedure

1.  Navigate to **All** &gt; **Alumni Service Center** &gt; **Administration** &gt; **Configuration**.

2.  In the Personal Details Review tab, select the **Add Filter Condition** to configure a trigger condition, which creates a task for employees during their offboarding stage.

    This HR task enables employees leaving the organization to verify and update their personal information, which includes personal email, phone number, and shipping address. These details are essential for post-employment communication. Employees can verify their details in two ways:

    -   Verify Personal Details activity – offboarding Journey lifecycle event
    -   Verify Personal Details task – In Employee Center To-dos.
3.  In the Automatic creation tab, select the **Add Filter Condition** to configure specific conditions on creating the alumni record automatically.

    1.  In the Default state field, select Approve or Approval needed.

        The alumni records are automatically created in the staging table. Selecting Approved creates an alumni staging record with Approved status, and selecting Approval needed creates an alumni staging record that require manual approval.

        **Note:** A scheduled job \(Import Approved Staged to Alumni\) generates alumni records for the staging entries in the Approved status.

4.  In the Admin import tab, select the relevant properties to configure the alumni record status when the data is imported via an Excel sheet.

<table id="table_ej2_5hg_tmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default state \(sn\_asc.import.default.state\)

</td><td>

The default status for the staged alumni records when created by an import set and default transform map.The default state is Approved.

</td></tr><tr><td>

Alumni suffix \(sn\_asc.import.alumni.suffix\)

</td><td>

Suffix added to the end of the user names for alumni records. Having a suffix distinguishes between your current work force and alumni.**Note:** The default suffix provided is .alum. You can also customize the suffix to match your requirements.

</td></tr><tr><td>

Username max tries \(sn\_asc.import.user\_name.max.tries\)

</td><td>

The number of times the application attempts to add a digit to an alumni user ID to create a unique ID.For example, when you have multiple people with the same name, the system adds a unique number at the end of each user name. This property determines how many times the system adds a unique number to similar user IDs.

**Note:** The default value is 50. If zero \(0\) is entered, only the suffix is used to distinguish between users with the same name.

</td></tr></tbody>
</table>5.  In the Self-registration tab, select the default approval status to create alumni users without manual intervention when users self-register on the alumni portal.

    -   Default state - Use this status when the self-registered user details don’t match with the details in the HR profile. Selecting Approved creates an alumni staging record in Approved status.
    -   Default state\(Alumni verified\) - Use this status when the self-registered user details match with the details in the HR profile. Selecting Approved creates an alumni staging record with Approved status.
    -   Default fields to match on - Use the configurable JSON script where you can add fields in the 'must' \(all the fields must be matched\) and 'any' \(any one of the fields must be matched\) categories to map the alumni user internally.

        For example,

        ```
        
        {
          "must": [
            {
              "sourceField": "first_name",
              "targetTable": "sys_user",
              "targetField": "first_name"
            },
            {
              "sourceField": "last_name",
              "targetTable": "sys_user",
              "targetField": "last_name"
            }
          ],
          "any": [
            {
              "sourceField": "u_employee_number",
              "targetTable": "sys_user",
              "targetField": "employee_number"
            },
            {
              "sourceField": "email",
              "targetTable": "sn_hr_core_profile",
              "targetField": "personal_email"
            }
          ]
        }
        
        ```

    **Note:** A scheduled job \(Import Approved Staged to Alumni\) automatically generates alumni records for these approved entries.

6.  Select **Update**.


