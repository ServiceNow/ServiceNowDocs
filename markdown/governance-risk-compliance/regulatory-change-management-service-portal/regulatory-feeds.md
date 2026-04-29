---
title: Regulatory alerts
description: Regulatory alerts are an aggregation of different regulatory events and documents that are sourced from multiple regulatory intelligence providers. Similar to web feeds, a regulatory alert is a record of these regulatory changes. Such changes are frequently updated, and the alerts help you stay informed about the regulatory landscape.
locale: en-US
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory alerts

Regulatory alerts are an aggregation of different regulatory events and documents that are sourced from multiple regulatory intelligence providers. Similar to web feeds, a regulatory alert is a record of these regulatory changes. Such changes are frequently updated, and the alerts help you stay informed about the regulatory landscape.

The Regulatory Change Management application transforms and maps the alerts. The application provides the information in regulatory alert tables.

The Regulatory Change Management life cycle starts with the regulatory alert record. Each regulatory alert record contains metadata that helps stakeholders to translate the changes, create an action plan, and implement actions to comply with the regulatory changes.

With the Regulatory Change Management application, you can use the regulatory alerts to inform the users about regulatory updates.

## Types of alerts and associated regulatory tasks

Different types of alerts are displayed under the Regulatory Alerts module in the Regulatory Change Management application.

You can use the following types of regulatory alerts:

-   Regulatory event alerts: Signify alerts, provide updates to news, and provide insights on regulatory changes. Alerts are by default regulatory event alerts. All RSS feeds result in a regulatory alert record.
-   Source document alerts: Signify changes to the citations. Citations are like various sections of an authority document. ServiceNow® GRC offers the Network Frontiers Unified Compliance Framework \(UCF\) integration. The integration creates authority documents after the import, and it creates corresponding citations under each authority document. When an existing citation is updated or a new citation is inserted, it signifies a change in the source document. Source document alerts are only available when integrating with a third-party regulatory intelligence provider; for example, Thomson Reuters.

The difference between a regulatory event alert and a source document alert is scope. Regulatory event alerts signify general alerts for general changes and for upcoming regulatory changes. In contrast, source document alerts signify changes that are specific to the citations. When an existing citation is updated or a new citation is inserted, it signifies a change in the source document.

The different types of alerts each involve a separate set of regulatory tasks. These tasks are created whenever a user with the sn\_grc\_reg\_change.user or sn\_grc\_reg\_change.admin role takes an alert and then marks it as applicable. These tasks are the following:

-   Regulatory change task: This task is created for regulatory event alerts. The task is used to evaluate the changes and to update the GRC objects, such as policies, controls, and risk statements in the library.
-   Source document import task: This task is created for source document alerts. The task is used to update an existing citation or to insert a new citation that is received from the provider into the regulatory library.

## Alerts and user roles

Alerts can have different states. The main property of an alert is whether it’s assigned or unassigned. For assigned alerts, the **Coordinator** field has a value. An alert can be assigned either to a user with the sn\_grc\_reg\_change.manager role or the sn\_grc\_reg\_change.user or sn\_grc\_reg\_change.admin role. In contrast, an unassigned alert isn’t assigned to anyone.

You can do various actions on unassigned alerts. These actions are the following:

-   Update
-   Applicable
-   Defer
-   Initiate Impact Assessment
-   Not Applicable
-   Cancel Regulatory Alert
-   Delete

When an unassigned regulatory event alert is marked as applicable, a regulatory change task is created. When an unassigned source document alert is marked as applicable, a source document import task is created.

When an unassigned alert is marked as not applicable with due comments, its state is updated as Closed in the regulatory alert form.

Assigned alerts can have different states. These states are the following:

-   New
-   Deferred
-   Impact Assessment
-   In Progress
-   Closed

In terms of user roles, all alerts can be accessed by users with either the sn\_grc\_reg\_change.admin role or the sn\_grc\_reg\_change.manager role. Users with the sn\_grc\_reg\_change.user role can view assigned alerts that are assigned to them, but they can’t view unassigned alerts or alerts that are assigned to other people.

## Table cleaners for regulatory alerts

The alert records that are marked as not applicable must be cleaned at regular intervals. The Regulatory Change Management application provides table cleaners for cleaning the alert records automatically. Users specify the time and frequency for the cleanup activity. Only users with the sn\_grc\_reg\_change.admin role can perform cleanup activities.

Similarly, registry file records that have been processed can be cleaned at specified time intervals.

-   **[Perform actions on regulatory alerts](../task/perform-actions-reg-event-feeds.md)**  
Perform various actions on unassigned and other types of regulatory alerts. For example, you can assign an unassigned alert, initiate impact assessment on an alert, and mark an alert as applicable, among other actions.
-   **[Add an AI-recommended citation to a regulatory alert](../task/add-recommended-citations-to-a-regulatory-alert.md)**  
Add an AI-recommended citation to a regulatory alert by using the GRC: Predictive Intelligence application.
-   **[Manage and assign regulatory event alerts](../task/manage-regulatory-feeds.md)**  
Assign regulatory event alerts that are received from the regulatory intelligence provider to an appropriate user. You can review other properties of the regulatory event alert.
-   **[Train and use the similarity solution to recommend citations on regulatory alerts](../task/retrain-ml-reg-compliance-mapping.md)**  
Train and use the machine learning solution by activating the Governance, Risk, and Compliance Predictive Intelligence plugin. The solution enables the system to automatically recommend correct citations on regulatory alerts to associate.
-   **[Manage and assign source document alerts](../task/manage-source-document-feeds.md)**  
Assign source document alerts that are received from the regulatory intelligence provider to an appropriate user. You can review other properties of the source document alert.

**Parent Topic:**[Regulatory Change Management Core UI](using-rcm-classic-ui.md)

