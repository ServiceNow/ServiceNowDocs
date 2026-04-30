---
title: Content filtering for Workflow Studio flows
description: Specify which content a user can access based on the user's role.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [User access to flows, Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Content filtering for Workflow Studio flows

Specify which content a user can access based on the user's role.

Display only content that is relevant for a particular user, hiding content that is unnecessary or sensitive. Specify the Workflow Studio flow content that you want to control access to and the role that a user must have to access it. For example, if a user with the hr\_manager role in human resources is creating a flow, show only the set of actions and subflows that are relevant to HR cases.

Content filtering uses:

-   Content definitions to specify types of content.
-   Content filtering rules to determine who can access the content.

Workflow Studio includes several default definitions and filtering rules. Set up content filtering by modifying pre-existing rules or creating your own.

## Content definitions

Content definitions specify a type of Workflow Studio flow resource. Resources are the key components of Workflow Studio flows, such as triggers, actions, and subflows. Create definitions to include an entire resource, or refine your definitions through conditions. For example, you can create a definition that includes all flow triggers, or you can use conditions to include only triggers with a category of date.

You can further refine content definitions through tagging. Add tags to items in a resource list, then design your content definition to only include resources with that tag.

## Content filtering rules

Content filtering rules specify the role that a user must have to access the content in a particular definition. Each rule associates a single user role with a single content definition. When a user accesses Workflow Studio flows, content filtering rules determine what content the user may access based on the user's role.

## Feature access

You can also filter access to Workflow Studio flow features. Features are UI elements and sections. Access to both elements and sections can be managed by configuring content definitions and filtering rules. However, access to UI elements can also be managed through a simplified UI. For more information, see [Manage access to Workflow Studio flow features](../task/manage-access-features.md).

## Read-only flows

Users may be able to view a flow, subflow, or action containing content that they can't normally access. For example, a flow that's visible to a user might include an action the user wouldn't usually be able to view. When a flow contains restricted content, the entire flow becomes read-only. Users can run the flow but can't modify or copy it.

The creation of read-only flows doesn't apply to feature filtering. If a user doesn't have access to a feature, the feature doesn't render for that user. It doesn't affect the ability to copy or modify a flow. If a user doesn't have access to transform functions and uses a flow that already has a transform function applied, the transform function is read-only. The rest of the flow can still be copied and modified.

## Access summary

<table id="table_b54_sj5_4lb"><thead><tr><th>

Resource filtered

</th><th>

User has role

</th><th>

User does not have role

</th></tr></thead><tbody><tr><td>

Flow

</td><td>

-   The flow is visible to select during design.
-   The flow can be copied.
-   The flow can be modified.

</td><td>

-   The flow is hidden and cannot be selected during design. For example, the flow is hidden when creating a Playbooks activity definition.
-   The flow cannot be copied.
-   The flow is read-only.

</td></tr><tr><td>

Flow execution details

</td><td>

The flow execution details are visible.

</td><td>

The flow execution details are hidden.

</td></tr><tr><td>

Trigger

</td><td>

-   The trigger is visible to select during design.
-   Any flow that includes the trigger can be copied.
-   Any flow that includes the trigger can be modified.

</td><td>

-   The trigger is hidden and cannot be selected during design.
-   Any flow that includes the trigger cannot be copied.
-   Any flow that includes the trigger is read-only.

</td></tr><tr><td>

Subflow

</td><td>

-   The subflow is visible to select during design.
-   Any flow that calls the subflow can be copied.
-   Any flow that calls the subflow can be modified.

</td><td>

-   The subflow is hidden and cannot be selected during design.
-   Any flow that calls the subflow cannot be copied.
-   Any flow that calls the subflow is read-only.

</td></tr><tr><td>

Subflow execution details

</td><td>

The subflow execution details are visible.

</td><td>

The subflow execution details are hidden.

</td></tr><tr><td>

Flow logic

</td><td>

-   The flow logic is visible to select during design.
-   Any flow that includes the flow logic can be copied.
-   Any flow that includes the flow logic can be modified.

</td><td>

-   The flow logic is hidden and cannot be selected during design.
-   Any flow that includes the flow logic cannot be copied.
-   Any flow that includes the flow logic is read-only.

</td></tr><tr><td>

Action

</td><td>

-   The action is visible to select during design.
-   Any flow that includes the action can be copied.
-   Any flow that includes the action can be modified.

</td><td>

-   The action is hidden and cannot be selected during design.
-   Any flow that includes the action cannot be copied.
-   Any flow that includes the action is read-only.

</td></tr><tr><td>

Action execution details

</td><td>

The action execution details are visible.

</td><td>

The action execution details are hidden.

</td></tr><tr><td>

Step

</td><td>

-   The step is visible to select during design.
-   Any action that includes the action can be copied.
-   Any action that includes the step can be modified.

</td><td>

-   The step is hidden and cannot be selected during design.
-   Any action that includes the step cannot be copied.
-   Any action that includes the step is read-only.

</td></tr><tr><td>

UI elements and sections, excluding transform functions

</td><td>

-   The UI element or section is visible to use during design.
-   Any flow, subflow, or action that includes the UI element or section can be copied.
-   Any flow, subflow, or action that includes the UI element or section can be modified.

</td><td>

-   The UI element or section is hidden and cannot be used during design.
-   Any flow, subflow, or action that includes the UI element or section can be copied.
-   Any flow, subflow, or action that includes the UI element or section can be modified.

</td></tr><tr><td>

Transform functions

</td><td>

-   Transform functions are visible to use during design.
-   Any flow, subflow, or action that includes a transform function can be copied.
-   Any flow, subflow, or action that includes a transform function can be modified.

</td><td>

-   Transform functions are hidden and cannot be used during design.
-   Any flow, subflow, or action that includes a transform function can be copied. The transform function is read-only.
-   Any flow, subflow, or action that includes a transform function can be modified. The transform function is read-only.

</td></tr></tbody>
</table>-   **[Configure content filtering definitions](../task/configure-content-filtering.md)**  
Specify which content a user can access by creating content definitions.
-   **[Configure content filtering rules](../task/configure-content-filtering-rules.md)**  
Use content filtering rules to specify the role a user must have to access content.

**Parent Topic:**[User access to Workflow Studio flows](user-access-flow-designer.md)

