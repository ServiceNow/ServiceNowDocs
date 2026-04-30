---
title: Components, tables, and roles used by Opportunity Marketplace \(OPM\)
description: Learn about the components used with Opportunity Marketplace.
locale: en-US
release: zurich
product: Opportunity Marketplace
classification: opportunity-marketplace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference Opportunity Marketplace roles and tables, Opportunity Marketplace, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Components, tables, and roles used by Opportunity Marketplace \(OPM\)

Learn about the components used with Opportunity Marketplace.

## Opportunity Marketplace roles and tables

You can configure which columns are visible in forms. Select the gear icon in the header of the form to personalize which columns you want to see and how they’re formatted.

**Important:** The descriptions in these tables don’t contain all available fields. Select the gear icon in the header of the form to see all available fields.

<table id="table_jrz_snv_xbc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin \[sn\_opp\_market.admin\]

</td><td>

The OPM admin role enables access to the administrative modules for the app.

 The OPM admin role contains these roles.

-   `[sn_egd_shared_lib.admin]`
-   `[flow_designer]`
-   `[user_criteria_admin]`

</td></tr></tbody>
</table><table id="table_mpw_vnv_xbc"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Opportunity \[sn\_opp\_market\_opportunity\]

</td><td>

Tracks details about an opportunity, such as-   **Title**
-   **Opportunity type**
    -   **Gig**
    -   **Project**
    -   **Volunteer**
-   **State**
-   **Owners**
-   **Published date**

</td></tr><tr><td>

Opportunity Location Mapping \[sn\_opp\_market\_m2m\_opp\_location\]

</td><td>

Tracks details about the location of the opportunity-   **City**
-   **Country**
-   **Location**

</td></tr><tr><td>

Opportunity position \[sn\_opp\_market\_opportunity\_position\]

</td><td>

Tracks information about the job \(opportunity\) that is available, such as-   **Title**
-   **Opportunity**
-   **Description**
-   **Location**
-   **Employee levels**

</td></tr><tr><td>

Opportunity Type Auxiliary \[sn\_opp\_market\_opportunity\_type\_aux\]

</td><td>

Holds the names of approvers for an opportunity type

</td></tr><tr><td>

User Opportunity Preference \[sn\_opp\_market\_user\_opportunity\_preference\]

</td><td>

Tracks the user preferences of an applicant, such as-   **Configuration item**
-   **Employee**
-   **Table**: The table that contains details related to the opportunity preference configuration item.

</td></tr><tr><td>

Opportunity Preference Configs \[sn\_opp\_market\_opportunity\_preference\_config\]

</td><td>

Tracks the details of the opportunities, such as -   **Display name**
-   **Name**
-   **Active**
-   **Type**
-   **Table**
-   **Field**

</td></tr><tr><td>

Opportunity Type \[sn\_opp\_market\_opportunity\_type\]

</td><td>

Tracks details about opportunities \(Gig, Project, Volunteer\), such as -   **Title**: The type of opportunity. The standard opportunities provided with OPM are Gig, Project, and Volunteer. You can create your own opportunity types, see [Create opportunities in Opportunity Marketplace](../task/egd-create-other-opportunities.md).
-   **Description**
-   **Role display**
-   **Icon**
-   **Active**
-   **Updated**: The date the opportunity was last updated.

</td></tr><tr><td>

Role Application \[sn\_opp\_market\_position\_application\]

</td><td>

Tracks details of the application for a role by an applicant.-   **Employee**: The name of the applicant.
-   **Role**: The position being applied for.
-   **State**
-   **Submission Message**: The message that an applicant created to submit with the application.
-   **Created**: The date the application was submitted.

</td></tr><tr><td>

Position Skill \[sn\_opp\_market\_opportunity\_position\_skill\]

</td><td>

Tracks the skills that are associated with a role, such as-   **Opportunity role**
-   **Skill**
-   **Skill level**

</td></tr><tr><td>

Application Quick Link \[sn\_opp\_market\_quick\_link\]

</td><td>

Tracks quick link details that are displayed on an application form, such as-   **Application**
-   **Display order**
-   **Title**
-   **URL**

</td></tr><tr><td>

Shared Opportunity \[sn\_opp\_market\_shared\_opp\]

</td><td>

Tracks the details of opportunities that have been shared with an employee, such as-   **Created**: The date the opportunity was created.
-   **Opportunity**: The number for an opportunity. An opportunity can be a job posting, an opportunity, or an opportunity role.
-   **Recipient**: The employee who the opportunity was shared with.
-   **Sender**: The employee who sent or shared the opportunity with another employee.

</td></tr></tbody>
</table>## Hiring Core tables and roles

Hiring Core \[sn\_ta\_hiring\_core\] is a dependent application that is installed when you install OPM.

Hiring Core provides a repository where you can store information that you’ve created or received from any third party talent acquisition platform for your hiring requirements.

The description contains examples of some of the available columns. Select the gear icon to see all the available columns \(fields\).

<table id="table_gl3_zh3_b1c"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applicant certification \[sn\_ta\_hiring\_core\_applicant\_certification\]

</td><td>

Tracks data related to an applicant's certifications, such as -   **Certificate name**
-   **Issuer name**
-   **Valid till**

.

</td></tr><tr><td>

Applicant education \[sn\_ta\_hiring\_core\_applicant\_education\]

</td><td>

Tracks an applicant's related educational data, such as-   **Institute name**
-   **Field of study**
-   **Degree type**
-   **Location**

