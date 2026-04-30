---
title: Injury and illness fields
description: Safety managers and agents can use the Injury and illness form to log an injury or illness. A safety compliance manager can access an injury and illness report and mark it as recordable for reporting purposes. They can also use it to generate the injury and illness reports.
locale: en-US
release: yokohama
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Reference, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Injury and illness fields

Safety managers and agents can use the Injury and illness form to log an injury or illness. A safety compliance manager can access an injury and illness report and mark it as recordable for reporting purposes. They can also use it to generate the injury and illness reports.

For more information, see [Log an injury and illness](../task/log-injury-illness.md).

<table id="table_injury_illness"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Person

</td></tr><tr><td>

Person type

</td><td>

Type of the person who's injured or ill.-   **Employee**: An employee of the organization where this injury happened.
-   **Visitor**: A person from outside the organization who came to the site as a visitor.
-   **Public**: A person from public who was present at the site of safety incident or observation.
-   **Contractor**: A contract worker from a contractor company who came to the site to perform required tasks. This option appears only when the Health and Safety Contractor Management \(sn\_hs\_crm\) application is installed on your instance.

</td></tr><tr><td>

Employee

</td><td>

Name of the employee who's injured or ill. This field appears only when **Employee** is selected from **Person type**.

**Tip:** If an incident affected more than one person, you must create an injury and illness report for each.

</td></tr><tr><td>

Visitor

</td><td>

Name of the visitor who's injured or ill.This field appears only when **Visitor** is selected from **Person type**.

**Note:** This field only lists visitors who have Health and Safety profile assigned to them. For more information, see [Add a Health and Safety visitor](../task/hs-add-health-safety-visitor.md).

</td></tr><tr><td>

Name

</td><td>

Name of the public person who's injured or ill.This field appears only when **Public** is selected from **Person type**.

</td></tr><tr><td>

Contractor

</td><td>

Name of the contract worker who's injured or ill. This field appears only when **Contractor** is selected from **Person type**.

**Note:** This field only lists users who have the \[snc\_external\] role assigned to them and have their Health and Safety profile created. For more information, see [Assign Health and Safety profile to a user](../task/assign-hs-profile-user.md).

</td></tr><tr><td>

Redact name

</td><td>

Option to redact the employee's name from the record, if there’s a privacy concern. Redacting protects the privacy of the affected employee.When this option is selected for a recordable injury and illness, the employee's name is redacted from any reports that are generated, such as an OSHA form. Their name is replaced with the **Privacy concern case** on the generated reports.

</td></tr><tr><td>

Sensitive content

</td><td>

Option that indicates that the incident contains sensitive information.Only a user with the Sensitive content user role can view a report marked as sensitive. For more information on roles, see [Components installed with Health and Safety Incident Management](components-installed-with-hs-incident-mgmt.md).

**Note:** When you generate a report \(such as OSHA 300 or 300A\), it contains all incidents, including the ones marked as sensitive, according to the template. However, sensitive information is not disclosed in the report as incident details are not included.

</td></tr><tr><td>

Establishment

</td><td>

Name of the establishment where this injury or illness happened.When a safety compliance manager generates a report, such as an OSHA form, only records with an assigned establishment are included.

</td></tr><tr><td class="sub-head" colspan="2">

Healthcare

</td></tr><tr><td>

Treatment administered offsite

</td><td>

Option to indicate if the treatment for the injury or illness is provided outside the workplace.When this option is selected, all other fields in the **Healthcare** section become available.

</td></tr><tr><td>

Name of physician or other healthcare professional

</td><td>

Name of the physician or healthcare professional providing the treatment.

</td></tr><tr><td>

Facility

</td><td>

Name of the hospital where the treatment is provided.

</td></tr><tr><td>

Facility address

</td><td>

Address of the hospital where the treatment is provided.

</td></tr><tr><td>

Treated in emergency room

</td><td>

Option to indicate that the treatment is provided in an emergency room.

</td></tr><tr><td>

Hospitalized overnight

</td><td>

Option to indicate whether the employee spent the night in the hospital.

</td></tr><tr><td class="sub-head" colspan="2">

Injury and illness details

