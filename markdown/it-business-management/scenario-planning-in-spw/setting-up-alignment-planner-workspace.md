---
title: Configuring Strategic Planning Workspace
description: Learn about the process required to set up Strategic Planning to enable your product and portfolio managers start aligning their work with business goals and strategy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/setting-up-alignment-planner-workspace.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configuring Strategic Planning Workspace

Learn about the process required to set up Strategic Planning to enable your product and portfolio managers start aligning their work with business goals and strategy.

## Configuration workflow

Use the following steps as guidelines to set up Strategic Planning. Some of these steps require the admin role and some require the sn\_align\_core.apw\_admin role.

1.  [Install Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/install-alignment-planner-workspace.md).
2.  Assign user roles.

    See the Roles installed table in [Components installed with Strategic Planning Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/components-installed-with-alignment-planner-workspace.md).

    **Note:** If you are upgrading from an older version to Strategic Planning v2.1.0 or higher, a fix script is run to remove the milestone\_editor role from the roadmap\_editor role because the roadmap\_editor role is no longer used. In this case, you may experience a longer time for the upgrade to complete if your ServiceNow instance has a large number of users with the roadmap\_editor role. For more information, see [KB1443618](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1443618).

3.  Configure lenses to enable your planning managers to create portfolio plans.

    See [Lens configuration in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/configuring-lens-in-alignment-planner-workspace.md).

4.  Enable high-level planning for tables that are not enabled by default.

    See [High-level planning configuration in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/high-level-portfolio-planning-configuration.md).

5.  Validate your configuration for lens, planning items, portfolio plans, high-level planning, and others.

    See [Strategic Planning diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/strategic-planning-diagnostics.md).

6.  Configure Prioritization and Roadmap display settings.

    See [Prioritization display settings in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/configuring-prioritization-and-roadmap-settings-strategic-planning.md).

7.  Configure Feedback and manage your feedback and product ideas. See [Configuring Feedback application in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/product-feedback/configuring-product-feedback-in-sp.md).
8.  Integrate Strategic Planning with a ServiceNow® execution system of your choice. This integration enables you to plan in Strategic Planning and execute in your chosen app.

    See [Configuring Strategic Planning with PPM, Agile 2.0, and SAFe](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/configuring-apw-with-agile-safe-and-ppm.md) and [Configuring Feedback application in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/product-feedback/configuring-product-feedback-in-sp.md).

9.  Migrate your existing goals to Strategic Planning and configure goal preferences.

    See [Configuring goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/configuring-goal-framework-apw.md).

10. Configure Capacity Planning and generate resource capacity.

    See [Capacity configuration in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/config-cp-spw.md).

11. Enable financial planning for epics and customise the Financials screen view.

    See [Configure financials for planning items Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/config-fin-spw.md).


## Guided Setup to configure Strategic Planning

Guided Setup provides a sequence of tasks to help you with the required configuration on your ServiceNow instances. After [installing Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/install-alignment-planner-workspace.md), navigate to **All** &gt; **Strategic Planning** &gt; **Guided Setup**.

When you’re configuring a task from the Guided Setup, you can launch the in-app help for additional guidance by clicking the Show Help icon \(\[Omitted image "Banner\_HelpIcon.png"\] Alt text: Show Help.\).

