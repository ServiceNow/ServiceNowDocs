---
title: Submit to CSF X Sandbox
description: Submit to CSF X Sandbox is an example of an activity definition process.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Activity Definitions, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit to CSF X Sandbox

Submit to CSF X Sandbox is an example of an activity definition process.

## Basic

The basic details captures the name \(label\), application, description, Table, and from which all applications it is accessible from.

Add the Automation plan, Activity experience and submit. Once submitted, edit the document to add more details against each tab.

## Automation Plan

The Automation Plan associates the backend action/subflow built using the flow designer. This example uses **Submit to Sandbox - ESCM Activity**sub-flow.

![Activity definitions](../image/sandbox.png)

![Activity Definition - Submit to CSF Sandbox](../image/sandbox-auto-plan.png)

This sub-flow enables submitting the malicious observables to sandbox. It has all the input fields and output fields defined.

Security incident is the input field.

## Activity Experience

In this example, **Record** type is selected.

## Associated Record

Associated record is to store the associated data pertaining to the current activity. This would capture the run time data, as well the status of the experience.

-   Associated table: Flow Data
-   Associated Record: VL
-   Experience status table: Flow Data
-   Experience Status record: VL

## Details

-   Tag Line: Send Email
-   Icon: Envelope outline
-   Title: **Activity** &gt; **Activity Instance** &gt; **Label**. Here we have selected the activity instance’s label. This dot walking will replace the label value as the title dynamically at run time.
-   Description: VL \(Sub-flow output is mapped\)
-   Pending State Title: blank
-   Pending State Description: blank
-   Record Fields
-   Footer

## Form

-   Form View: blank
-   Form Fields: blank

## Attachments

In this example:

-   Attachment Source - None
-   Attachment Read only - Unchecked

1.  Attachment Source - This is a drop down. What attachments to show on the card: those attached to the Parent Record, the Associated Record, or none.
2.  Attachment Read only - This is a True / False. Prevent the user from renaming or deleting the existing attachments.

## Features

In this example,

-   Show SLA - Unchecked
-   Show Checklist - Unchecked
-   Is Automated - Unchecked

## Playbook Actions in Activity Definition

This section has the actions that will be rendered on the activity card.

This example has Skip, View Sandbox Results, Submit to Sandbox, and Restart actions.

To add a new action to the activity card, you need to create a new record in the Playbook Actions related list present at the bottom of the page.

## Playbook override

No Playbook overrides for this example.

**Parent Topic:**[Activity Definitions](../concept/build-activities.md)

