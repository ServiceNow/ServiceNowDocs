---
title: Add custom conditions to enable ReleaseOps deployments
description: If you want to add additional conditions to enable ReleaseOps deployments, modify the Deployment Migration to ReleaseOps decision table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/app-engine-management-center/add-custom-conditions-to-enable-releaseops-deployment.html
release: zurich
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

    \[Omitted image "aemc-workflow-studio-decision-tables.png"\] Alt text: Select Decision tables on the Workflow Studio home page to display only decision tables.

3.  Select the decision table with the name **Deployment Migration to ReleaseOps**.

4.  Add conditions and results to the decision table to set up additional conditions for ReleaseOps deployments.

    **Tip:** For more information about how to use decision tables, see the following resources:

    -   
    -   

