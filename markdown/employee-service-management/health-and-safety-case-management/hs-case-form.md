---
title: Health and Safety case form
description: Safety case manager can use the safety case form to resolve health and safety questions that they receive from employees.
locale: en-US
release: zurich
product: Health and Safety Case Management
classification: health-and-safety-case-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Health and Safety Case Management, Health and Safety, Employee Service Management]
---

# Health and Safety case form

Safety case manager can use the safety case form to resolve health and safety questions that they receive from employees.

When a health and safety question is submitted, it creates a safety case. Some of the fields on the case form are populated from the request from which it is created.

After the case is assigned, a safety agent fills out the fields on the case from Health and Safety Workspace.

<table id="table_iqx_xtw_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the case.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the request.

</td></tr><tr><td>

Requested for

</td><td>

Person for whom the information is requested.

</td></tr><tr><td>

Category

</td><td>

Type of the case or employee's question.-   **Health and safety procedures**: Queries related to the organization’s health and safety procedures.
-   **Training**: Queries related to health and safety training.
-   **Equipment**: Queries related to health and safety equipment.
-   **Injury / Incident related leave**: Queries related to leaves due to injuries or incidents and the related return to work considerations.
-   **General inquiry**: Any other general health and safety queries.

</td></tr><tr><td>

Related incidents / observations

</td><td>

Safety incident or observation this case is related to.This field appears only when the Health and Safety Incident Management \(sn\_hs\_im\_incident\) application is installed on your ServiceNow instance. For more information, see [Install Health and Safety Incident Management](../../ohs-incident-management/task/install-hs-incident-mgmt.md).

</td></tr><tr><td>

Return to work case

</td><td>

Option whether this case is related to an employee returning to work after an injury or illness. Only a user with the Return to work case writer \[sn\_hs\_cm.rtw\_writer\] role can edit this field.A Return to work case is usually opened related to an incident where an employee was injured and required time off to recover.

The following items appear when **Yes** is selected in this field:

-   **Return to work details** section on the case form.
-   **Leaves** and **Injury and illness** tabs for this case.

</td></tr><tr><td>

Compensation claim case

</td><td>

Option whether this case is related to a to compensation claim.The following sections appear when **Yes** is selected in this field. Only a user with the Claim case writer \[sn\_hs\_cm.claim\_case\_writer\] role can edit fields in these sections.

-   Employee claim details
-   Closure details

</td></tr><tr><td>

Parent case

</td><td>

Parent Health and Safety case ID number this case is related to.

</td></tr><tr><td>

State

</td><td>

State of the case.

</td></tr><tr><td>

Assignment group

</td><td>

Safety assignment group the case is assigned to. If the case isn’t assigned to a user yet, any member of this group can work on the case.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to this case.

</td></tr><tr><td>

Contact type

</td><td>

Method to contact the person this information is requested for, such as email or phone number.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the case.

</td></tr></tbody>
</table>## Return to work details

The **Return to work details** section on the Health and Safety case form appears only when **Yes** is selected from **Return to work case**. The fields enable you to assess the employee's capability to work before they return from an injury or illness.

Only a user with the Return to work case writer \[sn\_hs\_cm.rtw\_writer\] role can edit fields in this section.

|Field|Description|
|-----|-----------|
|Leave category|Reason the employee was away from work.|
|Expected return date|Date the employee is expected to return to work.|
|Medical clearance received|Option to indicate whether a medical clearance is received for the employee before they return to work from an injury or illness returning.|
|Accommodations needed|Changes required to help the employee return to work.|
|Work restrictions|Limitations identified during the return to work planning for the employee.|

**Parent Topic:**[Health and Safety Case Management reference](../concept/hs-case-management-reference.md)

