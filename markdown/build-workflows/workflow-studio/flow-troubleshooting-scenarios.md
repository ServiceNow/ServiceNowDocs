---
title: Flow troubleshooting scenarios
description: Learn how the Flow Troubleshooting Agent addresses common flow execution errors and troubleshooting scenarios you may encounter when designing and running flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/flow-troubleshooting-scenarios.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [reference, scenarios, troubleshooting, flow execution]
breadcrumb: [Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Flow troubleshooting scenarios

Learn how the Flow Troubleshooting Agent addresses common flow execution errors and troubleshooting scenarios you may encounter when designing and running flows.

## Tested troubleshooting scenarios

The Flow Troubleshooting Agent has been validated against a wide range of troubleshooting scenarios. These scenarios represent common flow execution failures that the agent can help diagnose and resolve.

-   Approval action troubleshooting
-   Trigger troubleshooting

## Approval action troubleshooting

Approval actions are a common point of failure in flows. The agent can diagnose and resolve issues related to:

-   **Missing or empty approval recipients**

    The approval action fails because the recipient field is empty or cannot resolve the user reference.

    **How the agent helps:** The agent traces the data flow through previous steps to identify where the recipient field value is being lost or cleared. It checks for business rules or other flows that might be clearing the field and recommends reordering your flow steps or modifying conflicting business rules.

-   **Approval audit trail gaps**

    The approval is created but audit history shows missing or incorrect decision tracking.

    **How the agent helps:** The agent analyzes the approval engine's expected behavior and compares it with your flow's configuration. It identifies missing approval history tracking and recommends enabling the necessary logging or adjusting your approval action settings.

-   **Business rule conflicts with approval engine**

    A business rule is interfering with the approval action's execution or the approval engine's ability to process decisions.

    **How the agent helps:** The agent scans your business rules against the approval engine's expected operations and identifies rules that might be preventing the approval from functioning correctly. It recommends specific changes such as adding flow conditions to business rules or adjusting execution order.


## Trigger troubleshooting

Flow triggers control when your flow runs. Trigger-related issues can prevent flows from executing:

-   **Trigger not firing as expected**

    A flow trigger is configured but the flow does not execute when the trigger condition should occur.

    **How the agent helps:** The agent analyzes your trigger configuration and compares it against the actual data changes or events occurring in your system. It identifies mismatches between the trigger condition and real-world events and recommends adjusting trigger logic or investigating data event patterns.

-   **Trigger role or permission issues**

    The flow trigger is not executing because the user or process lacks the necessary permissions to trigger the flow.

    **How the agent helps:** The agent checks your flow trigger's role and permission settings against the users or processes that should trigger the flow. It recommends enabling the necessary roles or adjusting trigger visibility settings.


**Parent Topic:**[Flows, subflows, and actions reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/flow-designer-reference.md)

