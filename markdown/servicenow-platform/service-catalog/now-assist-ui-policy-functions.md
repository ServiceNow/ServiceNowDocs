---
title: Now Assist: UI policy functions
description: Now Assist can generate UI policies with multiple actions from simple natural language.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Catalog item generation reference, Now Assist in Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Now Assist: UI policy functions

Now Assist can generate UI policies with multiple actions from simple natural language.

## What you can do with UI Policies using Now Assist

As a Catalog Builder editor, you can use Now Assist to create new UI policies, update existing ones, and deactivate them, all through simple, conversational prompts. Each UI policy can include multiple actions, and Now Assist can create that for you.

## Making targeted changes

You don't have to recreate a UI policy from scratch every time you need to tweak something. Now Assist lets you make specific, focused changes to an existing UI policy, such as updating its name or description, changing the conditions that trigger the policy, and adding, modifying, or removing individual actions within the policy.

## Managing UI policy actions

UI policy actions are the individual rules that tell the system what to do when the policy's conditions are met, for example, making a field mandatory or hiding a variable. You can add new actions, update existing ones, or delete actions you no longer need, all through Now Assist.

## Confirmation after every change

After Now Assist generates or updates a UI policy, it will send you a confirmation message letting you know what was done and prompting you to review the behavior. This gives you a chance to verify the output before moving on.

## Multiple actions in a single instruction create one UI policy

If a user provides multiple condition–action statements in one message. For example: “If RAM is 8GB, set storage to 2TB and set color to red.” The Now Assist creates one UI Policy with:

-   Condition: RAM = 8GB
-   Actions: storage = 2TB, color = red

## Adding to an existing UI policy

-   If you give Now Assist a new instruction that uses the same condition as a UI policy that was already created, the system doesn't create a duplicate. Instead, it adds the new action to the existing UI policy.
-   For example, if you previously said "If RAM is 8GB, set storage to 2TB" and later say "If RAM is 8GB, set color to red", Now Assist recognizes that both instructions share the same condition and simply adds the new action to the existing policy rather than creating a separate one.

## Using conversational cues to group actions

Now Assist also picks up on natural conversational phrases to understand when you want to keep adding to the same policy. If you use phrases like "also", "add one more thing", or "add to the same policy", the system treats your new instruction as an addition to the UI policy that is currently being worked on.

## Creating a new UI policy for a different condition

-   If your instruction involves a condition that is different from any existing UI policy, Now Assist automatically creates a new, separate UI policy for it.
-   For example, if you say "If RAM is 16GB, hide the processor field" and no policy with that condition exists yet, a new UI policy is created specifically for that condition.

## What happens when there is a conflict

If a new instruction contradicts an existing UI policy, for example, one policy says "If RAM is 8GB, set color to red" and you now ask it to "set color to blue" under the same condition, Now Assist flags the conflict rather than overwriting silently. It will ask you to confirm how you want to proceed, for example: "There is an existing UI policy with a conflicting action for this condition. Do you still want to proceed with creating this action?" This ensures that changes are always intentional and nothing gets overwritten by mistake.

**Parent Topic:**[Catalog item generation reference](catalog-item-generation-reference.md)

