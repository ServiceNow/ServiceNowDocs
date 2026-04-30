---
title: Monitoring calls
description: Call monitoring is a feature in the Contact Center as a Service \(CCaaS\) solution that enables supervisors and managers to observe, monitor, and analyze customer interactions.Supervisors can monitor live customer calls enabling them to provide immediate guidance and support through listening, coaching, or intervening as needed. This helps promote high-quality customer interactions.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-06"
reading_time_minutes: 2
breadcrumb: [ICC for voice calls, Integrating with contact centers, Integrate, Customer Service Management]
---

# Monitoring calls

Call monitoring is a feature in the Contact Center as a Service \(CCaaS\) solution that enables supervisors and managers to observe, monitor, and analyze customer interactions.

Contact centers integrating with ServiceNow’s native voice call capability via Interaction Controls Component \(ICC\) and OpenFrame have the option to enable the call monitoring feature, embedded in their CSM Configurable Workspace.

## Key benefits of call monitoring

Some of the key advantages of enabling this feature are as follows:

-   Provides real-time feedback to agents, helping them improve their interactions.
-   Identifies training needs for agents.
-   Promotes consistent quality of customer interactions.
-   Offers insights into customer preferences and sentiment, influencing strategic decisions.

## Core functionality of call feature

-   **Monitor:**

    Enables supervisors to listen-in to live calls for training and compliance.

-   **Coach:**

    Enables supervisors to support agents during live calls via:

    -   Coach, where the supervisor privately coaches using a one-way whisper feature enabling the supervisor to provide guidance that only the Agent can hear.
    -   Barge in, where the supervisor joins the call as a participant and can speak with both the agent and customer.

## Supervisor proactive call monitoring

Supervisors can monitor live customer calls enabling them to provide immediate guidance and support through listening, coaching, or intervening as needed. This helps promote high-quality customer interactions.

### Dependencies

Enable the following capabilities to view and use the call monitoring features in the Active call and Global call list:

-   **Contact Center as a Service \(CCaaS\) integration:**

    Contact centers must enable the call monitoring capability when integrating with the native call controls via Interaction Controls Component \(ICC\) and OpenFrame.

-   **Role-based access and permissions:**

    When a supervisor with the `awa_manager` role views an interaction, the CCaaS is notified and configures the call controls accordingly.

-   **UI controls:**

    On enabling the feature, the action buttons for Monitor, Coach, and Barge in display as actionable icons on the supervisors call interface.


### How does the process work

The following steps define a typical workflow for a supervisor-initiated call monitoring:

1.  The supervisor views a dashboard of active calls and agent interactions. They can select an active interaction and choose to monitor, coach, or barge in, depending on the scenario and their permissions.
2.  The CCaaS platform is notified when a supervisor views an interaction.
3.  The CCaaS platform sets the context for the supervisor's available actions.
4.  The manager selects the **Monitor** button to begin monitoring the call.

    **Note:** Silent monitoring isn't visible to the agent.


![Supervisor call monitoring workflow](../image/int-supervisor-proactive-call-monitoring.png "Supervisor call monitoring workflow")

