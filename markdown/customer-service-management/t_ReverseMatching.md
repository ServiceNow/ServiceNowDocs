---
title: Reverse matching
description: Reverse matching uses the same matching rules to match tasks to a resource rather than resources to a task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/t\_ReverseMatching.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure case routing and assignment, Route and assign cases, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Reverse matching

Reverse matching uses the same matching rules to match tasks to a resource rather than resources to a task.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager, and admin

## About this task

The resource matching engine can match resources and tasks in two ways:

-   Forward: matches resources for a task
-   Reverse: matches tasks for a resource

The same matching rule can be used for both forward and reverse matching.

## Procedure

-   In the Customer Service Management application, you can use reverse matching to determine which call the next available agent should take.

-   Reverse matching returns a list of case sys\_ids instead of user sys\_ids.

    When using reverse matching, you can also limit the cases returned to a specific set. The following example shows how to use reverse matching.

    ```
    MatchingRuleProcessor.processAndGetCandidates(resource, taskLimit, "sn_customerservice_case", "reverse", false, [<array of cases to consider>])
    ```


