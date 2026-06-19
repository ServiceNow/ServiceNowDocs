---
title: Add members to a Grant Program internal program team
description: Add members of the Internal Grant Program team who will be responsible for administering this program. Designate a program approver, lead and co-lead, collaborators, and observers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-gmp-using-add-members-internal-program-team.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set up a grant program, Grants Management Program Setup, Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Add members to a Grant Program internal program team

Add members of the Internal Grant Program team who will be responsible for administering this program. Designate a program approver, lead and co-lead, collaborators, and observers.

## About this task

The Internal Team plays a crucial role in supporting the Grant Program Manager throughout the lifecycle of the grant program. This group is responsible for assisting with the development and configuration of program parameters, managing internal processes, and ensuring that all compliance and operational requirements are met. Members collaborate to provide expertise across areas such as budgeting, timelines, proposal evaluations, and documentation, enabling a streamlined and transparent grant management process, and can be sub-classified as approver, observer, program lead, program co-lead, or other.

\[Omitted image "psds\_gmp\_internalpgrteam\_view.png"\] Alt text: internal progam team playbook view

These are different than points of contact that potential applicants can reach out to during the proposal phase.

To add public-facing points of contact that potential applicants can reach out to, see [Add points of contact to a Grant Program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-using-gmp-pgr-announcement.md).

## Before you begin

Role required: sn\_gsm\_grnt\_mgmt.program\_manager, sn\_gsm\_grnt\_mgmt.grant\_director, sn\_svc\_appl\_pgm\_mg.grant\_program\_manager, or sn\_svc\_appl\_pgm\_mg-grant\_program\_director

To add a user as an Internal Team Member, an Employee Profile must be created.

-   Approvers review and decide on approvals triggered by the “Complete Approval” activity and “Funding Proposal” process. Each Grant Program can only have one approver. To add a user as an Approver, the user must have the following role: **sn\_svc\_appl\_pgm\_mg.grant\_program\_director**

**Note:** All Internal Team Members must have the pps\_resource role; The pps\_resource role is essential for users to be managed within the Strategic Portfolio Management \(SPM\) application. Only users assigned this role can be included in resource plans and capacity planning.

## Procedure

1.  Open the grant program record for which you want to configure the internal program team members.

2.  Select the **Internal Program team** activity.

3.  In the **Employee name** field, enter the name of the employee you want to add as an internal program team member.

    These members are different than points of contact that potential applicants can reach out to during the grant proposal phase. You add public points of contact in a later step, using existing contacts from the **Employee name** drop-down list.

    **Note:**

    Only grant directors appear in the employee name.

4.  Select the role responsibility that the user will play within the grant program.

    By default, you can assign the following role responsibilities to users within the internal program team. These internal team member personas have been identified as generic roles across government grant spaces. For more information on how to customize these, see [Configure custom internal program team roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-internal-program-roles.md).

    To add members to this team, a user record must already have been created within the grants organization. This does not modify roles at a user level. For more information on user roles and responsibilities, see [Assign user personas, roles, groups, and responsibilities in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-assign-user-roles-responsibilities.md).

5.  Select **Save**.

6.  Repeat these steps until you have added all the users and their respective responsibilities to the internal program team list.

    \[Omitted image "psds\_gmp\_internalpgrteam\_view.png"\] Alt text: Internal Program Team agent view

7.  Select **Mark Complete**.


## Result

Whenever a user is added in the **Internal Program Team activity**, a new record is created in the sn\_plng\_att\_core\_resource\_assignment table with the user’s name in the resource field, the selected role in the role field, and the grant program name in the planning item field. In the user\_has\_resource table, if a record for that user and role already exists, no new record is created; otherwise, a new record is added.

The internal program team for this grant program has now been established. In a later step, the user with the approver responsibility will approve the grant program when it needs to be published.

To verify the assignments of internal program team members, you can go to the sn\_plng\_att\_core\_resource\_assignment table and verify the record. The "Planning Item” \(planning\_item\) field should reference the Grant Program ID, and the “User” \(user\_resource\) field should be populated as the user you are trying to add to the team. Every time a user is added as part of this activity, a record is created in the User Resource Role table for the specified role.

## What to do next

Establish the Grant Program budget, budget categories, and more.

