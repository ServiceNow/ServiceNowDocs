---
title: Enterprise-Wide Deployment for demands
description: Enterprise-Wide Deployment \(EWD\) partitions demand data by criteria such as department. Demand experiences extends that by controlling each demand's fields, modules, and layout.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/ewd-for-demands-dw.html
release: brazil
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 4
breadcrumb: [Explore, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Enterprise-Wide Deployment for demands

Enterprise-Wide Deployment \(EWD\) partitions demand data by criteria such as department. Demand experiences extends that by controlling each demand's fields, modules, and layout.

Demands support EWD in two complementary ways: partitioning, which controls who can see a demand, and demand experiences, which control what a demand looks like to users who can see it. For the full EWD concept, including partitions for other SPM tables, see [Exploring SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/explore-ewd.md).

Partitions and demand experiences are two independent, complementary layers, and the boundary between them is deliberate: partitions control who can see a demand and its dashboards; demand experiences control what a demand looks like and how it's navigated once you can see it. Partitions don't determine the record view, form fields, related lists, modules, or record tabs. Those are all controlled by the demand experience field.

## Partitioning demands

The Demand \[dmn\_demand\] table is one of the tables EWD supports for partitioning. Partitioning also applies to demand-related tables, such as demand tasks, cost plans, and resource assignments. For more information, see [Supported tables for partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/supported-tables-for-partition-ewd.md).

An administrator defines a partition criteria field on the Demand table, such as **Department**, and creates a partition for each value, such as **IT Operations** or **Finance**. When a demand is created, it's automatically stamped with the partition that matches its criteria field. A user then sees only the demands that belong to a partition their role grants them access to, across Strategic Planning Workspace, list views, search results, and dashboards.

An administrator can also configure a unique default dashboard for each partition; a user sees the default dashboard for their own partition automatically when they log in. For more information, see [Map a dashboard to a partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/map-dashboard-to-partition-ewd.md).

## Demand experiences

A demand experience controls the fields, modules, and layout a demand shows for a given governance process, such as Marketing or IT. See [Demand experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/demand-experiences-dw.md) for how a demand experience is structured, including form view precedence when more than one view rule applies, and [Create a demand experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-a-demand-experience-dw.md) for how to create one.

The following demand-record behaviors depend on a demand's experience:

-   Modules available for a given demand experience
-   Form layout for a given demand experience
-   Dynamic fields when a demand experience has a dynamic category with configured dynamic attributes

When a demand experience includes dynamic fields, the demand record displays an **Additional Information** tab that shows those fields. The Enterprise-Wide Deployment application \(`sn_spm_ewd`\) must be installed for the **Additional Information** tab to appear.

## Personas

|Role|Function|
|----|--------|
|EWD admin role \[sn\_spm\_ewd.ewd\_admin\]|Creates and configures partitions for the Demand table, including the partition criteria field and the role assigned to each partition.|
|System admin role \[sys\_admin\]|Creates dynamic categories from SPM Dynamic Categories.|
|PPS admin role \[pps\_admin\]|Creates and manages demand experiences: selects the table, form view, optional dynamic category, and which modules are enabled.|
|EWD PMO role \[sn\_spm\_ewd.ewd\_pmo\]|Views demands across all partitions, regardless of partition role assignment.|
|Demand user role \[it\_demand\_user\]|Creates and views demands in the partitions that their role grants access to. Doesn't administer experiences or dynamic categories. On a demand record, sees the modules enabled for that demand's experience and, when applicable, the **Additional Information** tab with its dynamic fields.|

## Demand data visibility

When EWD and demand experiences are both configured, a demand user sees:

-   Only demands that belong to their assigned partitions in list views, search results, and dashboards, with no indication that demands in other partitions exist.
-   A drop-down list of available views in the menu panel, when the user has access to more than one partition.
-   Only the modules on a demand that are enabled for that demand's experience.
-   An **Additional Information** tab on the demand record, only when the demand's experience has a dynamic category with configured dynamic attributes.

**Related topics**  


[Demand experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/demand-experiences-dw.md)

[Create a demand experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-a-demand-experience-dw.md)

[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-demand-from-dw.md)

[SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/ewd-landing-page.md)

