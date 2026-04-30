---
title: Create a service request record using Service Request Playbook
description: Create a service request record in the Public Sector Digital Services application by using a Service Request Playbook activity. By using a playbook, you can have an efficient, streamlined way to create and resolve a service request.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Request Playbook, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Create a service request record using Service Request Playbook

Create a service request record in the Public Sector Digital Services application by using a Service Request Playbook activity. By using a playbook, you can have an efficient, streamlined way to create and resolve a service request.

## Before you begin

**Note:** Before starting this procedure, verify that the Service Request Playbook application, which is separate from Public Sector Digital Services Core, has been installed and enabled in the CSM Configurable Workspace. For instructions, see [Install Service Request Playbook for Public Sector Digital Services](install-psds-service-request-playbook.md).

Role required: sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, and sn\_gsm.service\_manager

## About this task

If a playbook is configured to use the record generator feature, you can create a record using a playbook activity. If a case is already associated with a playbook, a new service request case type is opened in a new tab, with Playbook as the default tab. Creating a record from a list or form, or from an activity in another playbook, opens the Service Request playbook and initiates the first activity. This activity, the first step of the intake stage, guides you through the record creation process.

## Procedure

1.  In the CSM Configurable Workspace, navigate to **Lists** &gt; **Service Requests** &gt; **All**.

2.  Select **New**.

    The Service Request Playbook opens and initiates the first activity for collecting the request details, which is the Intake stage.

3.  On each activity card, fill in the information.

    Select Skip to bypass an intake activity.

4.  Select **Save**.

    A case is created with the service request information. The case number is added to the tab and the first activity in the Intake stage is marked as complete. The second activity in this stage is highlighted as the current activity.


## What to do next

Continue using the playbook stages and activities to resolve the constituent's issue and complete the case.