</td></tr><tr><td colspan="2">

Ensure that this section doesn't contain any personal information that can identify the affected employee.

</td></tr><tr><td>

Number

</td><td>

Auto-generated number for the injury and illness record.

</td></tr><tr><td>

Incident

</td><td>

Safety incident associated with this injury and illness. This field is auto-populated with the safety incident number the injury and illness report is created from.

</td></tr><tr><td>

Classification

</td><td>

Classification for this injury and illness.

</td></tr><tr><td>

OSHA injury type

</td><td>

Type of the injury or illness.This field appears only when the Health and Safety Incident Management OSHA Content Pack \(com.snc.sn\_hs\_im\_osha\) application is installed on your ServiceNow instance.

</td></tr><tr><td>

Date and time employee began work

</td><td>

Time when the employee starting working before this injury or illness.

</td></tr><tr><td>

Date and time of injury or illness

</td><td>

Date and time when this injury or illness happened.

</td></tr><tr><td>

Days away from work

</td><td>

Number of days the injured employee has been away from work.

</td></tr><tr><td>

Days job transfer or restriction

</td><td>

Number of days the injured employee is restricted in performing their tasks or transferred to another lower impact job, for example, until they are ready to return to their original job.

</td></tr><tr><td>

Recordable

</td><td>

Option that indicates that this injury or illness is recordable for any reporting purpose. Only a safety compliance manager can edit this field.Only records marked as recordable are included when you generate a report, such as an OSHA form. For example, see [Pre-requisites for generating OSHA forms](../concept/generating-osha-forms.md#reporting-prereq).

</td></tr><tr><td>

Unsure of time

</td><td>

Option to indicate that the time of this injury or illness isn’t available.

</td></tr><tr><td>

HRSD case record

</td><td>

HR case related to this injury.This field appears only when the following conditions are met:

-   Health and Safety Case Management \(sn\_hs\_cm\) application and the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin are installed on your ServiceNow instance.
-   Safety case manager \[sn\_hs\_cm.case\_manager\] role assigned to you.
-   **Employee** is selected in the **Person type** field.

For more information, see [Create an HR case from an injury or illness](../task/create-hr-case-injury-illness.md).

</td></tr><tr><td>

RTW case record

</td><td>

Return to Work case related to this injury.The injury record is auto-populated in the **Injury and illness** tab of the selected case. For more information, see [Health and Safety case](../../hs-case-management/task/hs-work-health-safety-case.md).

This field appears only when the following conditions are met:

-   Health and Safety Case Management \(sn\_hs\_cm\) application is installed on your ServiceNow instance.
-   Safety case manager \[sn\_hs\_cm.case\_manager\] role assigned to you.
-   **Employee** is selected in the **Person type** field.

However, the field doesn't appear when the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is also installed on the instance. For more information, see [Create a return to work case from an injury or illness](../task/create-rtw-case-injury-illness.md).

</td></tr><tr><td>

Injury type

</td><td>

Type of injury or illness.

</td></tr><tr><td class="sub-head" colspan="2">

What was the injury?

</td></tr><tr><td>

What was the injury?

</td><td>

Section where you can select injured body parts and add their details. This field is available only after you click **Save** in the record.

</td></tr><tr><td>

Front

</td><td>

Visual injury picker where you can add injuries on the front parts of a human body.Select a body part to select **Severity** and **Affected body part**, and add **Description** about the injury or illness.

To add multiple injury types to the same body part, select **Add New Injury** and fill in the fields.

</td></tr><tr><td>

Back

</td><td>

Visual injury picker where you can add injuries on the back parts of a human body.Select a body part to select **Severity** and **Affected body part**, and add **Description** about the injury or illness.

To add multiple injury types to the same body part, select **Add New Injury** and fill in the fields.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Attachments

</td></tr><tr><td>

Attachments

</td><td>

Section where you can add attachments related to this injury and illness.If this injury and illness is marked as recordable, all reports generated for it \(such as the OSHA 301 form\) are available in this area. For more information, see [Generate an OSHA 301 form](../task/generate-osha-301-report.md).

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Incident Management reference](../concept/hs-incident-mgmt-reference.md)

