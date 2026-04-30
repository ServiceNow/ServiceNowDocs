---
title: Organization chart
description: View your organization chart on both the org chart page and my team widget, search for employees, and more in the Employee Center. Configure what details to display on the org chart card for all employees.Use Org Chart Card Configuration to define what to show in the org chart cards.Create or modify a user display configuration record to define when members of a targeted audience display on the Organization chart page and my team widget in the Employee Center or Employee Center Pro.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
keywords: [Org Chart Configuration]
breadcrumb: [Setup employee communications, Configure, Employee Center, Employee Service Management]
---

# Organization chart

View your organization chart on both the org chart page and my team widget, search for employees, and more in the Employee Center. Configure what details to display on the org chart card for all employees.

**Note:**

You can offer a better org chart experience with the new org chart functionality available in the Employee Center Pro application. The newer org chart provides a more modern UI experience and configuration capabilities than the old org chart available in Content Publishing application. Opt in to the Employee Profile for new org chart enhancements. For more information, see [Organization chart in Employee Center Pro](employee-profile-org-chart.md).

The Organization chart page displays the employees organization chart, the relationships to other employees, and more.

## Configure the Organization chart

You control when users appear on both the Organization chart page and my team widget with the user display configuration records. The user display configuration records define when members of a targeted audience display based on a specified date. For example, you can configure a record so that new hires appear on their start date or several days prior.

**Note:** User display configuration records control when other users can see the new hire in the org chart page and my team widget. However, the new hire can still access the org chart page and my team widget to see their team if they have access to the portal.

You can configure what details to display on the org chart card for all employees.

## Default user display configuration record

A default user display configuration record is included with the Content Publishing application.

**Note:** You can have one or more user display configuration records, and they are evaluated in the order assigned. The default user display configuration record is always evaluated last.

Based on the new or upgrading customer, the default record is set to the following values:

|User type|Date|Table|
|---------|----|-----|
|New customers with Employee Center only|sys\_created\_on|User \[sys\_user\]|
|New customers with HR Service Delivery|employment\_start\_date|HR profile \[sn\_hr\_core\_profile\]|
|Upgrading customers|sys\_created\_on|User \[sys\_user\]|

\(HR Service Delivery only\) User display configuration records control when other users can see the new hire in the org chart page and my team widget. If the record is configured to display based on the HR profile \[sn\_hr\_core\_profile\] table and an associated date field, the new hire must have an HR profile with an associated date value in order to appear. They do not appear based on the creation of their record in the User \[sys\_user\] table.

## Configure the Organization chart card

Use **Org Chart Card Configuration** to define what to show in the org chart cards.

### Before you begin

Role required: sn\_cd.content\_admin, sn\_hr\_sp.admin

Org chart cards show additional information on employees that are useful for identifying and contacting the employee.

**Note:** New hires appear in an org chart when they are onboarded and a sys\_user record is created.

You can configure up to four lines of information on the card of an employee.

**Note:** The defaults are: user.email, work\_phone, work\_mobile, and location.

Information is dot-walked from the HR Profile \[sn\_hr\_core\_profile\] or User \[sys\_user\] tables.

### Procedure

1.  Navigate to **Content Publishing** &gt; **Organization Chart** &gt; **Org Chart Configurations**.

2.  Change the scope to the application you are using.

<table id="choicetable_o2w_fss_bbb"><thead><tr><th align="left" id="d261657e255">

Field

</th><th align="left" id="d261657e258">

Description

</th></tr></thead><tbody><tr><td id="d261657e264">

**Profile table**

</td><td>

The table you want to pull details from.-   HR profile \[sn\_hr\_core\_profile\]

**Note:** Only displays when you have HR Service Delivery licensed and activated.

-   User \[sys\_user\]
 **Note:** Any tables that extend the HR profile or User tables also appear.

</td></tr><tr><td id="d261657e290">

**Show detail**

</td><td>

Check to show the detail information on the org chart card.

</td></tr><tr><td id="d261657e299">

**Detail**

</td><td>

Select the field from the table you selected. Detail pulls the information from the field to show in the org chart card.

</td></tr></tbody>
</table>3.  Select **Submit** or **Update**.


## Configure a user display configuration record

Create or modify a user display configuration record to define when members of a targeted audience display on the Organization chart page and my team widget in the Employee Center or Employee Center Pro.

### Before you begin

Role required: sn\_hr\_sp.esc\_admin or sn\_cd.content\_admin

Each user display record is associated with an audience record and a date for when members of that audience are set to appear. You can have one or more user display records, and they are evaluated in the order assigned. The default user display record is always evaluated last, and only if none of the previous records were a match.

### Procedure

1.  Navigate to **Content Publishing** &gt; **Organization Chart** &gt; **User Display**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_app_yj5_phb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the user display configuration record.

</td></tr><tr><td>

Audience

</td><td>

Audience record to apply to the user display configuration record.**Note:** Audiences define the conditions or criteria that a user must meet for the user display configuration to apply to them. See [Audiences](ecpro-audience.md) for more information.

</td></tr><tr><td>

Table

</td><td>

Table that the user display configuration record is associated with.

</td></tr><tr><td>

Date

</td><td>

Date field that the user display configuration record is associated with.

</td></tr><tr><td>

Date offset type

</td><td>

Offset type to apply to the date field.

</td></tr><tr><td>

Offset in days

</td><td>

Number of days to apply to the offset type.

</td></tr><tr><td>

Order

</td><td>

Order number for when the user display configuration record is evaluated. Lower numbered user display configuration records are evaluated before higher numbered user display configuration records.**Note:**

-   Make sure that the order number is unique for each user display configuration record.
-   The default user display configuration record is always evaluated last, and only if none of the previous user display configuration records were a match.


</td></tr><tr><td>

Active

</td><td>

Option to activate the user display configuration record for use.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


