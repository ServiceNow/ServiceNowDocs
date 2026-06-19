---
title: Configure the business continuity plan template
description: Configure the business continuity plan template in the Business Continuity Management application for your business. You can use the plan template to recover a specific primary element such as Employees or Web Servers. Similarly, you can create a plan template for different plan authoring types such as documentation, loss scenarios, and recovery tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/configure-a-bcp-template-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring plan template, Setup for a BCP, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure the business continuity plan template

Configure the business continuity plan template in the Business Continuity Management application for your business. You can use the plan template to recover a specific primary element such as Employees or Web Servers. Similarly, you can create a plan template for different plan authoring types such as documentation, loss scenarios, and recovery tasks.

## Before you begin

Role required: sn\_bcm.admin

## About this task

The sn\_bcm.admin role contains the sn\_bcp.plan\_admin role. The sn\_bcm.admin role is necessary to view the **Plan Templates** menu. The BCM administrator can navigate to the **Plan Templates** menu and then the plan administrator can update the plan templates.

By configuring the plan template, you can:

-   Define the primary object type that has to be recovered.
-   Define documentation sections that should be included right at the beginning of a plan.
-   Identify the loss scenarios and plan accordingly using the template.

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **Plan Configuration** &gt; **Plan Templates**.

2.  Select **New**.

3.  On the Plan Template form, fill in the fields.

    For more information on the fields, see [Plan Template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/plan-template-form.md).

    **Note:** The synchronization fields are:

    -   Plan scope asset synchronization: auto-sync scope assets to loss scenario dependencies based on element definition
    -   Synchronize loss scenario assets with recovery strategy assets: keeps loss scenario asset lists aligned with recovery strategies
4.  Configure asset synchronization between the plan scope, loss scenarios, and recovery strategies using the template's synchronization options.

5.  On the **Task template groups** and **Task templates** related lists, add the recovery task template groups and task templates that should be created automatically when a plan is created from this template.

    Templates that you add at the plan template level produce tasks on the plan record itself. To pre-populate tasks on a loss scenario or recovery strategy, open the corresponding loss scenario or recovery strategy nested inside the plan template and add the templates there.

    When a planner creates a plan from this template, the system creates documentation, loss scenarios, recovery strategies, and recovery tasks in a single operation. The progress tracker on the plan record shows the creation status.

    \[Omitted image "plan-template-with-task-templates.png"\] Alt text: Plan template showing Task template groups and Task templates related lists alongside Loss scenarios.

    \[Omitted image "plan-progress-tracker-from-template.png"\] Alt text: Plan record after creation from a template, with the progress tracker indicating that documentation, loss scenarios, and recovery tasks are being created.

6.  Select **Submit**.


-   **[Plan Template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/plan-template-form.md)**  
Use the Plan Template form in BCM UIB Workspace to input details regarding the business continuity plan.

**Parent Topic:**[Configuring plan template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-admin-plan-templates.md)

