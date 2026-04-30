---
title: Regulatory process flow and tasks
description: The Regulatory Change Management process flow includes the tasks that different users can perform to help your organization manage and comply with regulatory changes.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory process flow and tasks

The Regulatory Change Management process flow includes the tasks that different users can perform to help your organization manage and comply with regulatory changes.

Regulatory alerts are sourced from the external providers that provide the data as regulatory alerts. The alert may be received as Really Simple Syndication \(RSS\) feeds or from an external provider such as the Thomson Reuters Regulatory Intelligence \(TRRI\). The Regulatory Change Management application receives the new regulatory changes that are applicable to an organization.

The Regulatory Change Management application has the following user roles:

-   RCM administrator: A user who has the sn\_grc\_reg\_change.admin role.
-   RCM Manager: A user who has the sn\_grc\_reg\_change.manager role.
-   RCM User or coordinator: A user who has the sn\_grc\_reg\_change.use role. This user ensures that the regulatory changes are assigned to the correct teams and that the changes are completed in time.
-   Business user role: A user who has the sn\_grc.business\_user role.
-   Risk or Compliance manager: A user who has the sn\_risk.manager or sn\_compliance.manager role. This user would perform the changes as part of the Regulatory Change Management application.

For more information about the roles, see [User roles in Regulatory Change Management](../reference/roles-installed-rcm.md).

## Regulatory Change Management process flow

The following infographic shows the Regulatory Change Management process flow.

![Regulatory process flow and tasks. For a text description, refer to the steps that follow.](../image/regulatory-change-management-process-flow.png "Regulatory Change Management process flow and tasks performed by different users")

The steps to complete the Regulatory Change Management process flow are:

1.  Set up the integration. Your customers can subscribe to a public RSS feed for the regulatory bodies or they can subscribe to a subscription provider such as TRRI that is a curated intelligence provider. A subscription provider can aggregate the regulatory changes from different sources and provide the collective changes as feeds.
2.  Set up an internal taxonomy. The taxonomy elements are the different classifiers that an organization can apply to its regulatory content to categorize it. You can use taxonomy elements to create a hierarchical structure of different classifications for setting up the regulatory content for an organization.
3.  Review a regulatory alert. A user with the sn\_grc\_reg\_change.manager role \(RCM manager\) reviews a regulatory alert and assigns it to a coordinator or a user with the sn\_grc\_reg\_change.user role \(RCM user\). The user with the sn\_grc\_reg\_change.user role reviews the alert. If the regulatory change requires an impact assessment, the RCM user sends it to a subject matter expert \(SME\) with a business user role.
4.  Assess the impact. The subject matter expert \(SME\) with a business user role assesses the impact of the regulatory change and sends the score of the impact assessment to the Regulatory Change Management application. If the alert is not applicable to the organization, the RCM user closes the alert. If the alert is applicable to the organization, the RCM user creates a new regulatory change task and assigns it to the same or a new coordinator.
5.  Devise an action plan. The coordinator identifies the steps to comply with the regulatory change, devises an action plan, and creates the action tasks for the different teams that need to complete the identified action items. The coordinator then creates the action tasks that are associated with the regulatory change task. After the action plan is created, it’s sent to the RCM manager for an approval. The manager reviews the action plan and confirms if more action tasks need to be created or if some of the action tasks aren’t necessary.
6.  Complete the action tasks. The compliance analyst sends the actions for approval to a user with the sn\_grc\_reg\_change.manager role \(RCM manager\). If the action plan is rejected, the coordinator goes through the action plan, updates the actual tasks, and sends the action plan back for an approval. The compliance manager can see all compliance-based action tasks and the risk manager can see all the risk-based action tasks. After the tasks are assigned to the risk and compliance users, the action tasks are tracked until they are completed. A due date is marked and tracked for the action tasks. When the tasks are completed, the regulatory alert and the parent regulatory change tasks are closed and the change process flow is completed.

**Parent Topic:**[Exploring Regulatory Change Management](what-is-rcm.md)

**Related topics**  


[Regulatory Change Management application landing page](rcm-workspace-for-managers.md)

[Tasks page in the Compliance Workspace](tasks-page.md)

[Source document import tasks](source-document-import-tasks.md)

[RSS feeds overview](rss-feeds.md)

[Impact assessments for the regulatory alerts](impact-assessment-task.md)

[Regulatory assessment for a regulatory alert](regulatory-assessment-in-rcm.md)

[Next Experience Discuss and Chat Collaboration](next-experience-discuss-chat-collaboration.md)

[Regulatory Change Management application in the Compliance Workspace](rcm-workspace-overview.md)

