---
title: Create an information request record using Information Request Playbook
description: Create an information request record in the Public Sector Digital Services application by using an Information Request Playbook activity. By using a playbook, you can have an efficient, streamlined way to create and resolve an information request.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Information Request Playbook, Playbooks, Use, Public Sector Digital Services \(PSDS\)]
---

# Create an information request record using Information Request Playbook

Create an information request record in the Public Sector Digital Services application by using an Information Request Playbook activity. By using a playbook, you can have an efficient, streamlined way to create and resolve an information request.

## Before you begin

**Note:** Before you start this procedure, verify that the Information Request Playbook application, which is separate from Public Sector Digital Services Core, is installed and enabled in the CSM Configurable Workspace. For instructions, see [Install Information Request Playbook for Public Sector Digital Services](install-psds-information-request-playbook.md).

Role required: sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, and sn\_gsm.service\_manager

## About this task

If a playbook is configured to use a record generator, you can create a record by using a playbook activity. If a case is already associated with a playbook, a new information request case type is opened in a new tab, with Playbook as the default tab. Creating a record from a list or form, or from an activity in another playbook, opens the Information Request Playbook and initiates the first activity. This activity, the first step of the Intake stage, guides you through the record creation process.

## Procedure

1.  In the CSM Configurable Workspace, navigate to **Lists** &gt; **Information Requests** &gt; **All**.

2.  Select **New**.

    The Information Request Playbook opens and initiates the first activity for collecting the request details, which is the Intake stage.

3.  On the Enter Request Details activity card, fill in the information.

4.  Select **Save**.

    A case is created with the information request information. The case number is added to the tab and the first activity in the Intake stage is marked as complete. The second activity in this stage is highlighted as the current activity.


