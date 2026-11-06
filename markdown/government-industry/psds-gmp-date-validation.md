---
title: Grants Management date validations
description: The Grants Management date validations hierarchy defines how funding timelines nest and relate to one another in the grants management system. All dates are validated in sequence to prevent scheduling conflicts and ensure conformance with funding program constraints.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/government-industry/psds-gmp-date-validation.html
release: australia
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 10
keywords: [date validation, grants management, funding program, grant program, timeline]
breadcrumb: [Grants Management reference, Reference, Public Sector Digital Services \(PSDS\)]
---

# Grants Management date validations

The Grants Management date validations hierarchy defines how funding timelines nest and relate to one another in the grants management system. All dates are validated in sequence to prevent scheduling conflicts and ensure conformance with funding program constraints.

## Date definitions

The date hierarchy, visually represents the nesting relationship of all dates in the Grants Management system.

\[Omitted image "date-hierarchy-diagram.png"\] Alt text: Visual representation of the date hierarchy in grants management

The following table defines each date used in the grants management validation hierarchy and the phase it occurs in:

|Date|What it means|Phase|
|----|-------------|-----|
|Funding Program start date|The date the funding program's overall funding window opens. Every Grant Program created under it must start on or after this date.|Funding Program setup|
|Funding Program end date|The date the funding program's overall funding window closes. Every Grant Program under it must end on or before this date.|Funding Program setup|
|Grant Program start date|The date this specific grant program's own window opens; every internal date must fall on or after it.|Grant Program setup|
|Grant Program end date|The date this grant program's own window closes; every internal date must fall on or before it.|Grant Program setup|
|Announcement publication date|The date the program's public announcement goes live on the portal.|Publish program|
|Proposal publication date|The date applicants can begin submitting proposals. Indicates when the "Apply Now" button is enabled, allowing applicants to begin submitting proposals.|Publish program|
|Proposal close date|The hard deadline for proposal submission. After this date, new submissions are blocked and any proposal still in Draft is auto-cancelled by the "Cancel Expired Grant Proposals" scheduled job.|Publish program|
|Announcement removal date|The date the public announcement is taken down from the portal.|Publish program|
|Review task due date|The deadline for the Merit Review activity's review task.|Merit Review|
|Program Milestone due date|The deadline for a Program Milestone defined on the program.|Grant Program setup \(Program Milestones activity\)|
|Goals \(Calendar period\)|The calendar period attached to a proposal goal.|Proposal Narrative|
|Deliverables \(Calendar period\)|The calendar period attached to a Goal's deliverable.|Proposal Narrative|
|Award start date|The date the award starts. It must fall within the grant program's start and end dates.|Award setup|
|Award end date|The date the award ends. Milestone due dates and disbursement dates must fall within the award start and end dates.|Award setup|
|Award milestone due date|The deadline for a milestone on an award. It must fall within the award start and end dates.|Award milestones|
|Disbursement start date|A date field on the award's disbursement plan. Disbursement schedule generation doesn't use it. The schedule runs on the award's own start and end dates. If the field is changed, the new date must fall within the award start and end dates.|Award disbursements|
|Disbursement end date|A date field on the award's disbursement plan. Disbursement schedule generation doesn't use it. The schedule runs on the award's own start and end dates. If the field is changed, the new date must fall within the award start and end dates.|Award disbursements|
|Disbursement task due date|The due date of a disbursement task on an award. It must fall within the award start and end dates.|Award disbursements|

## Error prevention checklist

When setting up a new grant program, verify:

-   Grant Program: Grant program dates fall entirely within Funding Program dates.
-   Merit review: All Merit Review task due dates are within Grant Program window and not in the past.
-   Publish Program:
    -   Publish Now:

        When selected, the program will be published immediately. These two date fields must be entered manually:

        -   Proposal close date
        -   Announcement removal date
        **Note:** These two date fields don't appear on the form but are automatically populated to the current system date and time:

        -   Announcement Publication Date: Set to current date and time
        -   Proposal Publication Date: Set to current date and time
    -   Schedule Publication:

        When selected, allows you to manually define future publication dates. These dates must satisfy the sequence requirements:

        ```
        Announcement publication date ≤ Proposal publication date ≤ Proposal close date ≤ Announcement removal date
        ```

-   Proposal deliverables: All Proposal Submission window dates are within Grant Program window.
-   No circular date dependencies. For example, an end date before a start date.

## Date validations by grant setup activity

The following table captures the grants date validations across every grant phase or activity.

**Note:** The two-digit year format \(yy\) isn't supported. Use the dd/mm/yyyy format.

<table><thead><tr><th>

Phase

</th><th>

Condition

</th><th>

Result

</th><th>

Message shown

</th></tr></thead><tbody><tr><td rowspan="4">

Grant Program

</td><td>

Program start date is after the earliest of the other dates in the same grant program \(milestone dates excluded\).

</td><td>

BLOCKED

</td><td>

The program start date cannot be after the \{date name\} \{date\}.

</td></tr><tr><td>

