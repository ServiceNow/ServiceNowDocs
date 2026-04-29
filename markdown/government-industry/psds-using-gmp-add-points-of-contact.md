---
title: Add points of contact to a Grant Program
description: As an agent or manager, you can add members of your internal program team to a points of contact list to allow them to be contacted by grant seekers. This list is displayed on the grants program announcement page.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Add points of contact to a Grant Program

As an agent or manager, you can add members of your internal program team to a points of contact list to allow them to be contacted by grant seekers. This list is displayed on the grants program announcement page.

## About this task

Adding a person will create a resource assignment record where the resource \(user\_resource\) field is a reference to a user \(sys\_user\) record. The resource role reference will be added to the points of contact list.

To ensure a user can be added as a point of contact, make sure the user has the **pps\_resource** role and an employee profile \(sn\_employee\_profile\) record. For information on how to create an employee profile, see.

**Note:** Points of contact can only be added from the internal team list record. To add members to the internal team list record, see [Create a grant program using Grants Management program setup for Public Sector Digital Services](psds-gmp-using-set-up-grants-management-program.md).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **CSM Configurable Workspace** &gt; **List**.

2.  Select **Grant Programs** &gt; **My grant programs**.

3.  Navigate to **All** &gt; **User Resource Roles**.

4.  Add a record for the desired user and set the resource role to **Point of contact**.

5.  Verify the user appears in the point of contact resource\_role record, as well as in the proposal playbook activity.