</td></tr><tr><td>

Applicant work experience \[sn\_ta\_hiring\_core\_applicant\_work\_exp\]

</td><td>

Tracks an applicant's work experience, such as-   **Company name**
-   **Start date**
-   **End date**
-   **Presently working here** \(true or false\)
-   **Location**

</td></tr><tr><td>

Candidate \[sn\_ta\_hiring\_core\_job\_applicant\]

</td><td>

Tracks an applicant's basic information, such as name and email address.

</td></tr><tr><td>

Extracted Skill \[sn\_ta\_hiring\_core\_extracted\_skills\]

</td><td>

Track's details about skills extracted from the Skills Foundation app, including-   **Job applicant**
-   **Skill**
-   **Skill name**

</td></tr><tr><td>

Interview attendee \[sn\_ta\_hiring\_core\_interview\_attendee\]

</td><td>

Track's details about interview participants and the interview process details.-   **Name**
-   **Hiring role**
-   **Acceptance status**
-   **Job interview**
-   **Job title**
-   **Type**

</td></tr><tr><td>

Interview slot \[sn\_ta\_hiring\_core\_interview\_slot\]

</td><td>

Tracks information about the **Job interview** and the interview start and end dates and time.

</td></tr><tr><td>

Job Application \[sn\_ta\_hiring\_core\_job\_application\]

</td><td>

Tracks job applications and related records, such as-   **Number**: the application number.
-   **Job requisition**
-   **Job applicant**
-   **State**
-   **Applied on**: the date an applicant applied for this job.

</td></tr><tr><td>

Job Board \[sn\_ta\_hiring\_core\_job\_board\]

</td><td>

Tracks information about related job boards, such as-   **Name**: the name of the job board.
-   **Logo**
-   **Active**

</td></tr><tr><td>

Job Hiring Team \[sn\_ta\_hiring\_core\_job\_hiring\_team\]

</td><td>

Tracks information about your hiring team, such as-   **Job requisition**
-   **Hiring role**
    -   **Hiring manager**
    -   **Interviewer**
    -   **Recruitment coordinator**
-   **Team Member**: The name of the interviewer.
-   **Type**: The designation of **Primary interviewer** or **Optional interviewer**.
-   **Visibility to applicant**: The flag that determines whether an applicant can see information about the hiring team \(true = visible, false = not visible\).

</td></tr><tr><td>

Job interview \[sn\_ta\_hiring\_core\_job\_interview\]

</td><td>

Tracks key information related to an interview and the interview process, such as-   **Number**
-   **Interview name**
-   **Interview type**
-   **State**
-   **Interview start**
-   **Interview end**

</td></tr><tr><td>

Job Posting \[sn\_ta\_hiring\_core\_job\_posting\]

</td><td>

Tracks job posting details, such as-   **Number**: The number used to track a job posting.
-   **Title**
-   **Job requisition**: the number of the job requisition associated with a job posting. A job requisition can have more than one associated job posting.
-   **Job board**
-   **Location flexibility**
-   **State**
-   **Posting date**

</td></tr><tr><td>

Job Requisition \[sn\_ta\_hiring\_core\_job\_requisition\]

</td><td>

Tracks your job requisition details, such as-   **Employment type**
    -   **Full-time employee**
    -   **Part-time employee**
    -   **Temporary employee**
    -   **Contingent**
    -   **Contractor**
-   **Hiring manager**
-   **Job title**
-   **Number**: The number used to track the job requisition details.
-   **Number of headcounts**
-   **Primary location**

 Select the form personalization icon at the top of the form the select which fields are displayed in the form.

</td></tr><tr><td>

Profile link \[sn\_ta\_hiring\_core\_profile\_link\]

</td><td>

-   **Site**
-   **Job Applicant**
-   **Link**
-   **Type**

</td></tr><tr><td>

Recruitment Task \[sn\_ta\_hiring\_core\_recruitment\_task\]

</td><td>

Tracks the tasks that are associated with a job requisition, such as-   **Number**: the job requisition number
-   **Priority**
-   **State**
-   **Assigned to**: The name of the recruiter the task is assigned to.
-   **Short description**

</td></tr></tbody>
</table><table id="table_ch4_5n5_bdc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[sn\_ta\_hiring\_core.admin\]

</td><td>

Admin

</td></tr><tr><td>

\[sn\_ta\_hiring\_core.applicant\]

</td><td>

Applicant

</td></tr><tr><td>

\[sn\_ta\_hiring\_core.external\_applicant\]

</td><td>

This role is for the external applicants and contains the applicant and the \[snc\_external\] role.

</td></tr><tr><td>

\[sn\_ta\_hiring\_core.hiring\_manager\]

</td><td>

Hiring manager

</td></tr><tr><td>

\[sn\_ta\_hiring\_core.internal\_applicant\]

</td><td>

This role is for the internal applicants and contains the applicant and the \[snc\_internal\] role.

</td></tr><tr><td>

\[sn\_ta\_hiring\_core.interviewer\]

</td><td>

Interviewer

</td></tr><tr><td>

\[sn\_ta\_hiring\_core.recruiter\]

</td><td>

Recruiter

</td></tr><tr><td>

\[sn\_ta\_hiring\_core.recruitment\_coordinator\]

</td><td>

Recruitment coordinator

</td></tr></tbody>
</table>**Parent Topic:**[Reference Opportunity Marketplace roles and tables](../concept/egd-oppt-mrktplc-references.md)

