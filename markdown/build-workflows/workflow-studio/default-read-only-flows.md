---
title: Default read-only flows
description: Open existing flows in a read-only state to protect them from accidental changes. While a flow is in a read-only state, you can only review, test, deactivate, or request to edit it.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Default read-only flows

Open existing flows in a read-only state to protect them from accidental changes. While a flow is in a read-only state, you can only review, test, deactivate, or request to edit it.

## Request to edit flow

As of the Washington DC release, you must request to edit an existing flow before you can change it. If you don't have permission to edit a flow, the Edit flow button remains disabled.

![Example flow displaying the Edit flow option.](../../workflow-studio/images/example-edit-flow-option.png "Edit flow option")

When you request to edit a flow, Workflow Studio checks whether another person already has the flow open for edit. If the flow is available for editing, you open the flow in an editable state. If the flow is already being edited, you see a message displaying the name of the user editing the flow.

![Unable to edit flow. Another user is currently editing the flow: Abel Tuter. You will be able to edit the flow once the other user has closed it.](../../workflow-studio/images/unable-to-edit-flow.png "Unable to edit flow message")

## Stop editing a flow

Flows remain in an editable state until one of these events occur.

-   You close the Workflow Studio flow tab.
-   You close the Workflow Studio browser tab.
-   You select the **Make flow read only** option.
-   You remain inactive in the flow for more than 30 minutes.

When you're done editing a flow, you can make it read only so that other people can edit it. You can use the **Make flow read only** option to stop editing a flow.

![More actions menu displaying the Make flow read only option.](../../workflow-studio/images/example-make-flow-read-only-option.png "Make flow read-only option")

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

