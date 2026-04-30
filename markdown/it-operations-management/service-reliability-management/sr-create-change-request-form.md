---
title: Create change request forms
description: Fill out the fields in the forms to create a change task to implement a controlled process for modifying approved and supported actions for SRM.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Service Reliability Management reference, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Create change request forms

Fill out the fields in the forms to create a change task to implement a controlled process for modifying approved and supported actions for SRM.

## Change request form

Create a new change request. For more information, see [Manually create an SRM change task](../task/sr-create-change.md).

<table id="id_pmn_dcs_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description of the change request.

</td></tr><tr><td>

Description

</td><td>

Description based on Short description.

</td></tr><tr><td>

Number

</td><td>

Identifier for the change request.

</td></tr><tr><td>

Category

</td><td>

Category for the change request. Choices are:

-   Hardware
-   Software
-   Service
-   System Software
-   Application Software
-   Network
-   Telecom
-   Documentation
-   Other \(default\)

</td></tr><tr><td>

Model

</td><td>

Model to use for the change request. Standard \(default\)

</td></tr><tr><td>

Risk

</td><td>

Risk the issue poses.Choice are:

-   High
-   Moderate \(default\)
-   Low

</td></tr><tr><td>

Type

</td><td>

Type of change request. Standard \(default\).

Read-only.

</td></tr><tr><td>

Impact

</td><td>

Impact the issue poses.Choices are:

-   1 - High
-   2 - Medium
-   3 - Low \(default\)

</td></tr><tr><td>

State

</td><td>

State of the change request.Choices are:

-   New \(default\)
-   Assess

If approval is required further states are unavailable.

-   Scheduled
-   Implement
-   Canceled

</td></tr><tr><td>

Work notes list

</td><td>

Team members to receive notifications when work notes are added.**Note:** An administrator must have already created an email notification for the work notes list for this to be available.

</td></tr><tr><td>

Work notes

</td><td>

Any additional information related to the request.

</td></tr></tbody>
</table>## Impact, Assignment, Planning, Schedule, Notes, and Closure information

<table id="id_s3q_tcs_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

Asset affected by the issue.

</td></tr><tr><td>

Service

</td><td>

Service affected by the issue.

</td></tr><tr><td>

Service offering

</td><td>

Service offering affected by the issue.

</td></tr><tr><td>

Assignment group

</td><td>

Team assigned to the change request

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the change request.

</td></tr><tr><td>

Justification

</td><td>

Reasoning for the change request.

</td></tr><tr><td>

Implementation plan

</td><td>

Imported text.

</td></tr><tr><td>

Risk and impact analysis

</td><td>

Analysis of risk and impact of the issue.

</td></tr><tr><td>

Backout plan

</td><td>

Imported text.

</td></tr><tr><td>

Test plan

</td><td>

Imported text.

</td></tr><tr><td>

Planned start date

</td><td>

Expected date to begin change.

</td></tr><tr><td>

Planned end date

</td><td>

Expected date to finish change.

</td></tr><tr><td>

Actual start date

</td><td>

Date change implementation began.

</td></tr><tr><td>

Actual end date

</td><td>

Date change implementation ended.

</td></tr><tr><td>

Conflict status

</td><td>

Not run. Read-only.

</td></tr><tr><td>

Conflict last run

</td><td>

Based on Conflict status. Read-only

</td></tr><tr><td>

Watch list

</td><td>

Interested users.

</td></tr><tr><td>

Work notes list

</td><td>

Team members to receive notifications when work notes are added.**Note:** An administrator must have already created an email notification for the work notes list for this to be available.

</td></tr><tr><td>

Additional comments

</td><td>

Additional notes for the request.

</td></tr><tr><td>

Work notes

</td><td>

Additional notes on the work done for the request

</td></tr><tr><td>

Close code

</td><td>

Code for the change request. Choices are:

-   None \(default\)
-   Successful
-   Successful with issues
-   Unsuccessful

</td></tr><tr><td>

Close notes

</td><td>

Notes on the change request closure.

</td></tr></tbody>
</table>**Parent Topic:**[Service Reliability Management reference](service-reliability-management-reference.md)

