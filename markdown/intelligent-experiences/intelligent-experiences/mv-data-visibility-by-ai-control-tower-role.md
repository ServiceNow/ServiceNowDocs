---
title: Role based data visibility
description: The AI Control Tower shows value, engagement, and cost data for the AI systems in a user’s scope. AI stewards can view data for all AI systems in an instance. Product owners can view data only for the AI systems that they manage.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Role based data visibility

The AI Control Tower shows value, engagement, and cost data for the AI systems in a user’s scope. AI stewards can view data for all AI systems in an instance. Product owners can view data only for the AI systems that they manage.

AI Control Tower supports two responsibility levels. AI stewards oversee AI systems at the instance level. Product owners oversee individual AI systems.

To access AI Control Tower, users must have either the AI steward role \(`sn_ai_governance_ai_steward`\) or the product owner \(`sn_ai_governance_ai_asset_owner`\) role. Users without one of these roles can’t access the application.

## Data scope for each role

Data scope is based on the **Managed by** field on the AI system record. If the **Managed by** field lists a user, that AI system is in the user’s scope. AI Control Tower filters value, engagement, and cost data to that scope.

A product owner’s scope is always a subset of an AI steward’s scope. For example, an AI steward might see all AI systems in the instance, while a product owner sees only the AI systems that they manage.

Only deployed AI systems are included in calculations. Retired AI systems and AI systems in other states are excluded. As a result, the number of AI systems shown in a chart can be lower than the number of AI systems in the user’s scope.

If a product owner doesn’t manage any AI systems, AI Control Tower shows zero values and empty widgets.

## Why access differs

A product owner has detailed knowledge of the AI systems that they manage and can adjust how those AI systems are measured. Instance-level decisions stay with the AI steward, so a product owner can't change settings that affect AI systems outside their scope.

Cost configuration is defined at the vendor level. Changes to vendor configuration affect every AI system mapped to that vendor, including AI systems outside a product owner’s scope. For this reason, cost configuration is read-only for product owners.

## When product owners use scoped data

Product owners use scoped data to review value and engagement results, map AI systems to value templates, and review cost output for the vendors behind their AI systems.

**Related topics**  


[Feature access by role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mv-feature-access-by-role.md)

[Review AI system value and engagement data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/review-ai-system-value-and-engagement-data.md)

