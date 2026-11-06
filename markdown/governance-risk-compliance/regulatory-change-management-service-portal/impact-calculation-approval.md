---
title: Impact radius for regulatory alerts of type regulatory event
description: Impact radius typically refers to the extent to which a regulatory change affects an organization. Adding impacted areas to a regulatory alert of type regulatory event helps to calculate the impact radius of a regulatory alert.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/regulatory-change-management-service-portal/impact-calculation-approval.html
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Impact radius for regulatory alerts of type regulatory event

Impact radius typically refers to the extent to which a regulatory change affects an organization. Adding impacted areas to a regulatory alert of type regulatory event helps to calculate the impact radius of a regulatory alert.

## Impacted areas

Assess regulatory events that could affect the compliance or risk posture of your organization. The impact radius measures how a regulatory event affects GRC objects and identifies action tasks. The Regulatory Change Management application supports impact radius calculation for regulatory alerts and automatically creates action tasks.

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

**Note:** Impacted areas can be added to regulatory alerts that are of type regulatory event. For more information, see [Add impacted areas manually to a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/regulatory-change-management-service-portal/add-impacted-area-reg-alert.md)

## Impact radius calculation

Add impacted areas to a regulatory alert of type regulatory event and assign it to a user. When the user marks the alert as applicable, regulatory tasks are automatically generated and assigned to a user. When the assigned user responds to the tasks, action tasks are generated for each impacted area. You can also manually add action tasks beyond those automatically created from the impacted areas.

## Representation of regulatory changes in the Compliance Workspace

The Compliance Workspace is updated to display the regulatory changes by impacted areas. The following figure displays the regulatory changes section under the Tracking widget.

\[Omitted image "compliance-workspace-reg-changes.png"\] Alt text: The figure shows the link to the Regulatory change management dashboard and the regulatory change tasks.

