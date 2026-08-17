---
title: ServiceNow Otto: UI policy functions
description: ServiceNow Otto can generate UI policies with multiple actions from simple natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/now-assist-ui-policy-functions.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [AI Authoring for Catalog Builder reference, AI Authoring for Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# ServiceNow Otto: UI policy functions

ServiceNow Otto can generate UI policies with multiple actions from simple natural language.

## What you can do with UI Policies using ServiceNow Otto

As a Catalog Builder editor, you can use ServiceNow Otto to create new UI policies, update existing ones, and deactivate them, all through simple, conversational prompts. Each UI policy can include multiple actions, and ServiceNow Otto can create that for you.

## Making targeted changes

You don't have to recreate a UI policy from scratch every time you need to tweak something. ServiceNow Otto lets you make specific, focused changes to an existing UI policy, such as updating its name or description, changing the conditions that trigger the policy, and adding, modifying, or removing individual actions within the policy.

## Managing UI policy actions

UI policy actions are the individual rules that tell the system what to do when the policy's conditions are met, for example, making a field mandatory or hiding a variable. You can add new actions, update existing ones, or delete actions you no longer need, all through ServiceNow Otto.

## Confirmation after every change

After ServiceNow Otto generates or updates a UI policy, it will send you a confirmation message letting you know what was done and prompting you to review the behavior. This gives you a chance to verify the output before moving on.

## Multiple actions in a single instruction create one UI policy

If a user provides multiple condition–action statements in one message. For example: “If RAM is 8GB, set storage to 2TB and set color to red.” The ServiceNow Otto creates one UI Policy with:

-   Condition: RAM = 8GB
-   Actions: storage = 2TB, color = red

## Adding to an existing UI policy

-   If you give ServiceNow Otto a new instruction that uses the same condition as a UI policy that was already created, the system doesn't create a duplicate. Instead, it adds the new action to the existing UI policy.
-   For example, if you previously said "If RAM is 8GB, set storage to 2TB" and later say "If RAM is 8GB, set color to red", ServiceNow Otto recognizes that both instructions share the same condition and simply adds the new action to the existing policy rather than creating a separate one.

## Using conversational cues to group actions

ServiceNow Otto also picks up on natural conversational phrases to understand when you want to keep adding to the same policy. If you use phrases like "also", "add one more thing", or "add to the same policy", the system treats your new instruction as an addition to the UI policy that is currently being worked on.

## Creating a new UI policy for a different condition

-   If your instruction involves a condition that is different from any existing UI policy, ServiceNow Otto automatically creates a new, separate UI policy for it.
-   For example, if you say "If RAM is 16GB, hide the processor field" and no policy with that condition exists yet, a new UI policy is created specifically for that condition.

## What happens when there is a conflict

If a new instruction contradicts an existing UI policy, for example, one policy says "If RAM is 8GB, set color to red" and you now ask it to "set color to blue" under the same condition, ServiceNow Otto flags the conflict rather than overwriting silently. It will ask you to confirm how you want to proceed, for example: "There is an existing UI policy with a conflicting action for this condition. Do you still want to proceed with creating this action?" This ensures that changes are always intentional and nothing gets overwritten by mistake.

**Parent Topic:**[AI Authoring for Catalog Builder reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-item-generation-reference.md)

