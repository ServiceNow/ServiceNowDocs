---
title: UI policy functions
description: AI can generate UI policies with multiple actions from simple natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/now-assist-ui-policy-functions.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Things to know while creating items using AI, AI Authoring for Catalog Builder reference, AI Authoring for Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# UI policy functions

AI can generate UI policies with multiple actions from simple natural language.

## What you can do with UI Policies using AI

As a Catalog Builder editor, you can use AI to create new UI policies, update existing ones, and deactivate them, all through simple, conversational prompts. Each UI policy can include multiple actions, and AI can create that for you.

## Making targeted changes

You don't have to recreate a UI policy from scratch every time you must tweak something. AI lets you make focused changes to an existing UI policy—renaming it, editing its description, updating trigger conditions, or adding, modifying, or removing individual actions.

## Managing UI policy actions

UI policy actions are the individual rules defining what happens when a policy's conditions are met—for example, making a field mandatory or hiding a variable. You can add new actions, update existing ones, or delete actions you no longer need, all through AI.

## Confirmation after every change

After AI generates or updates a UI policy, it will send you a confirmation message letting you know what was done and prompting you to review the behavior. This gives you a chance to verify the output before moving on.

## Multiple actions in a single instruction create one UI policy

If a user provides multiple condition–action statements in one message. For example: “If RAM is 8GB, set storage to 2TB and set color to red.” The AI creates one UI Policy with:

-   Condition: RAM = 8GB
-   Actions: storage = 2TB, color = red

## Adding to an existing UI policy

-   If you give ServiceNow Otto a new instruction that uses the same condition as a UI policy that was already created, the system doesn't create a duplicate. Instead, it adds the new action to the existing UI policy.
-   For example, if you previously stated:

    "If RAM is 8GB, set storage to 2TB", later say "If RAM is 8GB, set color to red". Then AI recognizes that both instructions share the same condition and simply adds the new action to the existing policy rather than creating a separate one.


## Using conversational cues to group actions

AI also picks up on natural conversational phrases to understand when you want to keep adding to the same policy. Phrases like "also, add one more thing, or add to the same policy" tells system to treat your new instruction as an addition to the current UI policy.

## Creating UI policy for a different condition

-   If your instruction involves a condition that is different from any existing UI policy, AI automatically creates a new, separate UI policy for it.
-   For example, saying "If RAM is 16GB, hide the processor field" when no policy with that condition exists creates a new UI policy specifically for that condition.

## What happens when there is a conflict

If an instruction contradicts an existing policy, like changing "set color to red" to "set color to blue" under the same condition, AI flags the conflict instead of overwriting it. AI asks you to confirm how you want to proceed. For example, "There is an existing UI policy with a conflicting action for this condition. Do you still want to proceed with creating this action?"

This confirms that changes are intentional and nothing gets overwritten by mistake.

**Parent Topic:**[Things to know while creating items using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/things-to-know-while-creating-items-using-ai.md)

