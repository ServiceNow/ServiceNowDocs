---
title: Configuring Portfolio Planning
description: Learn about the process required to set up Portfolio Planning to enable your product and portfolio managers start aligning their work business objectives.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Portfolio Planning, Strategic Portfolio Management]
---

# Configuring Portfolio Planning

Learn about the process required to set up Portfolio Planning to enable your product and portfolio managers start aligning their work business objectives.

## Configuration workflow

Use the following steps as guidelines to set up Portfolio Planning. Some of these steps require the admin role and some require the sn\_align\_core.apw\_admin role.

1.  [Install Portfolio Planning](../task/install-portfolio-planning.md).
2.  Assign user roles.

    See the Roles installed table in [Components installed with Portfolio Planning](../reference/installed-with-portfolio-planning.md).

    **Note:** If you are upgrading from an older version to Portfolio Planning v6.1.1 or higher, a fix script is run to remove the milestone\_editor role from the roadmap\_editor role because the roadmap\_editor role is no longer used. In this case, you may experience a longer time for the upgrade to complete if your ServiceNow instance has a large number of users with the roadmap\_editor role. For more information, see [KB1443618](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1443618).

3.  Configure lenses to enable portfolio plans.

    See [Configuring lens in Portfolio Planning](configuring-lens-in-portfolio-planning.md).

4.  Integrate ServiceNow® Portfolio Planning with Project Portfolio Management \(PPM\).

    See [Portfolio Planning with Project Portfolio Management](portfolio-planning-integration-with-execution-applications.md).

5.  Configure Capacity Planning and generate resource capacity.

    See [Capacity configuration in Portfolio Planning](config-cp-pp.md).

6.  Enable financial planning for epics and customise the Financials screen view.

    See [Configure financials for planning items in Portfolio Planning](../task/config-fin-pp.md).


## Guided Setup to configure Portfolio Planning

Guided Setup provides a sequence of tasks to help you with the required configuration on your ServiceNow instances. After installing Portfolio Planning, navigate to **All** &gt; **** &gt; **Portfolio Planning** &gt; **Guided Setup**.

When you’re configuring a task from the Guided Setup, you can launch the in-app help for additional guidance by clicking the Show Help icon \(![Show Help.](../../alignment-planner-workspace/images/help-icon.png)\).

