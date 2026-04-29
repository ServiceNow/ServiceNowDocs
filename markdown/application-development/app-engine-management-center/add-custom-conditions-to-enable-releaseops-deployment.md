---
title: Add custom conditions to enable ReleaseOps deployments
description: If you want to add additional conditions to enable ReleaseOps deployments, modify the Deployment Migration to ReleaseOps decision table.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Migration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Add custom conditions to enable ReleaseOps deployments

If you want to add additional conditions to enable ReleaseOps deployments, modify the Deployment Migration to ReleaseOps decision table.

## Before you begin

Role required: admin or app\_engine\_admin

## Procedure

1.  On your production instance, navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the Workflow Studio home page, select **Decision tables**.

    ![Select Decision tables on the Workflow Studio home page to display only decision tables.](../image/aemc-workflow-studio-decision-tables.png)

3.  Select the decision table with the name **Deployment Migration to ReleaseOps**.

4.  Add conditions and results to the decision table to set up additional conditions for ReleaseOps deployments.

    **Tip:** For more information about how to use decision tables, see the following resources:

    -   [Using decision tables](https://www.servicenow.com/docs/access?context=using-decision-builder&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
    -   [Modify decision table rules in Workflow Studio](https://www.servicenow.com/docs/access?context=modify-decision-table-rules&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

