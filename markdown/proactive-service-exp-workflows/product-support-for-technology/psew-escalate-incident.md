---
title: About escalating incidents
description: An escalation can be triggered when an incident is created with the appropriate category and sub category and the Escalate UI option is triggered within the Service Operations Workspace.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# About escalating incidents

An escalation can be triggered when an incident is created with the appropriate category and sub category and the **Escalate UI** option is triggered within the Service Operations Workspace.

The following diagram provides a visual representation of the escalation flow.

![Escalation flow](../image/psew-incident-escalate-flow.png)

The following category and sub category values are available with the base system:

-   Category: SD-WAN
-   Sub category:
    -   Link failure
    -   Device failure
    -   Protocol failure
    -   Soft-WAN link failure
    -   Software failure

The following values are available for the Stage field in the Incident table:

-   Triage
-   L1 investigation
-   L2 investigation
-   L3 investigation

Based on the defined conditions, such as current stage, category, and sub-category, the Incident Escalation Policy decision table determines the results and the next escalation stage if appropriate.

![Incident Escalation Policy decision table to configure incident escalation results in Service Operations Workspace](../image/psew-incident-dec-table.png)

The decision table is provided with the Proactive Service Experience Workflows application. You can modify the conditions that have been defined, and the results to suit your requirements. For more details on updating decision tables, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=australia&pubname=australia-application-development&ft:locale=en-US).

When an incident is escalated, the status of the Needs attention field is updated to **True**. The status can be changed to **False** by the owner of the Assignment Group field.

**Note:** As a system administrator, you can configure the **Set Needs Attention False** business rule.

-   **[Escalate an incident in Proactive Service Experience Workflows](../task/escalate-incident-aw.md)**  
Escalate an incident to continue the investigation and diagnosis of that incident. By escalating an incident, you can ask for help from a more-experienced resource so that the issue is resolved more quickly.

**Parent Topic:**[Using Proactive Service Experience Workflows](use-assurance-workflows.md)

