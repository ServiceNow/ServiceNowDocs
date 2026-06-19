---
title: Invoke the MatchingRuleProcessor API
description: After you create one or more matching rules, you can invoke the MatchingRuleProcessor API and run the rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/t\_InvokeMatchingRuleAPI.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure case routing and assignment, Route and assign cases, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
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


