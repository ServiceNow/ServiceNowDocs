---
title: Onboard to DevOps Change Velocity using Workspace
description: After installing DevOps Change Velocity, you can integrate with your DevOps toolchain and automate change requests directly from the DevOps Change Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-change-velocity/onboarding-using-devops-change-workspace.html
release: zurich
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

    \[Omitted image "onboard-01.png"\] Alt text: Onboarding page for DevOps admins.

    **Note:** To automate change requests for pipelines, connect your orchestration tool.

2.  Using the connect playbook activity, connect to your DevOps tools.

    For more information about connecting to a tool, see [Integrating DevOps Change Velocity with third party tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/integrating-devops-change-with-third-party-tools.md).

3.  Select **Create an application** to create an application and associate objects to it.

    For more information about creating an application, see [Create an application - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/app-create-workspace.md).

    \[Omitted image "onboard-02.png"\] Alt text: Create an application.

4.  To automate change requests for pipelines, connect your orchestration tool and associate the pipelines with your application.

    For more information on associating pipelines, see [Associate tool objects to applications - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/apps-associate-objects-wkspc.md).

5.  Select **Automate change** to create an automated change request.

    For more information about creating automated change requests, see [Automate DevOps change request creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/automate-devops-change-request.md).

    \[Omitted image "onboard-03.png"\] Alt text: Automate change requests.

6.  Modify your orchestration pipeline to enable change control.

    You can run the pipeline to verify that change requests are automatically created.

    \[Omitted image "onboard-11.png"\] Alt text: Waiting for change request creation.


The getting started guide will be marked as complete when the first automated change request is created by the orchestration pipeline.\[Omitted image "onboard-08.png"\] Alt text: Completed getting started guide for tool owner.

## Onboard as a tool owner

Role required: sn\_devops.tool\_owner.

1.  From the Home page, from the Get started with DevOps Change Velocity guide, select **Connect a tool**.

    \[Omitted image "onboard-04.png"\] Alt text: Connect a tool.

    **Note:** To automate change requests for pipelines, connect your orchestration tool.

2.  Using the connect playbook activity, connect to your DevOps tools.

    For more information about connecting to a tool, see [Integrating DevOps Change Velocity with third party tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/integrating-devops-change-with-third-party-tools.md).

3.  If an application hasn't been created, ask your DevOps admin or app owner to create an application and associate objects to it.

    For more information about creating an application, see [Create an application - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/app-create-workspace.md).

    \[Omitted image "onboard-10.png"\] Alt text: Ask app owner to connect an application.

4.  To automate change requests for pipelines, connect your orchestration tool and associate the pipelines with your application.

    For more information on associating pipelines, see [Associate tool objects to applications - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/apps-associate-objects-wkspc.md).

5.  Select **Automate change** to create an automated change request.

    For more information about creating automated change requests, see [Automate DevOps change request creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/automate-devops-change-request.md).

    \[Omitted image "onboard-05.png"\] Alt text: Automate change requests.

6.  Modify your orchestration pipeline to enable change control.

    You can run the pipeline to verify that change requests are automatically created.


The getting started guide will be marked as complete when the first automated change request is created by the orchestration pipeline.\[Omitted image "onboard-12.png"\] Alt text: Completed getting started guide for tool owner.

## Onboard as an app owner

Role required: sn\_devops.app\_owner.

1.  Ask your DevOps admin or tool owner to connect to your DevOps tools.

    \[Omitted image "onboard-06.png"\] Alt text: Getting started guide for app owners.

    **Note:** To automate change requests for pipelines, connect your orchestration tool.

2.  Select **Create an application** to create an application and associate objects to it.

    For more information about creating an application, see [Create an application - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/app-create-workspace.md).

    \[Omitted image "onboard-07.png"\] Alt text: Create an application.

3.  To automate change requests for pipelines, ask your DevOps admin or tool owner to connect your orchestration tool.
4.  Associate the pipelines for which you want to automate change requests with your application.

    For more information, see [Associate tool objects to applications - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/apps-associate-objects-wkspc.md).

5.  Select **Automate change** to create an automated change request.

    For more information about creating automated change requests, see [Automate DevOps change request creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/automate-devops-change-request.md).

    \[Omitted image "onboard-09.png"\] Alt text: Automate change requests.

6.  Modify your orchestration pipeline to enable change control.

    You can run the pipeline to verify that change requests are automatically created.


The getting started guide will be marked as complete when the first automated change request is created by the orchestration pipeline.\[Omitted image "onboard-13.png"\] Alt text: Completed getting started guide for app owner.

## Workspace widgets

-   **Tools widget**

    The Tools widget gives an overview of your connected tools, with the following details:

    -   Number of tools that are in the connected state. You can select the card to see the list of connected tools.
    -   Number of tools that need attention. You can select the card to see the list of unconfigured tools.
    -   Number of tools that are in disconnected state. You can select the card to see the list of disconnected tools.
    -   Number of tools grouped by their capabilities. You can select a capability to see the list of tools created for that capability.
    -   Number of tools grouped by their tool types. You can select an integration type to see the list of tools connections created for that particular tool type.
    -   DevOps admins and tool owners can connect to a tool from the widget.
    \[Omitted image "workspace-01.png"\] Alt text: Tools widget.

-   **Applications widget**

    The Applications widget gives an overview of your applications, with the following details:

    -   Number of applications with at least one associated pipeline. You can select the card to see the list of apps with pipelines.
    -   Number of without any pipelines. You can select the card to see the list of apps with no pipelines.
    -   Number of work items, commits, and pipeline executions from all applications in the last 30 days. You can select the card to see the list of disconnected tools.
    -   Number of tools grouped by their capabilities. You can select a capability to see the list of tools created for that capability.
    -   Number of tools grouped by their tool types. You can select an integration type to see the list of tools connections created for that particular tool type.
    -   DevOps admins and app owners have the option to create an application from the widget.
    \[Omitted image "workspace-02.png"\] Alt text: Applications widget.

-   **Automated change requests widget**

    The Applications widget gives an overview of your applications, with the following details:

    -   Number of change requests created in the last 30 days. You can select the card to see the list of change requests.
    -   Number of change requests that are pending approval in the last 30 days.
    -   Number of pipelines with change control enabled, but hasn't automatically created a change request.
    -   Number of tools grouped by their capabilities. You can select a capability to see the list of tools created for that capability.
    -   Number of tools grouped by their tool types. You can select an integration type to see the list of tools connections created for that particular tool type.
    \[Omitted image "workspace-03.png"\] Alt text: Automated change requests widget.


