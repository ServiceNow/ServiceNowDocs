---
title: Exploring Regulatory Change Management
description: The Regulatory Change Management application provides a framework that your organization can use to integrate with third-party regulatory intelligence providers to keep up with the regulatory changes and external regulations.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Regulatory Change Management, Governance, Risk, and Compliance]
---

# Exploring Regulatory Change Management

The Regulatory Change Management application provides a framework that your organization can use to integrate with third-party regulatory intelligence providers to keep up with the regulatory changes and external regulations.

## Regulatory Change Management overview

The Regulatory Change Management application enables you to manage your upcoming regulatory changes efficiently. The application provides the structured workflows that help your organization to assess the applicability of the regulatory changes, assess their impact, and implement risk and compliance-related changes.

The following infographic shows the process flow of the Regulatory Change Management application.

![Regulatory Change Management process flow.](../image/rcm-process-flow.png "Process flow of the Regulatory Change Management application")

The Regulatory Change Management application works with the following types of components:

-   Integration component: The regulatory intelligence partners typically provide the integration component. Through this integration, you can consume regulatory alerts into your instance.
-   Application framework component: The Regulatory Change Management application has an application framework component. This component provides the structured workflows that you can use to analyze and process the regulatory alerts that are received in the regulatory alerts table.

The Regulatory Change Management application consists of the following workflow:

1.  Manage regulatory taxonomy: Create an internal regulatory taxonomy that is specific to the ServiceNow AI Platform. You can map the taxonomy with the external taxonomies that are provided by the third-party regulatory intelligence providers for standardization. The internal taxonomy contains the following design elements:

    -   Content Type
    -   Jurisdiction
    -   Regulatory Body
    -   Sector
    -   Theme
    You can create and map these elements with the external taxonomy during the setup process.

2.  Integrate for regulatory intelligence: Integrate with the third-party regulatory intelligence providers and consume the alerts into your instance at regular intervals. You can monitor regulatory data in a rapidly changing environment.
3.  Triage regulatory events: Analyze the regulatory alerts and identify the regulatory events that are relevant to your organization.
4.  Assess impact: Assess the impact of regulatory events by using configurable impact assessment methodologies.
5.  Manage changes: Identify changes that should be done. These changes are implemented through the following action tasks:
    -   Update the underlying GRC objects, such as the policies, processes, risks, and controls in the regulatory library.
    -   Update the existing citations or import the new citations from the providers in the regulatory library.
6.  View reports and dashboards: Assess the state of the regulatory compliance by using reports and dashboards. You can maintain an audit trail of the compliance activities.

The following diagram shows the workflow of the Regulatory Change Management application.

![Regulatory Change Management workflow. For a text description, refer to the text that precedes this diagram.](../image/Regulatory_Change_Management_key_components.png "Workflow of the Regulatory Change Management application")

## Key product innovations

The following infographic shows the process for making innovations for the key products of the Regulatory Change Management application.

![Infographic that shows how to make key product innovations. A text description of the process follows.](../image/regulatory-change-management-product-key-innovations.png "Process for innovating key products")

The steps to complete the Regulatory Change Management process flow to innovate key products are:

1.  Set up the integration. Your customers can subscribe to a public RSS feed for the regulatory bodies or a subscription provider such as Thomson Reuters Regulatory Intelligence \(TRRI\) that is a curated intelligence provider. A subscription provider can aggregate the regulatory changes from different sources and provide the collective changes as feeds.
2.  Set up an internal taxonomy. The taxonomy elements are different classifiers that an organization can apply to its regulatory content to categorize it. You can use the taxonomy elements to create a hierarchical structure of the different classifications for setting up the regulatory content for an organization.
3.  Review a regulatory alert. A user with the sn\_grc\_reg\_change.manager role \(RCM manager\) reviews a regulatory alert and assigns it to a coordinator or a user with the sn\_grc\_reg\_change.user role \(RCM user\). The user with the sn\_grc\_reg\_change.user role reviews the alert. If the regulatory change requires an impact assessment, the RCM user sends it to a subject matter expert \(SME\) with a business user role.

    A user with sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles can generate AI-powered recommendations for a regulatory alert for the impacted citations, control objectives, and controls.