Program end date is before the latest of its other dates \(milestone dates excluded\).

</td><td>

BLOCKED

</td><td>

The program end date cannot be before the \{date name\} \{date\}.

</td></tr><tr><td>

Program start date is before the funding program's start date.

</td><td>

BLOCKED

</td><td>

The program start date cannot be before the funding program start date \{date\}.

</td></tr><tr><td>

Program end date is after the funding program's end date.

</td><td>

BLOCKED

</td><td>

The program end date cannot be after the funding program end date \{date\}.

</td></tr><tr><td rowspan="3">

Publish program

</td><td>

Any of the four dates \(Announcement Publication Date/Proposal Publication Date/Proposal Close Date/Announcement Removal Date\) is earlier than the current date/time, or before the Program Start Date.

</td><td>

BLOCKED

</td><td>

Date can't be before program start date. Date must be in the future.

</td></tr><tr><td>

A date is earlier than the running-maximum valid date already seen earlier in the sequence \(Announcement Publication ≤ Proposal Publication ≤ Proposal Close ≤ Announcement Removal\)

</td><td>

BLOCKED

</td><td>

Date can't be before \{publish program-date option\}Example: Date can't be before proposal publication date.

Example: Date can't be before proposal close date.

</td></tr><tr><td>

Any of the four dates is after the Program End Date.

</td><td>

BLOCKED

</td><td>

Date can't be after program end date.

</td></tr><tr><td rowspan="3">

Merit Review

</td><td>

Review task due date is set to a date before today.

</td><td>

BLOCKED

</td><td>

Date cannot be in the past.

</td></tr><tr><td>

Review task due date is before the Grant Program's own start date.

</td><td>

BLOCKED

</td><td>

The review task due date cannot be before the program start date.

</td></tr><tr><td>

Review task due date is after the Grant Program's own end date.

</td><td>

BLOCKED

</td><td>

The review task due date cannot be after the program end date.

</td></tr><tr><td>

Milestone

</td><td>

Milestone due date falls outside the program's start/end dates, or is in the past.

</td><td>

BLOCKED

</td><td>

Inline error on the milestone due date field.

</td></tr><tr><td rowspan="3">

Award dates

</td><td>

The award start date is after the award end date.

</td><td>

BLOCKED

</td><td>

`Award start date must occur before the award end date.`

</td></tr><tr><td>

The award start date is outside the grant program's start and end dates.

</td><td>

BLOCKED

</td><td>

`Award start date must fall within the grant program's start and end dates.`

</td></tr><tr><td>

The award end date isn't after the award start date.

</td><td>

Error shown on the field

</td><td>

`Award end date must occur after the award start date.`

</td></tr><tr><td rowspan="2">

Award milestones

</td><td>

A milestone due date is before the award start date or after the award end date, on the form or when the milestone is saved.

</td><td>

BLOCKED

</td><td>

`Milestone due date must fall within the award start and end dates.`

</td></tr><tr><td>

A milestone is created under an award that is cancelled or closed.

</td><td>

BLOCKED

</td><td>

`Cannot create a milestone under a cancelled or closed award.`

</td></tr><tr><td rowspan="4">

Award disbursements

</td><td>

The disbursement start date field is changed to a date outside the award start and end dates. The field isn't used to generate the disbursement schedule.

</td><td>

BLOCKED

</td><td>

`Disbursement start date must fall within the award start and end dates.`

</td></tr><tr><td>

The disbursement end date field is changed to a date outside the award start and end dates. The field isn't used to generate the disbursement schedule.

</td><td>

BLOCKED

</td><td>

`Disbursement end date must fall within the award start and end dates.`

</td></tr><tr><td>

A disbursement task due date is outside the award start and end dates.

</td><td>

BLOCKED \(form only\)

</td><td>

`Disbursement task due date must fall within the award start and end dates.`

</td></tr><tr><td>

A disbursement task is created under an award that is cancelled or closed.

</td><td>

BLOCKED

</td><td>

`Cannot create a disbursement task under a cancelled or closed award.`

</td></tr><tr><td rowspan="7">

Activate award

</td><td>

The award start date or end date is empty.

</td><td>

BLOCKED

</td><td>

`Complete the required award fields.`

</td></tr><tr><td>

The award has no milestone, or a milestone has no due date.

</td><td>

BLOCKED

</td><td>

`Add at least one performance milestone with a due date.`

</td></tr><tr><td>

A disbursement task has no due date.

</td><td>

BLOCKED

</td><td>

`Set due dates on all disbursements.`

</td></tr><tr><td>

The system property **sn\_svc\_appl\_pgm\_mg.grant\_agreement.required** is set to `true` and no grant agreement document is uploaded to the award. This check isn't enforced while the property is `false`, its shipped value.

</td><td>

BLOCKED

</td><td>

`Upload the signed grant agreement.`

</td></tr><tr><td>

The award has no disbursement type.

</td><td>

BLOCKED

</td><td>

`Configure the disbursement plan.`

</td></tr><tr><td>

A milestone due date is before today.

</td><td>

BLOCKED

