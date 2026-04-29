---
title: People Involved form
description: Safety managers and agents can use the People involved form to add or modify an involved person in a safety incident or observation assigned to them.
locale: en-US
release: australia
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# People Involved form

Safety managers and agents can use the People involved form to add or modify an involved person in a safety incident or observation assigned to them.

<table id="table_zhq_h2x_f5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Person type

</td><td>

Type of the person involved in the safety incident or observation. If an incident or observation involves more than one person, you must add a record for each.-   **Employee**: An employee of the organization where the safety incident or observation happened.
-   **Visitor**: A person from outside the organization who came to the site as a visitor.
-   **Public**: A person from public who was present at the site of safety incident or observation.
-   **Contractor**: A contract worker from a contractor company who came to the site to perform required tasks. This option appears only when the Health and Safety Contractor Management \(sn\_hs\_crm\) application is installed on your instance.

</td></tr><tr><td>

Employee

</td><td>

Name of the employee involved. This field appears only when **Employee** is selected from **Person type**.

</td></tr><tr><td>

Visitor

</td><td>

Email id of the visitor involved.This field appears only when **Visitor** is selected from **Person type**.

**Note:** This field only lists visitors who have Health and Safety profile assigned to them. For more information, see [Add a Health and Safety visitor](../task/hs-add-health-safety-visitor.md).

</td></tr><tr><td>

Contractor

</td><td>

Name of the contract worker involved.This field appears only when **Contractor** is selected from **Person type**.

**Note:** This field only lists users who have the \[snc\_external\] role assigned to them and have their Health and Safety profile created. For more information, see [Assign Health and Safety profile to a user](../task/assign-hs-profile-user.md).

</td></tr><tr><td>

Association

</td><td>

Type of involvement of the person.-   **Witness**: A person who was present at the safety incident or observation described.
-   **Injured party**: A person who got injured in the incident. This option appears only for the Employee and Visitor person type.
-   **Safety team**: A person from safety team handling the investigation of the incident.
-   **Collaborator**: A person who's collaborating in any in the investigation of this incident or observation.
-   **Involved**: A person who's involved in any other way with this incident or observation.

</td></tr><tr><td>

Name

</td><td>

Name of the person involved.For a public person, enter the name. This field is available only when the **Public** option is selected from **Person type**.

For a visitor, the name is auto-populated from the visitor profile.

</td></tr><tr><td>

Phone

</td><td>

Phone number of the involved person.For a public person, enter the phone number. This field is available only when the **Public** option is selected.

For an employee or visitor, the phone number is auto-populated from the user or visitor profile.

</td></tr><tr><td>

Email

</td><td>

Email ID of the involved person.For a public person, enter the email ID. This field is available only when the **Public** option is selected.

For an employee or visitor, the email ID is auto-populated from the user or visitor profile.

</td></tr><tr><td>

Preferred contact method

</td><td>

Method to contact the involved person such as email or phone number.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Incident Management reference](../concept/hs-incident-mgmt-reference.md)

