---
title: Create a runbook task
description: Create a runbook task to pause deployment and define the steps required to proceed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/releaseops/create-runbook-task.html
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, ReleaseOps, Deploying applications, Building applications]
---

# Create a runbook task

Create a runbook task to pause deployment and define the steps required to proceed.

## Before you begin

Role required: sn\_releaseops.releaseops\_tester or sn\_releaseops.releaseops\_developer

## About this task

Runbook tasks enable you to pause playbook progress until a task is resolved. To learn more about runbook tasks, see [Runbook tasks in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/runbook-tasks.md).

## Procedure

1.  On a deployment request record, select the **Deployment request tasks** tab in the Related lists section.

    \[Omitted image "releaseops-deployment-request-task-tab.png"\] Alt text: Select the Deployment request tasks tab.

2.  Select **New**.

3.  On the new deployment task record, select the playbook where you want the runbook task to occur.

    1.  In the **Pipeline stage** field, select the dropdown menu.

        \[Omitted image "releaseops-runbook-task-pipeline-stage.png"\] Alt text: Select the playbook where you want the runbook task to occur.

    2.  Select the playbook that you want the runbook task to occur in, either assessment or release.

4.  Select the playbook stage where you want the runbook task to occur.

    1.  In the **Playbook stage** field, enter the name of the playbook stage or find the available playbook stages using the lookup using list icon.

    2.  Select the playbook stage.

5.  Define when you want the runbook task to occur, either at the beginning or end of the selected playbook stage.

    1.  In the **Wait for runbook activity** field, select the Lookup using list icon\[Omitted image "lookup-using-list-icon.png"\] Alt text:.

        A dialog appears that displays the selected playbook stage and the options available for when the runbook task can occur.

        \[Omitted image "releaseops-wait-for-runbook-activity-dialog.png"\] Alt text: For the selected playbook stage, a dialog appears that shows the options for when the runbook task can occur.

    2.  In the dialog, select either **Before** the playbook stage or **After** the playbook stage.

6.  In the **Short description** field, describe the runbook activity that must occur.

    \[Omitted image "releaseops-runbook-task-short-desc-v1.png"\] Alt text: In the Short description field, describe the runbook task.

7.  Select **Submit**.


## Result

The runbook task is added to the playbook stage that you selected. When the playbook is executed, progress will stop until the runbook task is completed.

**Parent Topic:**[Using ReleaseOps to manage deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/using-releaseops-to-manage-deployments.md)

