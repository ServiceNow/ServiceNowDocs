---
title: Components installed with Hiring Core
description: Several types of components are installed with activation of the Hiring Core plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Components installed with Hiring Core

Several types of components are installed with activation of the Hiring Core plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_ivr_hqb_pdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Hiring Core admin

 \[sn\_ta\_hiring\_core.admin\]

</td><td>

This role is the super admin in the Hiring Experiences environment.

</td><td>

-   Hiring Core - Hiring manager

\[sn\_ta\_hiring\_core.hiring\_manager\]

-   Hiring Core - Recruiter

\[sn\_ta\_hiring\_core.recruiter\]

-   Talent Profile admin

sn\_ta\_tp.talent\_profile\_user


</td></tr><tr><td>

Hiring Core - Hiring manager\[sn\_ta\_hiring\_core.hiring\_manager\]

</td><td>

This role is for the hiring manager for a job requisition.

</td><td>

-   Skills Foundation user

\[skill\_user\]

-   Manager Hub user

\[sn\_mh.manager\_hub\_user\]

-   Talent Profile user

\[sn\_ta\_tp.talent\_profile\_user\]


</td></tr><tr><td>

Hiring Core - Recruiter\[sn\_ta\_hiring\_core.recruiter\]

</td><td>

This role is for the recruiter who creates and manages the job requisitions.

</td><td>

-   Skills Foundation user

\[skill\_user\]

-   Placeholder

\[template\_read\_global\]

-   Placeholder

\[template\_editor\_group\]

-   Placeholder
-   \[email\_composer\]
-   Recruitment coodinator

\[sn\_ta\_hiring\_core.recruitment\_coodinator\]

-   Talent Profile user

\[sn\_ta\_tp.talent\_profile\_user\]

-   Canvas user

\[canvas\_user\]


</td></tr><tr><td>

Hiring Core - Recruitment Coodinator

</td><td>

This role is for the recruiter coordinator who creates interviews and manages the application workflow.

</td><td>

-   Placeholder

\[template\_editor\_group\]

-   Placeholder

\[template\_read\_global\]

-   Canvas user

\[canvas\_user\]


</td></tr><tr><td>

Hiring Core - Interviewer\[sn\_ta\_hiring\_core.interviewer\]

</td><td>

This role is to provide an interviewer required information.

</td><td>

None

</td></tr><tr><td>

Hiring Core - Applicant\[sn\_ta\_hiring\_core.applicant\]

</td><td>

This role is to provide common information to both the internal and external applicants.

</td><td>

None

</td></tr><tr><td>

Hiring Core - Applicant external\[sn\_ta\_hiring\_core.external\_applicant\]

</td><td>

This role is for the external applicants and contains the snc\_external role. It applies to any external applicant who isn’t an employee of the company.

</td><td>

None

</td></tr><tr><td>

Hiring Core - Applicant internal\[sn\_ta\_hiring\_core.internal\_applicant\]

</td><td>

This role is for the internal applicants and contains the applicant and the snc\_internal role.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_kvr_hqb_pdc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MarkApplicantInactive

</td><td>

Deactivates applicants no longer viable to the system at regular intervals.

</td></tr><tr><td>

Notify Recruiters and Hiring manager on alternate days

</td><td>

Notifies the recruiters and the hiring managers when interview feedback is not received from the applicant.

</td></tr></tbody>
</table>## Tables installed

<table id="table_mvr_hqb_pdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applicant certification

 \[sn\_ta\_hiring\_core\_applicant\_certification\]

</td><td>

Certification details shared by the applicants.

</td></tr><tr><td>

Applicant education\[sn\_ta\_hiring\_core\_applicant\_education\]

</td><td>

Education details shared by the applicants.

</td></tr><tr><td>

Applicant work experience\[sn\_ta\_hiring\_core\_applicant\_work\_exp\]

</td><td>

Work experience details shared by the applicants.

</td></tr><tr><td>

Extracted skills\[sn\_ta\_hiring\_core\_extracted\_skills\]

</td><td>

Details of skills shared by the applicants.

</td></tr><tr><td>

Hiring Task\[sn\_ta\_hiring\_core\_hiring\_task\]

</td><td>

Details of the extracted skills from entered values by the applicants.

</td></tr><tr><td>

Interview attendee\[sn\_ta\_hiring\_core\_interview\_attendee\]

</td><td>

Details of interview attendees for a role.

</td></tr><tr><td>

interview Feedback\[sn\_ta\_hiring\_core\_interview\_feedback\]

</td><td>

Details of the interview feedback received.

</td></tr><tr><td>

Interview slot\[sn\_ta\_hiring\_core\_interview\_slot\]

</td><td>

Stores data of the interview slots.

</td></tr><tr><td>

Candidate\[sn\_ta\_hiring\_core\_job\_applicant\]

</td><td>

List of candidates stored in the system.

</td></tr><tr><td>

Job Application\[sn\_ta\_hiring\_core\_job\_application\]

</td><td>

List of job applications received.

</td></tr><tr><td>

Job Board\[sn\_ta\_hiring\_core\_job\_board\]

</td><td>

Gathers data of the job board.

</td></tr><tr><td>

Job Hiring Team\[sn\_ta\_hiring\_core\_job\_hiring\_team\]

</td><td>

Details of the hiring team for a requisition.

</td></tr><tr><td>

Job interview\[sn\_ta\_hiring\_core\_job\_interview\]

</td><td>

Details of interviews for a job requisition.

</td></tr><tr><td>

Job Posting\[sn\_ta\_hiring\_core\_job\_posting\]

</td><td>

Details of the job postings for each job requisition.

</td></tr><tr><td>

Job Requisition\[sn\_ta\_hiring\_core\_job\_requisition\]

</td><td>

List of job requisitions in the system.

</td></tr><tr><td>

Profile link\[sn\_ta\_hiring\_core\_profile\_link\]

</td><td>

Details of the profile linking data.

</td></tr><tr><td>

Interview reschedule history\[sn\_ta\_hiring\_core\_reschedule\_history\]

</td><td>

Historic data of the interview schedules.

</td></tr></tbody>
</table>**Parent Topic:**[Hiring Experiences reference](reference-frmwrk-ta.md)

