---
title: Recommendation Framework in Service Operations Workspace
description: An agent can view dynamic and contextual recommendations and perform a relevant action.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Recommendation Framework in Service Operations Workspace

An agent can view dynamic and contextual recommendations and perform a relevant action.

Recommendation Framework is now deprecated and no longer supported or available for new activation. Recommended Actions for ITSM feature provides the latest experience for this functionality. To get the advanced version, you must install the Advanced Recommended actions for ITSM \(com.snc.uib.sow\_itsm\_ra\_advanced\) plugin and you must procure ITSM Pro package subscription.

**Note:** The best practice to get the advanced version is to install the Task Intelligence for ITSM \(com.snc.itsm\_ml\_task\) plugin and procure the ITSM Pro package subscription. For more information, see [Exploring Recommended Actions for ITSM in Service Operations Workspace](exploring-recommended-actions-for-itsm-in-service-operations-workspace.md).

Recommendations are available in multiple areas for an incident in Service Operations Workspace.

## Recommendations from the sidebar for an incident

From the sidebar of an incident, you can access the **Recommendations** panel where you can configure and group recommendations in any of the following formats.

-   Record card: Relevant record details of a table and corresponding actions are available.
-   Message card: A message derived from the recommendation and corresponding actions is available. For example, **Propose major incident** card.

**Note:** All cards of the same recommendation rule are grouped. For example, for the Similar open incidents rule for an incident in Service Operations Workspace, all relevant incidents are grouped as cards under **Similar open incidents**.

![Recommendations from the sidebar](../../recommendation-framework/image/recommendation-panel.png "Recommendations from the sidebar")

For information on available card groups for an incident and their dependencies on recommendation rules, see [Recommendation rules for an incident in Service Operations Workspace](../reference/recommendation-rules.md).

When you click a card or its record number, detailed information about that card and its actions is displayed in a new tab.

Every card has a primary action and multiple other actions. For every action you perform on the card, the recommendations are recomputed. You can discard a recommendation if not relevant. Also, when you perform a primary action on a card, it moves from the **Current** tab to the **History** tab.

**Note:** Based on the priority, the first card of the top card group is displayed as the top recommendation at the top of the **Recommendations** panel.

## Recommendations at the field level for an incident

A predicted value is displayed for these fields in the **Details** tab of an incident.

-   Assignment group
-   Configuration item
-   Service

These values are predicted based on a recommendation rule for each field. For information about these rules, see [Recommendation rules for an incident in Service Operations Workspace](../reference/recommendation-rules.md). When a threshold value is configured, the recommended value can be stamped or auto-populated as the field value. For information about this configuration, see [Configure Recommendation Framework for an incident in Service Operations Workspace](../task/configure-rf-properties.md).

![Recommendations at field level](../../recommendation-framework/image/field-recommendation.png "Recommendations at field level")

-   **[Recommendation rules for an incident in Service Operations Workspace](../reference/recommendation-rules.md)**  
Recommendations for an incident are based on rules defined in Recommendation Framework.

**Parent Topic:**[Managing IT services in your organization](managing-services-operations-in-organization.md)

**Related topics**  


[Knowledge Management in Service Operations Workspace](knowledge-articles-sow.md)

[Major Incident Management in Service Operations Workspace](mim-in-sow.md)

[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)

[Problem Management in Service Operations Workspace](problem-sow.md)

[Recommended Actions for ITSM in Service Operations Workspace](recommended-actions-for-itsm-in-service-operations-workspace.md)

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace](msteams-sow.md)

[Service Level Management in Service Operations Workspace](slm-sow.md#)

[Walk-up Experience management in Service Operations Workspace](walkup-sow.md)

[Collaboration in Service Operations Workspace](collaboration-sow.md)

[Computer Telephony Integration in Service Operations Workspace](configure-cti-sow.md)

[Universal Request in Service Operations Workspace](using-ur-sow.md)

[Universal Task in Service Operations Workspace](using-ut-sow.md)

[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace](resetting-password-pr-sow.md)

