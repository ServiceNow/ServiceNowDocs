---
title: Organizational plugins for Strategic Portfolio Management
description: Strategic Portfolio Management offerings help you better manage demand, balance resources, manage agile and waterfall projects, perform budget planning, and map costs to technical and business services.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Strategic Portfolio Management]
---

# Organizational plugins for Strategic Portfolio Management

Strategic Portfolio Management offerings help you better manage demand, balance resources, manage agile and waterfall projects, perform budget planning, and map costs to technical and business services.

## Plugins at the organization level

-   **Organization Extension \(com.snc.organization\_extension\) plugin**

    Organization Extension \(com.snc.organization\_extension\) plugin activates Goals, Business unit, Enterprise strategy, and Business unit strategy entities. It is available on zBoot to all customers with demo data.

    Business Units, Goals, Enterprise Strategy, and Business Unit Strategy modules are available in the Organization application menu.

    Business Applications and Business Capabilities modules are also available within the Organization application menu, however, their related tables are moved to Configuration Management \(CMDB\) \(com.snc.cmdb\) plugin, which is available on zBoot but without demo data.

-   **Business Stakeholder \(com.snc.business\_stakeholder\) plugin**

    Business Stakeholder \(com.snc.business\_stakeholder\) plugin is activated at the SPM business unit level and contains business stakeholder read-only role \(child\) plugins at SPM product levels. Activating the child plugins at the product level enables the read-only access role at the respective product level. Users with this role can view and approve reports at their product level. Following are the child plugins activated at the product levels:


<table id="table_xtn_ky1_rhb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Read only roles for PPM Standard \(com.snc.pmo\_read\_roles\) plugin

</td><td>

-   The plugin provides the Read only roles for Financial Management \(sn\_itfm\_read\). Users with this role can access Financial Management dashboards. For more information on the list of dashboards and the levels of accessibility on the underlying tables, see [Read only roles for Financial Management](../../it-finance/reference/user-roles-fm-apm.md).
-   The plugin provides the Read only roles for Project Portfolio Management \(PPM\) and Timecard \(sn\_ppm\_read\). Users with this role can access Portfolio, Program, and Timecard dashboards along with the Resources report. For more information on the list of dashboards and the levels of accessibility on the underlying tables, see [Read only roles for PPM](../../project-portfolio-suite-with-financials/reference/business-stakeholder-role-ppm.md).

</td></tr><tr><td>

Read only roles for Agile 2.0 \(com.snc.agile\_read\_roles\) plugin

</td><td>

The plugin provides a Read only role for Agile Development 2.0, Scrum Programs, and Performance Analytics Content Pack for Agile 2.0 applications. A user with this role can read and retrieve data from these applications and generate reports and dashboards. For information on plugin availability and data access, see [Business stakeholder role for Agile 2.0](../../agile-development/reference/business-stakeholder-role-agile-dev-2-0.md).

</td></tr><tr><td>

Read only roles for SAFe \(com.snc.safe\_read\_roles\) plugin

</td><td>

The plugin provides a Read only role for Essential SAFe, Portfolio SAFe, and Performance Analytics Content Pack for Essential SAFe. A user with this role can read and retrieve data from these applications and generate reports and dashboards. For information on plugin availability and data access, see [Business stakeholder role for SAFe](../../agile-SAFe/reference/business-stakeholder-role-for-essential-safe-and-portfolio-safe.md).

</td></tr><tr><td>

Read only roles for Test Management 1.0 \(com.snc.tm1\_read\_roles\) plugin

</td><td>

The plugin provides a Read only role for Test Management 1.0. A user with this role can read and retrieve data from these applications and generate reports and dashboards. For information on plugin availability and data access, see [Business stakeholder role for Test Management 1.0](../../test-management/reference/business-stakeholder-role-tm-1.md).

</td></tr><tr><td>

Read only roles for Test Management 2.0 \(com.snc.tm2\_read\_roles\) plugin

</td><td>

The plugin provides a Read only role for Test Management 2.0. A user with this role can read and retrieve data from these applications and generate reports and dashboards. For information on plugin availability and data access, see [Business stakeholder role for Test Management 2.0](../../test-management2/reference/business-stakeholder-role-test-mgmt2.md).

</td></tr></tbody>
</table>