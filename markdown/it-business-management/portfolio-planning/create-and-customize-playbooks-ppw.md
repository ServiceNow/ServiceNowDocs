---
title: Create and customize playbooks
description: Configure playbooks to customize demand workflows or create playbooks for your organization.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Create and customize playbooks

Configure playbooks to customize demand workflows or create playbooks for your organization.

## Before you begin

Role required: admin

## About this task

Next Experience for Demand Management includes two predefined playbooks available in Workflow Studio:

-   Demand default
-   AI playbook

    **Note:** The AI playbook is available only when the AI Control Tower plugin is installed and the investment type of the demand is set to artificial intelligence.


These playbooks are ready to use without any additional configuration. Configure playbooks only when you must customize an existing playbook or create one for your organization's specific demand workflows.

In Next Experience for Demand Management, playbooks are triggered by record creation. A playbook is associated with demand records, and the Playbook page appears in the L-2 \(level 2\) menu when a demand meets the trigger condition.

For more information on how to create or customize playbooks, see [Configuring Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/setting-up-process-automation-designer.md)

## Procedure

1.  Navigate to **Workflow Studio** &gt; **Playbooks**.

2.  To customize an existing playbook or create one, create and configure the playbook according to your requirement.

    -   To activate a predefined playbook, select the required playbook and define an appropriate trigger condition. For more information, see [Activate Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/activate-process-automation-designer.md) and [Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-triggers.md).
    -   To create a playbook, select **New**. For more information, see [Create and configure playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/setting-up-process-automation-designer.md).
    -   Multiple playbooks can be enabled at a time. Define trigger conditions so that each demand maps to only one playbook type. For more information, see [Create and configure playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/setting-up-process-automation-designer.md).

**Related topics**  


[Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/building-a-process.md)

[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-experience-admins.md)

[Playbooks in Next Experience for Demand Management](../concept/playbooks-in-demand-workspace-ppw.md)

[Use Playbooks](use-playbooks-in-ppw.md)

[Demand default playbook stages and activities](../reference/demand-default-playbook-stages-activities-ppw.md)

