---
title: Task Active State Management business rule
description: The Task Active State Management business rule determines whether the active field value needs to change based on changes to the State field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/c\_TaskActiveStateMgmtBusRule.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Classic Business rules, Build workflows]
---

# Task Active State Management business rule

The Task Active State Management business rule determines whether the active field value needs to change based on changes to the **State** field.

The business rule is executed when the **State** is changed for a task record. Its execution order is 50, and it runs before most other task business rules.

If the current task table has the **close\_states** attribute defined on its table, or if it is inherited from a higher-level table, then the rule determines whether the active field needs to change. This is done by comparing the previous and current state values.

-   If the state changes from an active state to an inactive state, the **Active** field is set to false.
-   If the state changes from an inactive state to an active state, the **Active** field is set to true, effectively re-activating or re-opening the task.

It is recommended that you leverage the **\(current.active.changesTo\(\[true/false\]\)** action in your business rule, as opposed to creating rules on each task table that mark tasks as inactive or active.

**Parent Topic:**[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRules.md)