</td><td>

`Update the past-due performance milestone due date(s): {record numbers}`

</td></tr><tr><td>

A disbursement task due date is before today.

</td><td>

BLOCKED

</td><td>

`Update the past-due disbursement due date(s): {record numbers}`

</td></tr></tbody>
</table>**Note:**

When you select **Activate award** on a draft award and confirm, the Activate award checks all run together and the award activates only if none fails. If one check fails, the message is `Cannot activate award. The award can't be activated because` followed by the reason. If several checks fail, the message is `Cannot activate award. Resolve the following before you activate this award:` followed by one bullet for each failed check. The record numbers in the past-due messages link to the milestone or disbursement task. Milestones in any state are checked for missing and past-due dates. Cancelled and Rejected disbursement tasks aren't checked. Today is the server date when you confirm the activation.

The grant agreement check applies only when the system property **sn\_svc\_appl\_pgm\_mg.grant\_agreement.required** is set to `true`. The property ships set to `false`, so by default an award can be activated without a grant agreement document.

## Supported customization points

A customization point is the correct place to modify a validation's behavior. It's always a public wrapper class \(like `ServiceApplicantPgrmMgmtUtil`\), not the internal implementation \(Impl\) class.

The platform routes its own calls through the public wrapper. If you override the Impl class instead, your code won't run. It will also break on the next upgrade. The Impl class is an implementation detail that can be restructured without warning. Override the public wrapper class, not the Impl class.

The date-validation logic spans three application scopes. Stay in scope and confirm that you hold the correct scope and roles before editing. Select the matching scope access and roles to make changes:

-   Service Applicant Program Management \(sn\_svc\_appl\_pgm\_mg\)
-   Grants Management \(sn\_gsm\_grnt\_mgmt\)
-   Service Applicant Information \(sn\_svc\_appl\_info\)

**Important:**

Customize program and publish opportunity date logic at the public API class `ServiceApplicantPgrmMgmtUtil` that callers already reference and not by subclassing internal implementation \(Impl\) classes. All components run within a specific application scope. Always test in a non-production instance first.

<table><thead><tr><th>

Validation area

</th><th>

Customize at

</th><th>

Scope

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Grant program &amp; funding program dates

</td><td>

Public class `ServiceApplicantPgrmMgmtUtil`

</td><td>

sn\_svc\_appl\_pgm\_mg

</td><td>

—

</td></tr><tr><td>

Publish program dates

</td><td>

Public class `ServiceApplicantPgrmMgmtUtil`

</td><td>

sn\_svc\_appl\_pgm\_mg

</td><td>

The `onChange` client scripts and the client-to-server bridge only forward parameters to this class. Customize the public wrapper, never the Impl class directly.

</td></tr><tr><td>

Draft proposal auto-cancellation after close date

</td><td>

Scheduled Job "Cancel Expired Grant Proposals" \(runs daily at 3:30 AM\)

</td><td>

sn\_gsm\_grnt\_mgmt

</td><td>

Adjust the job schedule, or disable it, to change automatic cancellation of draft proposals.

</td></tr><tr><td>

Proposal deliverables \(Goals\)

</td><td>

UX Client Script Include `serviceApplicantInfoUIUtils`

</td><td>

sn\_svc\_appl\_info

</td><td>

UI-layer validation for required, unique, and non-empty deliverables.

</td></tr><tr><td>

Milestones

</td><td>

Milestones activity client logic

</td><td>

sn\_gsm\_grnt\_mgmt

</td><td>

No standalone validator — change milestone date behavior within the activity logic rather than a shared utility.

</td></tr><tr><td>

Merit Review task due date

</td><td>

Client script MeritReviewDateCheck \(past-date check\) and `ServiceApplicantPgrmMgmtUtilImpl.onValidateStartAndEndDate` \(same general check as Grant Program\)

</td><td>

sn\_svc\_appl\_pgm\_mg

</td><td>

Three separate mechanisms enforce the same field, so a change needs to span across all three

</td></tr><tr><td>

Award activation checks

</td><td>

The **Activate award** UI action, and the helper methods on the public class `AwardProgramManagementUtil`

</td><td>

sn\_svc\_appl\_pgm\_mg

</td><td>

Customize the helper methods on the public class, not the Impl class. To change which checks run or the messages shown, customize the UI action.

The helper methods are:

-   `validatePerformanceMilestoneByAward`
-   `getMilestonesWithPastDueDate`
-   `getMilestonesWithMissingDueDate`
-   `getDisbursementTasksWithPastDueDate`
-   `getDisbursementTasksWithMissingDueDate`
-   `isGrantAgreementRequired`

</td></tr><tr><td>

Award, milestone, and disbursement date checks

</td><td>

The business rules **Milestone due date check** and **Validate Disbursement Dates Within Award Window**, and the client scripts on the award, milestone, and disbursement review task forms

</td><td>

sn\_svc\_appl\_pgm\_mg

</td><td>

No shared public validator exists. Change the behavior in the individual business rule or client script.

</td></tr></tbody>
</table>