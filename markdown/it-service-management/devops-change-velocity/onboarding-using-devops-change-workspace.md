---
title: Onboard to DevOps Change Velocity using Workspace
description: After installing DevOps Change Velocity, you can integrate with your DevOps toolchain and automate change requests directly from the DevOps Change Workspace.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, DevOps Change Velocity, IT Service Management]
---

# Onboard to DevOps Change Velocity using Workspace

After installing DevOps Change Velocity, you can integrate with your DevOps toolchain and automate change requests directly from the DevOps Change Workspace.

You can onboard as a DevOps admin, a tool owner, or an app owner.

## Onboard as DevOps admin

Role required: sn\_devops.admin.

1.  From the Home page, from the Get started with DevOps Change Velocity guide, select **Connect a tool**.

    ![Onboarding page for DevOps admins.](../image/onboard-01.png)

    **Note:** To automate change requests for pipelines, connect your orchestration tool.

2.  Using the connect playbook activity, connect to your DevOps tools.

    For more information about connecting to a tool, see [Integrating DevOps Change Velocity with third party tools](../concept/integrating-devops-change-with-third-party-tools.md).

3.  Select **Create an application** to create an application and associate objects to it.

    For more information about creating an application, see [Create an application - Workspace](app-create-workspace.md).

    ![Create an application.](../image/onboard-02.png)

4.  To automate change requests for pipelines, connect your orchestration tool and associate the pipelines with your application.

    For more information on associating pipelines, see [Associate tool objects to applications - Workspace](apps-associate-objects-wkspc.md).

5.  Select **Automate change** to create an automated change request.

    For more information about creating automated change requests, see [Automate DevOps change request creation](automate-devops-change-request.md).

    ![Automate change requests.](../image/onboard-03.png)

6.  Modify your orchestration pipeline to enable change control.

    You can run the pipeline to verify that change requests are automatically created.

    ![Waiting for change request creation.](../image/onboard-11.png)


The getting started guide will be marked as complete when the first automated change request is created by the orchestration pipeline.![Completed getting started guide for tool owner.](../image/onboard-08.png)

## Onboard as a tool owner

Role required: sn\_devops.tool\_owner.

1.  From the Home page, from the Get started with DevOps Change Velocity guide, select **Connect a tool**.

    ![Connect a tool.](../image/onboard-04.png)

    **Note:** To automate change requests for pipelines, connect your orchestration tool.

2.  Using the connect playbook activity, connect to your DevOps tools.

    For more information about connecting to a tool, see [Integrating DevOps Change Velocity with third party tools](../concept/integrating-devops-change-with-third-party-tools.md).

3.  If an application hasn't been created, ask your DevOps admin or app owner to create an application and associate objects to it.

    For more information about creating an application, see [Create an application - Workspace](app-create-workspace.md).

    ![Ask app owner to connect an application.](../image/onboard-10.png)

4.  To automate change requests for pipelines, connect your orchestration tool and associate the pipelines with your application.

    For more information on associating pipelines, see [Associate tool objects to applications - Workspace](apps-associate-objects-wkspc.md).

5.  Select **Automate change** to create an automated change request.

    For more information about creating automated change requests, see [Automate DevOps change request creation](automate-devops-change-request.md).

    ![Automate change requests.](../image/onboard-05.png)

6.  Modify your orchestration pipeline to enable change control.

    You can run the pipeline to verify that change requests are automatically created.


The getting started guide will be marked as complete when the first automated change request is created by the orchestration pipeline.![Completed getting started guide for tool owner.](../image/onboard-12.png)

## Onboard as an app owner

Role required: sn\_devops.app\_owner.

1.  Ask your DevOps admin or tool owner to connect to your DevOps tools.

    ![Getting started guide for app owners.](../image/onboard-06.png)

    **Note:** To automate change requests for pipelines, connect your orchestration tool.

2.  Select **Create an application** to create an application and associate objects to it.

    For more information about creating an application, see [Create an application - Workspace](app-create-workspace.md).

    ![Create an application.](../image/onboard-07.png)

3.  To automate change requests for pipelines, ask your DevOps admin or tool owner to connect your orchestration tool.
4.  Associate the pipelines for which you want to automate change requests with your application.

    For more information, see [Associate tool objects to applications - Workspace](apps-associate-objects-wkspc.md).

5.  Select **Automate change** to create an automated change request.

    For more information about creating automated change requests, see [Automate DevOps change request creation](automate-devops-change-request.md).

    ![Automate change requests.](../image/onboard-09.png)

6.  Modify your orchestration pipeline to enable change control.

    You can run the pipeline to verify that change requests are automatically created.


The getting started guide will be marked as complete when the first automated change request is created by the orchestration pipeline.![Completed getting started guide for app owner.](../image/onboard-13.png)

## Workspace widgets

-   **Tools widget**

    The Tools widget gives an overview of your connected tools, with the following details:

    -   Number of tools that are in the connected state. You can select the card to see the list of connected tools.
    -   Number of tools that need attention. You can select the card to see the list of unconfigured tools.
    -   Number of tools that are in disconnected state. You can select the card to see the list of disconnected tools.
    -   Number of tools grouped by their capabilities. You can select a capability to see the list of tools created for that capability.
    -   Number of tools grouped by their tool types. You can select an integration type to see the list of tools connections created for that particular tool type.
    -   DevOps admins and tool owners can connect to a tool from the widget.
    ![Tools widget.](../image/workspace-01.png)

-   **Applications widget**

    The Applications widget gives an overview of your applications, with the following details:

    -   Number of applications with at least one associated pipeline. You can select the card to see the list of apps with pipelines.
    -   Number of without any pipelines. You can select the card to see the list of apps with no pipelines.
    -   Number of work items, commits, and pipeline executions from all applications in the last 30 days. You can select the card to see the list of disconnected tools.
    -   Number of tools grouped by their capabilities. You can select a capability to see the list of tools created for that capability.
    -   Number of tools grouped by their tool types. You can select an integration type to see the list of tools connections created for that particular tool type.
    -   DevOps admins and app owners have the option to create an application from the widget.
    ![Applications widget.](../image/workspace-02.png)

-   **Automated change requests widget**

    The Applications widget gives an overview of your applications, with the following details:

    -   Number of change requests created in the last 30 days. You can select the card to see the list of change requests.
    -   Number of change requests that are pending approval in the last 30 days.
    -   Number of pipelines with change control enabled, but hasn't automatically created a change request.
    -   Number of tools grouped by their capabilities. You can select a capability to see the list of tools created for that capability.
    -   Number of tools grouped by their tool types. You can select an integration type to see the list of tools connections created for that particular tool type.
    ![Automated change requests widget.](../image/workspace-03.png)


