---
title: Set up the grants program announcement details
description: Build the program announcement. Define the required forms, terms and conditions, required budget categories, and external-facing point of contact. Provides you with an opportunity to review the grant details.Add members of your internal program team to a points of contact list to allow them to be contacted by grant seekers. This list is displayed on the grants program announcement page.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-11"
reading_time_minutes: 2
breadcrumb: [Grants Management Program Setup, Grants Management, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Set up the grants program announcement details

Build the program announcement. Define the required forms, terms and conditions, required budget categories, and external-facing point of contact. Provides you with an opportunity to review the grant details.

Configure the announcement details with information that should be displayed on the program opportunity announcement page that is shown to prospective applicants. You must provide a banner image, grant synopsis, eligibility summary, and grant description.

**Note:** The information entered in the Define program activity also appears in the program announcement.

## Add points of contact to a Grant Program

Add members of your internal program team to a points of contact list to allow them to be contacted by grant seekers. This list is displayed on the grants program announcement page.

### About this task

Add members of your internal team who can be contacted by grant seekers.These users and their contact information are displayed publicly on the announcement page.

Adding a person will create a resource assignment record where the resource \(user\_resource\) field is a reference to a user \(sys\_user\) record. The resource role reference will be added to the points of contact list.

A new record is created in the sn\_plng\_att\_core\_resource\_assignment table with the user's name in the resource field, point of contact role in the role field, and the grant program name in the planning item field. In the user\_has\_resource table, if a record for that user and point of contact role already exists, no new record is created; otherwise, a new record is added.

To ensure a user can be added as a point of contact, make sure the user has the **pps\_resource** role and an employee profile \(sn\_employee\_profile\) record. For information on how to create an employee profile, see.

**Note:** Points of contact can only be added from the internal team list record. To add members to the internal team list record, see [Add members to a Grant Program internal program team](psds-gmp-using-add-members-internal-program-team.md).

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **CSM Configurable Workspace** &gt; **List**.

2.  Select **Grant Programs** &gt; **My grant programs**.

3.  Navigate to **All** &gt; **User Resource Roles**.

4.  Add a record for the desired user and set the resource role to **Point of contact**.

5.  Verify the user appears in the point of contact resource\_role record, as well as in the proposal playbook activity.