4.  Assess the impact. The subject matter expert \(SME\) with a business user role assesses the impact of the regulatory change and sends the score of the impact assessment to the Regulatory Change Management application. If the alert is not applicable to the organization, the RCM user closes the alert. If the alert is applicable to the organization, the RCM user creates a new regulatory change task and assigns it to the same coordinator or to a new coordinator.
5.  Devise an action plan. The coordinator identifies the steps to comply with the regulatory change, devises an action plan, and creates the action tasks for the different teams that must complete the identified action items. The coordinator then creates the action tasks that are associated with the regulatory change task. After the action plan is created, it’s sent to the RCM manager for an approval. The manager reviews the action plan and confirms if more action tasks must be created or if some of the action tasks aren’t necessary.
6.  Complete the action tasks and send them for review to a user with the sn\_grc\_reg\_change.manager role \(RCM manager\). If the action plan is rejected, the coordinator goes through the action plan, updates the actual tasks, and sends the action plan back for an approval. The compliance manager can see all compliance-based action tasks and the risk manager can see all risk-based action tasks. After the tasks are assigned to the risk and compliance users, the action tasks are tracked until they’re completed. A due date is marked and tracked for the action tasks. When the tasks are completed, the regulatory alert and the parent regulatory change tasks are closed and the change process flow is completed.

## A day in the life of a regulatory change manager

A user with the sn\_grc\_reg\_change.manager role \(RCM manager\) monitors, manages, decides, and verifies the regulatory changes on a daily basis.

The following infographic depicts a typical day for a regulatory change management.

![A user with the regulatory change manage role passes through various phases on a daily-basis.](../image/day-in-the-life-of-a-regulatory-change-manager.png "Typical day of a regulatory change manager")

-   **[Regulatory Change Management application landing page](rcm-workspace-for-managers.md)**  
The Regulatory Change Management application landing page view provides the overview of the regulatory activities in your organization. Users with the sn\_grc\_reg\_change.manager roles only can view the Regulatory Change Management landing page in the primary navigation in the Compliance Workspace.
-   **[Tasks page in the Compliance Workspace](tasks-page.md)**  
The Tasks page within the Compliance Workspace provides a centralized, task-centric interface for managing all activities related to regulatory events, source documents, and compliance workflows. It helps you stay organized, ensures timely and accountable action, and promotes overall regulatory readiness.
-   **[Source document import tasks](source-document-import-tasks.md)**  
The Regulatory Change Management application processes external alerts that may include citation titles, citation numbers, and references to legislative or regulatory materials relevant to compliance.
-   **[Regulatory process flow and tasks](reg-change-workflow-swimlane.md)**  
The Regulatory Change Management process flow includes the tasks that different users can perform to help your organization manage and comply with regulatory changes.
-   **[RSS feeds overview](rss-feeds.md)**  
A Really simple syndication \(RSS\) feed in Regulatory Change Management is like a subscription service for updates about new or changed rules and regulations. Instead of visiting multiple websites to check for updates, you can subscribe to feeds from regulatory bodies or industry news.
-   **[Impact assessments for the regulatory alerts](impact-assessment-task.md)**  
A regulatory event alert may result in a regulatory change to an organization. You can evaluate the impact of the regulatory change on your organization by performing impact assessments.
-   **[Regulatory assessment for a regulatory alert](regulatory-assessment-in-rcm.md)**  
Utilize the Smart Assessment Engine to perform smart assessments on regulatory alerts. This ability enhances regulatory decision-making by enabling impact assessments directly at the regulatory alert level, streamlining processes through a unified core assessment framework, and assigning analysis to multiple stakeholders for improved collaboration and efficiency.
-   **[Next Experience Discuss and Chat Collaboration](next-experience-discuss-chat-collaboration.md)**  
On a regulatory change management case, select **Discuss** from other options. Collaborate with virtual agents by using **Next Experience Chat Collaboration** and Discuss.
-   **[Regulatory Change Management application in the Compliance Workspace](rcm-workspace-overview.md)**  
Starting with GRC: Regulatory Change Management, version 13.0.1, the Regulatory Change Management application is available in Compliance Workspace. Compliance Workspace provides your users with a single-pane view so that they can check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes for the organization.
-   **[Exploring Now Assist in Regulatory Change Management \(RCM\)](rcm-exploring-now-assist-for-irm.md)**  
With Now Assist in Regulatory Change Management, part of the Now Assist for Integrated Risk Management \(IRM\) application, you can use agentic workflows and generative AI skills that streamline the analysis, summarization, and impact assessment of regulatory alerts. These capabilities empower compliance teams to act swiftly and accurately on regulatory changes.

**Parent Topic:**[Regulatory Change Management](../reference/reg-change-mgmt-landing-page.md)

