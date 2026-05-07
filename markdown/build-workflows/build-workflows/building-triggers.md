---
title: Building triggers
description: A trigger contains the start conditions for your automation. You can create separate triggers for each flow or create a reusable saved trigger that you can use in multiple flows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-06-19"
reading_time_minutes: 1
---

# Building triggers

A trigger contains the start conditions for your automation. You can create separate triggers for each flow or create a reusable saved trigger that you can use in multiple flows.

By creating a saved trigger, you enable the flow authors to use a predefined trigger rather than creating a new trigger definition for their flow. Any changes made to the trigger are propagated to each flow that uses the trigger.

The following video demonstrates how you can use saved triggers in Workflow Studio.

Saved triggers in Workflow Studio 

-   **[Create a saved record-based trigger](../task/create-saved-trigger.md)**  
Create a reusable trigger definition that responds to a record-based event. When a record is created or updated in a specific table, the trigger activates and starts the flows where it is used. You can allow flow authors to select the saved trigger, view its conditions, or add their own conditions.
-   **[Create a saved scheduled trigger](../task/create-scheduled-trigger.md)**  
Create a scheduled trigger that starts your flow when you need. Schedule the trigger to start your flow on a specific date and time or repeatedly at scheduled intervals. Reuse the trigger in flows that need to run on the same schedule.
-   **[Create a saved external trigger](../task/create-saved-external-trigger.md)**  
Save a set of trigger definitions as a reusable trigger that responds to external events through webhooks. When an event occurs in the configured third-party application that meets the specified conditions, the trigger is activated.
-   **[Use a saved trigger](../task/use-saved-trigger.md)**  
Instead of creating a trigger, use a saved trigger in your flow. Using a saved trigger enables you to reuse standardized trigger logic across flows, reducing the effort, improving consistency, and simplifying ongoing maintenance.
-   **[Edit a saved trigger](../task/edit-saved-trigger.md)**  
Edit a saved trigger in Workflow Studio to update the trigger definitions or other options according to your business needs.
-   **[Detach a saved trigger from a flow](../task/detach-saved-trigger.md)**  
View a list of flows that are associated with a saved trigger, and detach it from any of the flows. Detach a saved trigger before you specify different start conditions for your flow or before you delete the trigger.
-   **[Delete a saved trigger](../task/delete-saved-trigger.md)**  
Delete a saved trigger that you no longer need.

**Parent Topic:**[Workflow Studio flows, subflows, and actions](../../workflow-studio/reference/workflow-studio-flows-subflows-and-actions-landing.md)

