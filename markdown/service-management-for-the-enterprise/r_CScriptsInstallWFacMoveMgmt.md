---
title: Client scripts installed with Facilities Move Management
description: Client scripts define custom behaviors that run when events occur like when a form is loaded or submitted, or a cell changes value.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installed with Facilities Move Management, Activate Facilities Move Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Client scripts installed with Facilities Move Management

Client scripts define custom behaviors that run when events occur like when a form is loaded or submitted, or a cell changes value.

Facilities Move Management adds the following client scripts.

<table id="table_wtf_krf_2t"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remove bad date

</td><td>

Move Request\[move\_request\]

</td><td>

Remove default date

</td></tr><tr><td>

Autopopulate from\_location

</td><td>

Move Request\[move\_request\]

</td><td>

Auto-populate the from\_location based on the selected User to be moved.

</td></tr><tr><td>

Autopopulate From on embedded list

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Populate from location when a user is added

</td></tr><tr><td>

State is read only

</td><td>

Move Request\[move\_request\]

</td><td>

Set state to read only when state is Draft or Submitted

</td></tr><tr><td>

Warn to\_location not a Facility Space

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Warn the user that the **to location** is not a facility space \(fm\_space\)

</td></tr><tr><td>

Asset update

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Update assets for the user in a move

</td></tr><tr><td>

Close Complete Check

</td><td>

Enterprise Move Request\[enterprise\_move\_request\]

</td><td>

Check that all tasks are closed complete before setting request state

</td></tr><tr><td>

Autopopulate from location

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Populate from location when a user is added

</td></tr><tr><td>

hide submit

</td><td>

Move Request\[move\_request\]

</td><td>

Hide submit button when needed

</td></tr><tr><td>

Lock down form when request approved

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Prevent changes to the request after tasks are created

</td></tr><tr><td>

Info message

</td><td>

Move Request\[move\_request\]

</td><td>

Add an info message when state is Ready

</td></tr><tr><td>

Remove extra buttons on Workbench

</td><td>

Enterprise Move Scenario\[enterprise\_move\_scenario\]

</td><td>

Remove the extra buttons \(various icons, and so on\) while in a modal

</td></tr><tr><td>

Warn from\_location not a Facility Space

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Warn the user when the selected **from location** is a cmn\_location and not a facility space \(fm\_space\)

</td></tr><tr><td>

Warn from\_location not a Facility Space

</td><td>

Move Request\[move\_request\]

</td><td>

Warn the user when the selected **from location** is a cmn\_location and not a facility space \(fm\_space\)

</td></tr><tr><td>

Remove bad date2

</td><td>

Move Request\[move\_request\]

</td><td>

Remove default date

</td></tr><tr><td>

Set Building and Floor

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Automatically sets the destination building and floor when the **to location** is selected

</td></tr><tr><td>

Warn to\_location not a Facility Space

</td><td>

Move Request\[move\_request\]

</td><td>

Warn the user that the selected **from location** is a \(cmn\_location\)

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Move Management](r_InstallWFacMoveMgmt.md)

