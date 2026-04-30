---
title: Control ability to view breakdown elements
description: To limit which breakdown elements a subset of users can view on indicators, implement element security. Element security applies to widgets, workspaces, and the Analytics Hub .An elements security list prevents unauthorized access to breakdown elements.If deny list security is specified for a breakdown source, and any of the roles of a user are on an element security list for that breakdown source, that user cannot see the elements which that security list applies to.If allow list security is specified for a breakdown source, and any of the roles of a user are on an element security list for that breakdown source, that user can see the elements which that security list applies to.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Indicator breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Control ability to view breakdown elements

To limit which breakdown elements a subset of users can view on indicators, implement element security. Element security applies to widgets, workspaces, and the Analytics Hub.

## Before you begin

Roles required: pa\_admin or admin

## About this task

There are no visibility options for breakdowns. Instead, access to breakdowns is regulated by ACLs in the breakdown sources.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Breakdown Sources**.

2.  Open the breakdown sources record for the breakdown you want to set access to.

3.  In the **Security type** list, select from the following choices.

    |Security type|Description|
    |-------------|-----------|
    |**Deny list**|Exclude groups and users with the roles you specify. They cannot view the indicator scores for the breakdown elements you specify. Groups and users without these roles can view the scores for the elements.|
    |**Allow list**|Include groups and users with the roles you specify. Only they can view the indicator scores for the breakdown elements you specify. Groups and users without these roles cannot view the scores for the elements.|

4.  Define an Elements Security List record and either:

    -   Select the elements for the list.
    -   Set conditions to define which elements are on the list.
5.  Specify the roles that the elements security list applies to.


**Parent Topic:**[Indicator breakdowns](../concept/c_CreatingBreakdowns.md)

## Define an elements security list

An elements security list prevents unauthorized access to breakdown elements.

### Before you begin

Role required: pa\_admin

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Breakdown Sources**.

2.  Open an existing breakdown source record.

3.  In the **Elements Security List** related list, click **New**.

4.  Fill in the fields, as appropriate.

<table id="choicetable_vmr_xc2_jp"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the elements security list.

</td></tr><tr><td>

Description

</td><td>

A more detailed description of what the elements security list does and its purpose.

</td></tr><tr><td>

Active

</td><td>

Check box for making the elements security list active \(selected\) or inactive \(cleared\).

</td></tr><tr><td>

All roles

</td><td>

Select to indicate that the list applies to all roles. Clear the check box and click the lock icon to specify the roles belonging to this elements security list. You can use the search button to look for specific roles.

</td></tr><tr><td>

Security type

</td><td>

\[Read-Only\] Security type selected for the associated breakdown source.

</td></tr><tr><td>

Dimension

</td><td>

\[Read-Only\] Dimension selected for the associated breakdown source.

</td></tr><tr><td>

Facts table

</td><td>

\[Read-Only\] Facts table selected for the associated breakdown source.

</td></tr><tr><td>

Select elements

</td><td>

Select to specify explicitly the elements that this security list applies to. If this option is cleared, use **Conditions** to determine which elements to include.

</td></tr><tr><td>

All elements

</td><td>

Select for the security list to include all elements. Clear to specify individual elements in this security list. Default: selected

</td></tr><tr><td>

Show blank option

</td><td>

Select to allow a user on a breakdown dashboard to see scores without any breakdown elements specified. Clear to allow a user on a breakdown dashboard to see only scores for the breakdown elements that are visible to their role.This setting affects only widgets that follow breakdown dashboard elements. Users with the admin role can always see unfiltered scores on breakdown dashboards.

</td></tr><tr><td>

Conditions

</td><td>

The conditions for determining which breakdown elements the security list applies to. For example, **\[User.Manager\] \[is \(dynamic\)\] \[Me\]**. Conditions are applied on top of the breakdown source conditions. This field is available only if **Select elements** is not selected.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Role restrictions with deny lists

If deny list security is specified for a breakdown source, and any of the roles of a user are on an element security list for that breakdown source, that user cannot see the elements which that security list applies to.

|User role on element security list?|Visibility of elements|
|-----------------------------------|----------------------|
|None of the roles of the user are in an element security list.|All elements that the security list applies to are visible.|
|Any of the roles of the user are in an element security list.|None of the elements that the security list applies to are visible.|
|User has the admin role.|All elements are visible.|

## Role restrictions with allow lists

If allow list security is specified for a breakdown source, and any of the roles of a user are on an element security list for that breakdown source, that user can see the elements which that security list applies to.

|User role on element security list?|Visibility of elements|
|-----------------------------------|----------------------|
|None of the roles of the user are in a security list.|None of the elements that the security list applies to are visible.|
|Any of the roles of the user are in a security list.|All elements that the security list applies to are visible.|
|User has the admin role.|All elements are visible.|

