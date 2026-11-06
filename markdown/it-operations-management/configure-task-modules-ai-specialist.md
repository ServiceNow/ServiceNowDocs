---
title: Configure task modules for the AIOps AI Specialist
description: Enable and configure the AI Specialist's capabilities by activating the Deflect, Investigate, and Remediate modules that control what the AI Specialist does when it receives an alert.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/configure-task-modules-ai-specialist.html
release: australia
topic_type: task
last_updated: "2026-11-01"
reading_time_minutes: 2
keywords: [task modules, AI specialist, deflect, investigate, remediate, configure]
breadcrumb: [Onboard the AIOps specialist, AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# Configure task modules for the AIOps AI Specialist

Enable and configure the AI Specialist's capabilities by activating the Deflect, Investigate, and Remediate modules that control what the AI Specialist does when it receives an alert.

## Before you begin

Very you have the following setting

-   Platform version Brazil Patch 2 or later.
-   ServiceNow Otto for IT Operations Management \(ITOM\) application, version 2.10.0 or later.
-   AIOps Experience application, version 27.2.68 or later.
-   AIOps AI Specialist \(sn\_ai\_aiops\_force\) plugin, version 3.0.0 or later.

For the Remediate module, confirm that your instance has available automations enabled as alert management rules.

Role required: evt\_mgmt\_admin or evt\_aiops\_manager

## Procedure

1.  Configure the Noise reduction module.

    1.  In the **Tasks** tab, select the **Noise reduction** task module.

        \[Omitted image "ai-specialist-deflect.png"\] Alt text: Enable auto-close

    2.  Enable **Auto-close insignificant alerts**.

        **Note:** Noise reduction accuracy improves over time as the AI processes more alerts in your environment. In the first days of operation, monitor the [AI supervising](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/ai-supervisor-in-itom-aiops.md) tab to confirm the AI is deflecting the right alerts.

2.  Configure the Investigate module.

    1.  In the **Tasks** tab, select the **Investigation** task module.

    2.  Enable **Root Cause Analysis** if you want the AI Specialist to search for related alerts and changes that explain the alert.

    3.  Enable **Impact Analysis** if you want the AI to assess which services and business services are affected.

    4.  Under **Knowledge Sources**, select the knowledge bases you want the AI Specialist to reference during investigation.

        Including relevant knowledge sources improves the quality of the AI's probable cause assessment. Select the sources your operators already use for alert investigation.

    5.  Select **Save**.

3.  Configure the Remediate module.

    1.  In the **Tasks** tab, select the **Remediation** task module.

        \[Omitted image "ai-specialist-remediation.png"\] Alt text: Remediation action to resolve alerts.

    2.  Enable **Suggest remediation** if you want the AI Specialist to recommend a remediation action to resolve an alert.

        Remediate searches existing KB articles for available automation and suggests the best possible remediation actions that the user can execute.

    3.  Select **Save**.


## Example

**Tip:** A team new to AI Specialists starts with only Investigate enabled, with root cause and impact analysis on, and Noise Reduction and Remediate off. After two weeks, they review the AI's findings, confirm accuracy, and then enable Noise Reduction. Once they validate automation in an KB, they enable Remediate. This phased approach builds team confidence before expanding AI autonomy.

## What to do next

After configuring task modules, test the AI Specialist with a real alert. See [Test and activate the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/test-activate-ai-specialist.md).

**Parent Topic:**[Onboard the AIOps specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/onboard-ai-specialist.md)

