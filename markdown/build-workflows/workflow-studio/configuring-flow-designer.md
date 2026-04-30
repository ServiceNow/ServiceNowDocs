---
title: Configuring flows
description: Configure user access, API access, and properties for Workflow Studio flows.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Workflow Studio, Build workflows]
---

# Configuring flows

Configure user access, API access, and properties for Workflow Studio flows.

## Activation

Workflow Studio flows, subflows, and actions are ServiceNow AI Platform features that are active by default.

## Configuration options

|Configuration option|Reference|
|--------------------|---------|
|Retain flow execution details|[Flow execution details retention](flow-reporting.md)|
|Create flow-specific execution settings|[Flow execution settings](flow-execution-settings.md)|
|Enable flow reporting|[Activate flow reporting](../task/enable-flow-reporting.md#)|
|View flow and action dashboards|[FDIH Dashboard](fdih-dashboard.md)|
|Set flow priority|[Flow priority](flow-priority.md)|

|Configuration option|Reference|
|--------------------|---------|
|Grant users access to build flows by role|[User access to Workflow Studio flows](user-access-flow-designer.md)|
|Restrict access to individual flow and action features by custom roles|[Manage access to Workflow Studio flow features](../task/manage-access-features.md)|
|Filter flow and action content by role|[Content filtering for Workflow Studio flows](content-filtering-flow-designer.md)|

|Configuration option|Reference|
|--------------------|---------|
|Grant access to flow and action APIs|[API access to Workflow Studio flows](api-access-flow-designer.md)|
|Create code snippets|[Create code snippets for flows, subflows, and actions](../task/flow-design-code-snippet.md)|
|Create a client callable flow, subflow, or action|[Create a client callable flow, subflow, or action](../task/grant-access-flow-apis.md)|

|Configuration option|Reference|
|--------------------|---------|
|Manage cross-scope access to flows and actions|[Restricted caller access to Workflow Studio flows](restricted-caller-access-flow-designer.md#)|
|Upgrade restricted caller access|[Upgrade restricted caller access privileges for flows and actions](restricted-caller-access-flow-designer.md#)|

|Configuration option|Reference|
|--------------------|---------|
|Update flow diagramming|[Update to the latest version of Flow Diagramming](../task/update-to-latest-version-flow-diagramming.md)|
|Update Workflow Studio and all of its dependencies|[Update to the latest version of Workflow Studio](../../workflow-studio/task/update-to-the-latest-version-of-workflow-studio.md)|

-   **[Flow administration](flow-administration.md)**  
Identify and troubleshoot potential issues by reviewing action and flow executions, their result state, and their runtime duration.
-   **[User access to Workflow Studio flows](user-access-flow-designer.md)**  
Administrators can grant users access to Workflow Studio flows by assigning delegated development permissions or directly assigning a user role. Administrators can also specify which features and content a user can access based on user roles. Application developers can access Workflow Studio functionality through APIs for flows, subflows, and actions.
-   **[API access to Workflow Studio flows](api-access-flow-designer.md)**  
Application developers can access Workflow Studio functionality through APIs for flows, subflows, and actions. Flow authors can enable individual flows, subflows, and actions to be client callable during design.
-   **[Restricted caller access to Workflow Studio flows](restricted-caller-access-flow-designer.md#)**  
Track flows and actions that require access to cross-scope resources. Allow or deny flows and actions access to cross-scope resources.
-   **[Set flow user preferences](../task/set-flow-user-preferences.md)**  
Set your preferences when building and editing flows such as the default editor view.
-   **[Update to the latest version of Flow Diagramming](../task/update-to-latest-version-flow-diagramming.md)**  
Flow diagramming is automatically installed on your instance as a dependency of Workflow Studio.

**Parent Topic:**[Configuring Workflow Studio](../../workflow-studio/concept/configuring-workflow-studio.md)

