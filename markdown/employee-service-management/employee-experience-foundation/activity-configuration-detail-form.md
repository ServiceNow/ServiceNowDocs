---
title: Activity Configuration Detail form
description: Use the Activity Configuration Detail form to specify which records you want to retrieve from a table when certain conditions are met for a basic activity configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/activity-configuration-detail-form.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Employee Center reference, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Activity Configuration Detail form

Use the Activity Configuration Detail form to specify which records you want to retrieve from a table when certain conditions are met for a basic activity configuration.

<table id="table_cxh_dwv_nqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity Configuration

</td><td>

Name of the activity configuration.

</td></tr><tr><td>

Target Page

</td><td>

Page that you want to open when you click an activity on the My Active items widget.

</td></tr><tr><td>

Activity card mapping

</td><td>

Section to specify what records you want to retrieve from a table and how that information must be displayed. The choices are: -   **Basic**
-   **Scripted**

</td></tr><tr><td>

Table

</td><td>

Table that you want to retrieve the data from.

</td></tr><tr><td>

Application

</td><td>

Application that you want to create the activity configuration for.

</td></tr><tr><td>

Active

</td><td>

Option to activate the activity configuration for use.

</td></tr><tr><td>

Order

</td><td>

Order in which the activity configuration must appear.

</td></tr><tr><td>

Condition

</td><td>

The conditions in which the activity configuration applies.Specify filter conditions on the selected table. A condition includes a field, an operator, and a value. To add conditions, to the right of the fields, click **AND** or **OR**. Delete conditions by clicking the X icon next to the condition.

</td></tr><tr><td>

Basic Card View

</td><td>

Section that displays the fields corresponding to the table that you selected in the **Table** field. Choose how the My Activity widget displays information in the List View by filling in these fields:-   **Badge**
-   **Badge Color**
-   **Image**
-   **Title**
-   **Description**
-   **Field 1**
-   **Field 2**
-   **Action group**

When you select **Action group**, you can perform actions right from the my active items section itself. For more information on action groups, see [Action framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/action-group-framework.md).

This section appears only when **Basic** is selected from the **Activity card mapping** field.

</td></tr><tr><td>

Advanced Card View

</td><td>

In the Card mapping script section, add a JSON script to retrieve records from a table based on the on-screen example. This section appears only when **Scripted** is selected from the **Activity card mapping** field.

</td></tr></tbody>
</table>**Parent Topic:**[Employee Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/emp-center-reference.md)

**Related topics**  


[Activity Configuration form]()

[Approvals experience reference]()

[Connected Content form]()

[Default Employee Profile Header Configuration record]()

[Employee Center widgets]()

[Employee Profile form]()

[Employee Profile Header Configuration form]()

[Employee Profile portal configuration form]()

[Employee Profile upgrade scenarios]()

[Enhanced Requests Experience forms]()

[External Link form]()

[Featured Content form]()

[Footer form]()

[Footer Menus form]()

[Guided Self-Service reference]()

[Menu Item form]()

[Overview section form]()

[Portal notification configuration form]()

[Portal notification content form]()

[Trigger conditions form]()

[Quick Link form]()

[Tab widget mapping form]()

[Taxonomy form]()

[Topic form]()

[User Criteria form]()

[User Criteria output]()

[Schedule appointment form]()

[Location Consent form]()

[Website configuration form]()

