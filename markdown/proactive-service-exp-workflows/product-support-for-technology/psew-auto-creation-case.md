---
title: Auto-creation of cases and updates from incidents
description: Cases are created from the incidents.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# Auto-creation of cases and updates from incidents

Cases are created from the incidents.

A case is designated as a major case based on the value specified in the `major_case_affected_account_threshold` system property. This value can be modified by the administrator.

For more information to generate proactive cases, see [Redirection to the right case type](../task/generate-proactive-cases.md).

Depending on the threshold value, different flows are triggered to either create one major incident, or several individual cases. The case record is then populated. For example, in minor case scenarios, the following information is populated:

-   Short description
-   Description
-   Proactive is true
-   Channel
-   Incident
-   Account field

The administrator can specify the fields that must be passed to the case records from the parent incident record to suit their business needs.

-   **[Setting major case threshold for auto generated cases](../task/psew-set-major-case-threshold.md)**  
Set the threshold value for major cases generated from incidents in the system properties.
-   **[Redirection to the right case type](../task/generate-proactive-cases.md)**  
Create a proactive case from an incident in the Proactive Service Experience Workflows.

**Parent Topic:**[Using Proactive Service Experience Workflows](use-assurance-workflows.md)

