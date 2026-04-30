---
title: Invoke the MatchingRuleProcessor API
description: After you create one or more matching rules, you can invoke the MatchingRuleProcessor API and run the rules.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Route and assign cases, Administer, Customer Service Management]
---

# Invoke the MatchingRuleProcessor API

After you create one or more matching rules, you can invoke the MatchingRuleProcessor API and run the rules.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager, admin

## Procedure

-   You can invoke the matching engine using the processAndGetCandidates method of the matchingRuleProcessor class.

    Pass in the task record and the number of resources. The result is an array of resource sys\_ids.

-   The system processes the matching rules based on the number stored in the **Execution Order** field for each rule.

    The result is a list of users \(sys\_ids\), which you can use for case routing and assignment.


**Parent Topic:**[Routing and assigning customer service cases](../concept/c_CaseRouting.md)

