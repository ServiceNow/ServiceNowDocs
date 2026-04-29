---
title: Run a playbook in Service Portal
description: Launch a playbook as a Service Portal requestor.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbooks in Service Portal, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Run a playbook in Service Portal

Launch a playbook as a Service Portal requestor.

## Before you begin

Role required: snc\_internal or snc\_external

## About this task

Keep track of where you're at in an overall process more easily, and pause and resume the playbook as needed.

## Procedure

1.  Navigate to your Service Portal instance.

2.  In the home screen, search for the playbook and select it.

    ![A Service Portal home screen](../images/service-portal-home-screen.png)

    The playbook launches.

3.  In the URL, you can apply the following properties to your playbook.

    ![An example URL for a playbook in Service Portal](../images/portal-playbook-URL.png)

    |Property|Description|Example|
    |--------|-----------|-------|
    |layoutType|Set the playbook to a custom layout. If not specified, defaults to the default \(standalone\) layout.|layoutType=custom|
    |table|Enter the parent table that the playbook opens on. If not specified, defaults to the Incident table.|table=incident|
    |sys\_id|Enter the parent Sys ID of the record you want to open in the record generator table. If you want to use the record generator, leave it as -1. If you leave it as -1, the value changes once the record is generated.|sys\_id=-1|
    |playbookExperienceid|Enter the playbook experience record ID with the playbook configurations that you want for your Service Portal users. If not specified, defaults to the Global Playbook Experience, which has a record ID of 9809a560f2200102920c912d4767e1a.|playbookExperienceid=9809a560f2200102920c912d4767e1a|

4.  As you go through the playbook, you can open records and lists in a modal without needing to leave Service Portal, such as when you view a Knowledge Base article or a user record via the information icon.

    ![Opening playbook modals in Service Portal](../images/portal-playbooks-modal.gif)


|Error|Description|
|-----|-----------|
|404: The page you are looking for could not be found|The table or sysId is missing from the URL or the URL is incorrect.​|
|Configuration Error|The process cannot be found by the playbook. For example the table is interaction, but the Sys ID does not exists for this table.​|
|There are not playbooks available|There is a valid record for the table, but the record does not satisfy the conditions to show the playbook. For example an interaction record might need to be of type Chat and start with the short description of PLAYBOOK: to kick off a playbook.​|
|No Activities Available|Here are not activities to view for this particular stage of playbook. Activities can be hidden based on user role or Run Conditions from the process.​|
|No filtered results|When using the playbook filter, no results can be shown for a particular stage.|

For client-side issues, check local browser console.logs which might show a runtime issue using the browser's inspector.

