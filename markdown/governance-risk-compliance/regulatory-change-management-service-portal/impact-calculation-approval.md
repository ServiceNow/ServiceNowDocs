---
title: Impact radius for regulatory alerts of type regulatory event
description: Adding impacted areas to a regulatory alert of type regulatory event helps to calculate the impact radius of a regulatory alert. Impact radius typically refers to the extent to which a regulatory change affects an organization.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Impact radius for regulatory alerts of type regulatory event

Adding impacted areas to a regulatory alert of type regulatory event helps to calculate the impact radius of a regulatory alert. Impact radius typically refers to the extent to which a regulatory change affects an organization.

## Impacted areas

The regulatory events that could have an impact on the compliance or risk posture of your organization should be assessed. Calculating the impact radius is a method for assessing the impact of the regulatory event on the GRC objects and for suggesting action tasks based on the assessment of the impact. The Regulatory Change Management application supports the impact radius calculation process for a regulatory alert. Calculating the impact radius is a method of automatically creating action tasks for the users.

Regulatory alerts are of two types:

-   Regulatory event
-   Source document

Prior to the Yokohama release, the Regulatory Change Management users had the option to add only one or more number of citations impacted due to any regulatory change. This led to sole reliance on only citations and omitted taking other business operations such as policies, control objectives, controls, risks, third-parties, and so on, into consideration. To address this problem, a new table called impacted area \(sn\_grc\_reg\_change\_impacted\_area\) is created and it captures the following items including the previously captured citations:

-   Citation
-   Control objective
-   Policy
-   Authority document
-   Control
-   Acknowledgment campaign
-   Policy category
-   Policy exception
-   Risk statement
-   Risk framework
-   Risk

**Note:** Impacted areas can be added to regulatory alerts that are of type regulatory event. For more information, see [Add impacted areas manually to a regulatory alert](../../now-assist-irm/task/add-impacted-area-reg-alert.md)

## Impact radius calculation

When you add impacted areas to regulatory alerts of type regulatory event, assign it to a user, and the user marks the alert as applicable, regulatory tasks are automatically generated. The regulatory tasks are then assigned to a user. When the assigned user of the tasks chooses to respond to the tasks, action tasks for each impacted areas are generated. However, you can also manually add more action tasks, other than the ones that are automatically created based on the impacted areas.

## Representation of regulatory changes in the Compliance Workspace

The Compliance Workspace is updated to display the regulatory changes by impacted areas. The following figure displays the regulatory changes section under the Tracking widget.

![The figure shows the link to the Regulatory change management dashboard and the regulatory change tasks.](../../grc-rcm-workspace/image/compliance-workspace-reg-changes.png "Regulatory changes on the Compliance workspace")

