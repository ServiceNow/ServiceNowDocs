---
title: Create an application - Workspace
description: Create applications using the DevOps Change Workspace and associate pipelines, plans, and repositories to it.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Applications, DevOps Change Velocity, IT Service Management]
---

# Create an application - Workspace

Create applications using the DevOps Change Workspace and associate pipelines, plans, and repositories to it.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.app\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace**.

2.  You can create an application using any of the following options:

    -   Select **Create an application** from the Home page.
    -   Select the **Applications** \(![Applications icon.](../image/applications-icon.png)\) module and select **New**.
3.  In the Create an application modal, in the **Application name** field, enter the name for your application.

    ![Create an application.](../image/app-ws-01.png)

    You can either create a new application, which will create a new application model with the same name, or select an existing application model, which will create an application with the same name as the model.

<table id="table_mlr_qzd_zyb"><thead><tr><th>

Type

</th><th>

Result

</th></tr></thead><tbody><tr><td>

New application

</td><td>

-   The system generates a new DevOps application, a new application model, and a new SDLC component \(SDLC-C\) in the CMDB.
-   The SDLC-C is assigned the same name as the new application.
-   If the DevOps Config application is installed, then DevOps associates the application to the CDM application.


</td></tr><tr><td>

Existing application model

</td><td>

The system generates a new DevOps application from that application model.

-   The application is given the same name as the application model.
-   If an SDLC component exists for the application model, then DevOps associates the SDLC-C to the new application.
-   If an SDLC component doesn’t exist for the application model, then DevOps generates a new SDLC-C with the same name as the application model.
-   If DevOps Config is installed, then DevOps creates a CDM application and associates the SDLC-C to the application.


</td></tr></tbody>
</table>    The Create an Application playbook activity opens.

4.  In the Enter application details playbook activity:

    1.  Select the **Business app** in CMDB that you want linked to your application.
    2.  Add user groups to the **Maintained by** field to control access to the application.

        You can select any group that has at least one user with DevOps roles. When user groups are added:

        -   Users with DevOps App Owner role or DevOps Administrator role can edit the application.
        -   Users having other DevOps roles can view the application.
        -   Users having DevOps roles, but aren’t part of the groups added can't view the application.
    3.  Select **Next**.
    ![Enter the application details.](../image/app-ws-02.png)

5.  In the Associate pipelines playbook activity:

    1.  Add the orchestration tools whose pipelines you want to associate with the app to the **Tools** field.

        **Note:** You can skip this step if you haven't connected to an orchestration tool, or if you don't want to associate pipelines.

    2.  Select the pipelines that you want to associate with the app.
    3.  Select **Associate pipelines**.
    ![Associate pipelines to the application.](../image/app-ws-03.png)

6.  In the Assign services to pipeline steps playbook activity:

    1.  For each selected pipeline, all steps or stages are imported for the last successful execution. You can select the following for each pipeline step:
        1.  **Pipeline step type**: Select a step type for which you want to assign a service.

            **Tip:** Specify at least the **Prod deploy** step type for steps that represents the production deployment to enable DevOps to identify successful pipeline executions as production deployments.

        2.  **Service**: Select the CMDB application service that the pipeline step maps to.

            Application service maps approximately to the environment. If you use the same pipeline step to deploy to different environments, leave the field empty. Service information enables DevOps to identify and report on operational metrics such as incidents, outages, and so on.

    2.  Select **Assign services**.
    **Note:** You can skip this step if your pipeline doesn’t have any steps or if you haven't associated pipelines.

    ![Assign services to pipeline steps.](../image/app-ws-04.png)

7.  In the Associate plans playbook activity:

    1.  Add the planning tools whose plans you want to associate with the app to the **Tools** field.

        **Note:** You can skip this step if you haven't connected to a planning tool, or if you don't want to associate plans.

    2.  Select the plans that you want to associate with the app.
    3.  Select **Associate plans**.
    ![Associate plans to the application.](../image/app-ws-05.png)

8.  In the Associate repositories playbook activity:

    1.  Add the coding tools whose repositories you want to associate with the app to the **Tools** field.

        **Note:** You can skip this step if you haven't connected to a coding tool, or if you don't want to associate repositories.

    2.  Select the repositories that you want to associate with the app.
    3.  Select **Associate repositories**.
    ![Associate repositories to the application.](../image/app-ws-06.png)

9.  In the Import historical data playbook activity:

    1.  Select the start and end dates for import. You can import up to 90 days of data.

        **Note:** You can skip this step if you don't want to import any data from the select pipelines, plans, and repositories.

    2.  Select **Import data**.
    ![Import data to the application.](../image/app-ws-07.png)

    **Note:** If your import request could not be completed due to an error, you can select **Restart Import** in the corresponding **Import Request** record to retry the import.

    ![Restart Import button for Import Request](../image/restart-import-request.png)

10. From the **Summary** page, select **View application** to review the details of the created application.

    ![Application summary.](../image/app-ws-08.png)

    If you skipped associating objects to the application or if you want to associate other objects, see [Associate tool objects to applications - Workspace](apps-associate-objects-wkspc.md).


