---
title: Configure a business role
description: Create or modify a business role based on job function, geography, and so on.
locale: en-US
release: zurich
product: Employee Journey Management
classification: employee-journey-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Business roles, Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure a business role

Create or modify a business role based on job function, geography, and so on.

## Before you begin

Role required: sn\_businessroles.writer 

## About this task

Modeled after the organizational hierarchy for applications access, business roles enable you to provision applications to your employees. Depending on their job function, employees need different applications to perform their work. For example, the applications that a product designer requires differs from that of a software engineer. Each business role is mapped to one or more groups, and you can create default business roles and parent-child hierarchies to provision applications.

## Procedure

1.  Navigate to **All** &gt; **Business Roles** &gt; **Business Roles**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_d3b_cpj_2jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business role.

</td></tr><tr><td>

Parent business role

</td><td>

Other business roles of which this business role is a member. If the business role has a parent, then the child inherits all the applications that are provisioned to the parent.For example, say you have a parent business role called All Employees that provisions applications A and B, and a child business role called Marketing that provisions applications C, D, and E. When a new hire is assigned the Marketing business role, that user is provisioned applications A through E.

</td></tr><tr><td>

Short description

</td><td>

Description of the business role.

</td></tr><tr><td>

Default

</td><td>

Option to set this record as a default business rule. If selected, the business role is automatically assigned to all new hires that meet the audience criteria for that record.For example, a default business role called Active Users can be used to provision basic applications that users across your entire organization require.

</td></tr><tr><td>

Audience

</td><td>

Defines the conditions or criteria that the new hire must meet for the hiring manager to be able to assign the business role on their behalf.For example, you can use audience records so that one business role is only available for on-site workers and another business role is only available for remote workers.

 For details on how to configure an audience record, see [Audiences](../../employee-center/concept/ecpro-audience.md).

</td></tr><tr><td>

Active

</td><td>

Option to activate the business role for use.

</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.

5.  If you are integrating with the Okta service, map the business role to one or more Okta groups.

    1.  In the **Map to Okta groups** related list, click **Edit**.

    2.  From the list of available Okta groups on the left, move the groups that you want mapped to the business role to the list on the right.

        **Important:** If an Okta group is deleted from within the Okta system, that change will not be reflected in your instance. You must manually delete the record by navigating to **Okta Spoke** &gt; **Okta groups**, as well as remove it from any business role mappings.

    3.  Click **Save**.

6.  If you are integrating with the Microsoft Azure AD service, map the business role to one or more groups.

    1.  In the **Group** related list, click **Edit**

    2.  From the list of available groups on the left, move the groups that you want mapped to the business role to the list on the right.

        **Important:** If a group is deleted from within the Microsoft Azure AD system, that change will not be reflected in your instance. You must manually delete the record by navigating to **Directory Sync** &gt; **Groups**, as well as remove it from any business role mappings.

    3.  Click **Save**.

7.  Click **Update**.


**Parent Topic:**[Business roles](../concept/business-roles.md)

