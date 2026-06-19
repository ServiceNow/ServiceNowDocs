---
title: Set up the grants program announcement details
description: Build the program announcement. Define the required forms, terms and conditions, required budget categories, and external-facing point of contact. Provides you with an opportunity to review the grant details.Add members of your internal program team to a points of contact list to allow them to be contacted by grant seekers. This list is displayed on the grants program announcement page.Add links, knowledge articles, or documents that provide supplemental information about this program, its sponsoring agency, impact, or any other details that may help grant seekers better understand this opportunity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/public-sector-digital-services/psds-using-gmp-pgr-announcement.html
release: zurich
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-03-11"
reading_time_minutes: 3
breadcrumb: [Grants Management Program Setup, Grants Management, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Set up the grants program announcement details

Build the program announcement. Define the required forms, terms and conditions, required budget categories, and external-facing point of contact. Provides you with an opportunity to review the grant details.

Configure the announcement details with information that should be displayed on the program opportunity announcement page that is shown to prospective applicants. You must provide a banner image, grant synopsis, eligibility summary, and grant description.

**Note:** The information entered in the Define program activity also appears in the program announcement.

## Add points of contact to a Grant Program

Add members of your internal program team to a points of contact list to allow them to be contacted by grant seekers. This list is displayed on the grants program announcement page.

### About this task

The Points of Contact \(POC\) activity allows a Grant Program Manager to define members of the internal program team who can be contacted by grant seekers. These team members’ names and contact details will be published on the Portal and visible to applicants. This ensures that grant seekers have visibility into the appropriate internal team members for communication and inquiries.

Adding a person will create a resource assignment record where the resource \(user\_resource\) field is a reference to a user \(sys\_user\) record. The resource role reference will be added to the points of contact list.

A new record is created in the sn\_plng\_att\_core\_resource\_assignment table with the user's name in the resource field, point of contact role in the role field, and the grant program name in the planning item field. In the user\_has\_resource table, if a record for that user and point of contact role already exists, no new record is created; otherwise, a new record is added.

To ensure a user can be added as a point of contact, make sure the user has the **pps\_resource** role and an employee profile \(sn\_employee\_profile\) record. For information on how to create an employee profile, see.

**Note:** Points of contact can only be added from the internal team list record. To add members to the internal team list record, see [Add members to a Grant Program internal program team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-gmp-using-add-members-internal-program-team.md).

### Before you begin

Role required: admin, sn\_svc\_appl\_pgm\_mg.grant\_program\_manager

### Procedure

1.  Navigate to **All** &gt; **CSM Configurable Workspace** &gt; **List**.

2.  Select **Grant Programs** &gt; **My grant programs**.

3.  Navigate to **All** &gt; **User Resource Roles**.

4.  Add a record for the desired user and set the resource role to **Point of contact**.

5.  Verify the user appears in the point of contact resource\_role record, as well as in the proposal playbook activity.


### What to do next

[Configure program resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-using-gmp-pgr-announcement.md).

## Configure program resources

Add links, knowledge articles, or documents that provide supplemental information about this program, its sponsoring agency, impact, or any other details that may help grant seekers better understand this opportunity.

### Before you begin

Role required: admin, sn\_svc\_appl\_pgm\_mg.grant\_program\_manager

### About this task

The **Create program announcement** stage continues with the **Resources and support** activity, which allows a Grant Program Manager to add any resources for applicants to have access to the necessary supporting materials. Grants program managers can add links, knowledge articles, or documents, and can order these resources in order of importance. A minimum of one resource is required to complete this activity. You may skip the activity if there are no supplemental resources to add.

### Procedure

1.  Navigate to the **Create program announcement** stage of the Grants setup playbook.

2.  Select **Add Resource**, and use the dropdown to add links, knowledge articles, or documents that provide supplemental information about this program, its sponsoring agency, impact, or any other details that may help grant seekers better understand this opportunity.

3.  Select **Save**, and repeat the process until all supplemental information has been added.

4.  Select **Mark Complete**.


### Result

The program announcement as it will appear on the grants portal is now configured.

### What to do next

.

