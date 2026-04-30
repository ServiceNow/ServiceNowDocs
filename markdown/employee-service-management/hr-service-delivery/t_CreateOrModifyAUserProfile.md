---
title: Add or modify an HR profile
description: Employees can directly edit some information in their HR profile, such as emergency contact information, but they are restricted from editing certain fields. If employees want to change information that they are restricted from editing, they must submit a general request to HR for the changes.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [HR Profile, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add or modify an HR profile

Employees can directly edit some information in their HR profile, such as emergency contact information, but they are restricted from editing certain fields. If employees want to change information that they are restricted from editing, they must submit a general request to HR for the changes.

## Before you begin

Role required: sn\_hr\_core.secure\_info\_writer, sn\_hr\_core.basic, or sn\_hr\_core.manager

## About this task

The HR Administrator \[sn\_hr\_core.admin\] can configure which HR profile fields an employee can update. An update to information that the employee cannot change requires an HR employee information change request.

**Note:** Use the configurable allow list to add fields that users can modify themselves. This allow list is a system property and accessed by going to **All** &gt; **HR Administration** &gt; **Properties**. The list of user editable fields appears as comma separated list. The property name is **sn\_hr\_core.hr\_profile\_editable\_fields**.

To update the HR profile when an employee information change request is assigned to you, complete the following steps.

## Procedure

1.  Navigate to **All** &gt; **HR Profile** &gt; **HR Profiles**.

    The HR Profiles list opens.

2.  Find the existing HR profile to update by selecting **User** from the HR Profiles list search menu, typing the name, and pressing Enter.

    Also, you can click a profile number to open a user profile.

    From **HR Profiles**, select **New** and type the user name in the **User** field on the HR Profile New record form to create the profile. You cannot change the user name after an HR profile is saved.

3.  Click the profile number to open the user profile.

    The profile opens displaying populated name, manager, department, location, and contact fields from the user record.

4.  Complete or update the form with as much additional information as you have.

<table id="table_tpp_ttf_qw"><thead><tr><th>

Section or related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The auto-assigned profile ID number, which cannot be changed.

</td></tr><tr><td>

User

</td><td>

The user associated with the profile. Click the **Lookup using list** icon and **New** to create a user.

</td></tr><tr><td>

Prefix

</td><td>

Click and select the personal title of the user.

</td></tr><tr><td>

First name

</td><td>

First name of the user, pulled from the user record.

</td></tr><tr><td>

Middle name

</td><td>

Middle name of the user, pulled from the user record.

</td></tr><tr><td>

Last name

</td><td>

Last name of the user, pulled from the user record.

</td></tr><tr><td>

Gender

</td><td>

Select the gender of the user.

</td></tr><tr><td>

Active

</td><td>

Check to indicate that the user is a current employee for your company.

</td></tr><tr><td>

Legal hold

</td><td>

Indicates that the HR profile is under legal hold and all associated employee documents cannot be deleted.-   Click the **Add Legal Hold** button in the form header.
-   Select a **Reason**.
-   Enter comments.
-   Click OK.
 To remove an HR profile from legal hold, click the **Remove Legal Hold** button in the form header.

</td></tr><tr><td>

Date of birth

</td><td>

Click the **Select Date** icon and select the birth date of the user.

</td></tr><tr><td>

Place of birth

</td><td>

Enter the location the user was born.

</td></tr><tr><td>

Country of birth

</td><td>

Select the country the user was born.

</td></tr><tr><td>

Marital status

</td><td>

Select the marital status of the user.

</td></tr><tr><td>

Nationality

</td><td>

Enter the nationality or nation in which the user is a citizen.

</td></tr><tr><td>

Ethnicity

</td><td>

Enter the ethnic group the user identifies with.

</td></tr><tr><td>

Ready to return to workplace

</td><td>

Identifies if the employee is ready to return to work. Works with Enterprise Employee Experience Packs for employees working from home during a health crisis.Select **Yes** and the employee is included in campaigns and lifecycle events related to returning to work.

 Select **I'm not sure** and the employee is included in some of the lifecycle events related to returning to work. An HR task triggers for HR to review the employee's concerns.

 For more information, see [Enterprise Employee Experience Pack](../../return-to-workplace/concept/return-workplace-employee-exp-pack.md).

</td></tr><tr><td>

Return to workplace date

</td><td>

Works with the **Ready to return to workplace** field. Select a date when the employee plans to return to work.

</td></tr><tr><td>

Employment Information

</td><td>

Information such as employment status and type of employment, employee number, and start and end dates.

</td></tr><tr><td>

Employment start date

</td><td>

For onboarding employees, click the **Select Date** icon and select the first day of employment.

</td></tr><tr><td>

Employment end date

</td><td>

For offboarding employees, click the **Select Date** icon and select the last day of employment.

</td></tr><tr><td>

Employment type

</td><td>

Select the employment type for the user.

</td></tr><tr><td>

Probation period

</td><td>

Enter the period the user is on probation.

</td></tr><tr><td>

Probation end date

</td><td>

Enter the date probation ends for the user.

</td></tr><tr><td>

Leave status

</td><td>

The status of the employee if leave was requested. Values are:-   Requested
-   Approved
-   On Leave
-   Rejected
-   Completed
-   Cancelled


</td></tr><tr><td>

Position

</td><td>

Click and select the job title for the user.

</td></tr><tr><td>

Department

</td><td>

Select the department the user belongs to.

</td></tr><tr><td>

Manager

</td><td>

Select the manager the user reports to.

</td></tr><tr><td>

Location

</td><td>

Select the office location of the user.

</td></tr><tr><td>

Location type

</td><td>

Select the location type of the user to further define the location.

</td></tr><tr><td>

Offboard type

</td><td>

For employees offboarding, click, and select the type of employment termination.

</td></tr><tr><td>

Notice period

</td><td>

For companies that require notice before dismissing an employee. Enter the time period between receipt of the letter of dismissal and the end of the last working day.

</td></tr><tr><td>

Employee number

</td><td>

Enter the employee number of the user.

</td></tr><tr><td>

Social Security number

</td><td>

Enter the social security number of the user.**Note:** This field is not encrypted for security. For security purposes, it is recommended to use the **National tax ID \(encrypted\)**, **National tax ID type**, and National tax ID country fields. For more information, see [HR profile encrypted tax identification fields](../concept/hr-profile-encrypted-fields.md).

</td></tr><tr><td>

National tax ID \(encrypted\)

</td><td>

The national tax identification number of the employee.**Note:** This field uses the Password2 \(2-way encrypted\) Key Management Framework \(KMF\) encryption.

</td></tr><tr><td>

National tax ID type

</td><td>

The type of national tax identification associated with your employee. The different types are:-   ITIN: Individual Taxpayer Identification Number
-   SSN: Social Security Number
-   TIN: Taxpayer Identification Number


</td></tr><tr><td>

National tax ID country

</td><td>

The country associated with the national tax identification number of the employee.You can enter the country name or select the Suggestion icon \(![Suggestion icon](../image/suggestion-icon.png)\) to view a list of countries.

</td></tr><tr><td>

Contact Information

</td><td>

Information such as address, phone number, personal email address. Some field values are copied from the onboarding form.

</td></tr><tr><td colspan="2">

The following related links are available:

</td></tr><tr><td>

Create new case

</td><td>

Click to create an HR case for the HR profile displayed.

</td></tr><tr><td>

Show employee org chart

</td><td>

Click to view the organization chart of the employee.

</td></tr><tr><td>

View Manager Profile

</td><td>

Click to view the HR profile of the manager of the employee.

</td></tr><tr><td class="sub-head" colspan="2">

The following related lists are automatically populated.

</td></tr><tr><td>

Beneficiaries

</td><td>

A list of beneficiaries associated with the employee. Click **New** to create a beneficiary.

</td></tr><tr><td>

Who is covered

</td><td>

A list of people who are covered under the benefits for the employee.

</td></tr><tr><td>

Emergency Contacts

</td><td>

A list of the employee emergency contacts. One contact in the list is designated as the primary and others can be entered as alternates.

</td></tr><tr><td>

Employee Documents

</td><td>

Lists all HR employee documents associated with the HR profile.**Note:** This tab only appears when the **Employee access** field is checked from the **Document Type** form.

</td></tr><tr><td>

Direct Reports

</td><td>

List of the employees who report directly to the user.

</td></tr><tr><td>

Colleagues

</td><td>

List of other employees who have the same manager as the user.

</td></tr><tr><td>

Cases

</td><td>

Open HR cases for the user.

</td></tr><tr><td>

Legal Holds

</td><td>

Lists legal or litigation holds on any employee-related documentation.Click **Add Legal Hold** or **New** to place documents associated with the employee on legal hold.

</td></tr><tr><td>

Employee Union Memberships

</td><td>

Lists the labor union information associated with the employee. Select **New** to add labor union information for the employee. For more information, see [Create employee union memberships](labor-union-employee-membership.md).

</td></tr></tbody>
</table>5.  Click **Submit** and return to the **HR Profiles** list page or **Save** and remain on the **HR Profile** form.

    **Note:** Some HR profile information, such as department, is synchronized between the User \[sys\_user\] and HR Profile \[hr\_profile\] records. Updating information in one record automatically applies the updates in the other record.


**Parent Topic:**[HR Profile](../concept/c_HRProfileRecords.md)

