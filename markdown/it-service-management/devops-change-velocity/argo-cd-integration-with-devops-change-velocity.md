---
title: Argo CD integration with DevOps Change Velocity
description: Connect to your Argo CD instance to automate the deployment of applications from GitHub repositories.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Argo CD integration with DevOps Change Velocity

Connect to your Argo CD instance to automate the deployment of applications from GitHub repositories.

## Argo CD integration overview

This integration enables the ServiceNow platform to manage the change request closure process based on the sync status received from Argo CD for continuous deployment of applications.

You must activate the DevOps Integration with Argo CD plugin \(sn\_devops\_argocd\) before connecting your Argo CD instance in ServiceNow. For more information on activating a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Workflow

Here is the workflow of how the continuous deployment process works through Argo CD in ServiceNow DevOps.

-   Create an Argo CD tool connection in ServiceNow DevOps Change Velocity using the Classic or Workspace UI.
-   Create a webhook in Argo CD manually.
-   Update your Config file in the GitHub repository for deployment. While updating the Config file, specify the change request number in the commit tag \(sn\_devops\_change-&lt;change request number&gt;\).

    **Note:** The change request number specified in the commit tag must already be created by the CI pipeline and in the implement state.

-   Sync the required app associated with your Config file and repository in Argo CD.
-   Once sync is successful, notifications are sent to ServiceNow DevOps and inbound events are created.
-   Change request number is retrieved from the inbound events and updated with the Argo CD synchronization status.
-   Change request is closed and based on the sync status, the close code, worknotes, and close notes fields are updated in the change request.

## Example

The following examples specify how changes made in Argo CD are notified to ServiceNow DevOps through the webhook.

-   The Config file is updated in GitHub with the following commit tag format:![Commit tag format in GitHub](../image/argocd-1.png)
-   Inbound events are created in ServiceNow when an app is synced in Argo CD:![Inbound event on sync in Argo CD](../image/argocd-2.png)
-   If sync is successful, the change request is closed and the close code, worknotes, and close notes fields are updated in the change request:![Change request updated with close state on successful sync in Argo CD](../image/argocd-3.png)![Change request work notes updated on successful sync in Argo CD](../image/argocd-4.png)

-   **[Onboard Argo CD to DevOps Change Velocity – Workspace](../task/onboard-argo-cd-to-devops-change-velocity-workspace.md)**  
Connect to your Argo CD instance using the DevOps Change Workspace playbook to automate the deployment of applications from GitHub repositories.
-   **[Onboard Argo CD to DevOps Change Velocity — Service Catalog](../task/sc-argo-cd.md)**  
Connect your Sonar instance using the ServiceNow Service Catalog.
-   **[Onboard Argo CD to DevOps Change Velocity — Classic](../task/onboard-argo-cd-to-devops-change-velocity-classic.md)**  
Connect your Argo CD instance using the Classic UI in DevOps Change Velocity.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

