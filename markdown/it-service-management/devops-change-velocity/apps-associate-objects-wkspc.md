---
title: Associate tool objects to applications - Workspace
description: After creating an application, you can associate plans, repositories, and pipelines with it. Applications group plans, repositories, and pipelines from DevOps tools, which provides traceability to user stories, commits, test results, and so on.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Applications, DevOps Change Velocity, IT Service Management]
---

# Associate tool objects to applications - Workspace

After creating an application, you can associate plans, repositories, and pipelines with it. Applications group plans, repositories, and pipelines from DevOps tools, which provides traceability to user stories, commits, test results, and so on.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.app\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** &gt; **Applications**.

2.  Select the application.

3.  From the application record page, select the tab for the object type that you want to associate.

<table id="choicetable_ewm_tlh_wwb"><thead><tr><th align="left" id="d348627e77">

Object type

</th><th align="left" id="d348627e80">

Steps

</th></tr></thead><tbody><tr><td id="d348627e86">

**Pipelines**

</td><td>

1.  Select the **Pipelines** tab.
2.  Select **Associate pipelines**.
3.  From the list of pipelines available in DevOps, select the pipelines to track and associate with the application.
4.  Select **Associate pipelines**.
5.  **Assign services** to the pipeline steps.

For each selected pipeline, all steps or stages are imported for the last successful execution. You can select the following for each pipeline step:

    1.  **Pipeline step type**: Select a step type for which you want to assign a service.

**Tip:** Specify at least the **Prod deploy** step type for steps that represents the production deployment to enable DevOps to identify successful pipeline executions as production deployments.

    2.  **Service**: Select the CMDB application service that the pipeline step maps to.

Application service maps approximately to the environment. If you use the same pipeline step to deploy to different environments, leave the field blank. Service information enables DevOps to identify and report on operational metrics such as incidents, outages, and so on.

6.  If you want to import historical data for the pipelines, select the start and end dates and select **Import data**.

You can import up to 90 days of data.

7.  To import data after associating the pipelines, select the required pipelines from the **Pipelines** tab and select **Import data**. Select the start and end dates and select **Import data**.
 **Note:** While associating a pipeline with an app, the pipeline steps are also fetched during import.

 **Note:** When the property **Enable automatic association of repos to apps on pipeline execution** is enabled, if a repository is already associated to an application, then the corresponding unassigned pipelines are automatically assigned to the same app.

</td></tr><tr><td id="d348627e205">

**Plans**

</td><td>

1.  Select the **Plans** tab.
2.  Select **Associate plans**.
3.  From the list of plans available in DevOps, select the plans to track and associate with the application.
4.  Select **Associate plans**.
5.  If you want to import historical data for the plans, select the start and end dates and select **Import data**.

You can import up to 90 days of data.

6.  To import data after associating the plans, select the required plans from the **Plans** tab and select **Import data**. Select the start and end dates and select **Import data**.

**Note:** Historical import of plans data is not supported for GitHub Issues.

</td></tr><tr><td id="d348627e264">

**Repositories**

</td><td>

1.  Select the **Repositories** tab.
2.  Select **Associate repositories**.
3.  From the list of repositories available in DevOps, select the repositories to track and associate with the application.
4.  Select **Associate repositories**.
5.  If you want to import historical data for the repositories, select the start and end dates and select **Import data**.

You can import up to 90 days of data.

6.  To import data after associating the repositories, select the required repositories from the **Repositories** tab and select **Import data**. Select the start and end dates and select **Import data**.
 **Note:** When the property **Enable automatic association of repos to apps on pipeline execution** is enabled, repositories are automatically assigned to applications when a pipeline associated with an app identifies commits of a repository that is not yet associated.

</td></tr></tbody>
</table>4.  Select **Save**.


