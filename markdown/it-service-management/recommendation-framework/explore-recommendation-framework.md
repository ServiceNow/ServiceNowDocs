---
title: Exploring Recommendation Framework
description: A reusable framework to deliver outcome-based recommendations for a user in a configurable workspace.
locale: en-US
release: yokohama
product: Recommendation Framework
classification: recommendation-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Recommendation Framework, IT Service Management]
---

# Exploring Recommendation Framework

A reusable framework to deliver outcome-based recommendations for a user in a configurable workspace.

Recommendations are available in multiple areas of a configurable workspace.

## Recommendations in a contextual panel

You can configure recommendations in a contextual panel, for example, the **Recommendations** panel that can be accessed from the sidebar of an incident in Service Operations Workspace. Recommendations can be configured and grouped in any of the following formats.

-   Record card: Relevant record details of a table and corresponding actions are available.
-   Message card: A message derived from the recommendation and corresponding actions are available. For example, **Propose major incident** card for an incident in Service Operations Workspace.

**Note:** All cards of the same recommendation rule are grouped. For example, for the Similar open incidents rule for an incident in Service Operations Workspace, all relevant incidents are grouped as cards under **Similar open incidents**.

![Recommendations from sidebar](../image/recommendation-panel.png "Recommendations from the sidebar")

For information on available card groups and their dependencies on recommendation rules, see [Recommendation rules for an incident in Service Operations Workspace](../../service-operations-workspace/reference/recommendation-rules.md).

When you click a card or its record number, detailed information about that card and its actions are displayed in a new tab.

Every card has a primary action and multiple other actions. For every action you perform on the card, the recommendations are recomputed. You can discard a recommendation if not relevant. Also, when you perform a primary action on a card, it moves from the **Current** tab to the **History** tab.

**Note:** Based on the priority, the first card of the top card group is displayed as the top recommendation at the top of the **Recommendations** panel.

## Recommendations at the field level

A predicted value is displayed at the field level based on the corresponding recommendation rule. For information about these rules for an incident, see [Recommendation rules for an incident in Service Operations Workspace](../../service-operations-workspace/reference/recommendation-rules.md). When a threshold value is configured, the recommended value can be stamped or auto-populated as the field value. For information about these configurations for an incident, see [Configure Recommendation Framework for an incident in Service Operations Workspace](../../service-operations-workspace/task/configure-rf-properties.md).

![Recommendations at field level](../image/field-recommendation.png "Recommendations at field level")

**Parent Topic:**[Recommendation Framework](recommendation-framework-landing-page.md)

