---
title: Domain separation with Spotlight
description: If you have domain separation enabled, Spotlight applies it during Spotlight jobs.
locale: en-US
release: australia
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Domain separation with Spotlight

If you have domain separation enabled, Spotlight applies it during Spotlight jobs.

## Domain of the Spotlight group

When you create a Spotlight group, you create it in the domain of the user that you are logged in as when you create the group. For example, if you are a user in the ACME Products domain and you create a Spotlight group, that group is created in the ACME Products domain. If you create a Spotlight group as a user who is not a member of any domain, that Spotlight group is in the Global domain.

You can copy a Spotlight group to other domains, as defined in ServiceNow AI Platform® domain separation.

## Session domain and Spotlight group domain

If you are logged into a different domain than the domain of a Spotlight group, you cannot edit that Spotlight group record. In this case, you can only copy the Spotlight group to another domain.

## Spotlight criteria domains

-   When you create Spotlight criteria for a global Spotlight group, the criteria are created in the domain of the logged-in user.
-   When you create Spotlight criteria for a Spotlight group that is in a specific domain, the Spotlight criteria are created in that domain.

Messages inform you of the domain situation when you create Spotlight criteria.

## Evaluating scores with domain separation

If the Spotlight group evaluates platform data, the main indicator and all criteria are queried according to the domain and domain visibility of the **Run As** user. If the Spotlight group evaluates records from a snapshot, the main indicator and indicator-based criteria use the Performance Analytics [snapshot](performance-analytics-glossary.md#) that is collected specifically for the **Run As** user domain. The domain visibility of the **Run As** user does not apply to indicators in this case. \(Query-based criteria always evaluate platform data, even when the Spotlight group is configured to evaluate snapshots. Therefore, query-based criteria always follow both the domain and the domain visibility of the **Run As** user.\)

**Note:** The snapshot of each indicator can differ depending on the domain configuration of the Performance Analytics [data collection job](performance-analytics-glossary.md#) that creates the snapshot.

**Parent Topic:**[Ranking records with Spotlight](spotlight.md)

**Related topics**  


[Create a Spotlight group](../task/create-spotlight-group.md#)

[Evaluating a snapshot or platform data](../task/create-spotlight-group.md#)

[Copy a Spotlight group to domains](../task/copy-spotlight-group-domain.md)

[Domain separation and Performance Analytics](c_PAWithDomainSeparation.md)

