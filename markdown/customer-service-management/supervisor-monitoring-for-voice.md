---
title: Supervisor call monitoring
description: Supervisors can monitor live customer interactions and respond to agent help requests by listening-in, coaching, or barging-in to calls. All supervisor actions taken after accepting a Help Request from an agent are logged with timestamps for audit and reporting.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Monitoring calls, ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Supervisor call monitoring

Supervisors can monitor live customer interactions and respond to agent help requests by listening-in, coaching, or barging-in to calls. All supervisor actions taken after accepting a **Help Request** from an agent are logged with timestamps for audit and reporting.

## Supervisor call monitoring overview

Supervisors can accept help requests from agents and take the following actions from their workspace:

-   Monitor \(silent\)
-   Coach
-   Barge In

Each action taken after a **Help Request** is accepted and recorded with a timestamp. The feature supports Chat, Messaging, and Voice interactions and integrates with conversation-monitoring and supervisor dashboards. Supervisors receive notifications when:

-   A **Help Request** is assigned to them
-   An agent cancels a **Help Request**

For more information, see:

-   [Manager Workspace landing page](../../workforce-optimization-for-customer-service-configurable/concept/csm-configurable-manager-workspace-dashboards-new.md)
-   [Manager dashboard for operational Insights](../../workforce-optimization-for-customer-service-configurable/concept/manager-dashboard-for-operational-insights.md)
-   [Listen, Monitor or Barge in to an agent call](../../workforce-optimization-for-customer-service-configurable/task/listen-agent-call-configurable-wfo-cs.md)

## Dependencies

Enable the following capabilities to view and use the call monitoring features in the Active call and Global call list:

-   **Contact Center as a Service \(CCaaS\) integration:**

    Contact centers must enable the call monitoring capability when integrating with the native call controls via Interaction Controls Component \(ICC\) and OpenFrame.

    Native call controls must be available through ICC and OpenFrame.

    ICC must support supervisor action controls.

-   **Role-based access and permissions:**

    Supervisors must have the  awa\_manager  role.

    When a supervisor with the awa\_manager  role views an interaction, the CCaaS is notified and configures the call controls accordingly.

-   **UI controls:**

    On enabling the feature, the action buttons for Monitor, Coach, and Barge In display as actionable icons on the supervisor's call interface.

    Supervisors can leave a call using the Disconnect button.

-   **Help Request data model**

    Each supervisor action triggered through a **Help Request** is logged with a timestamp.

    The system tracks the **Help Request** status and supports Search for audit and analytics.

    Supervisor actions are scoped to the relevant tenant or domain.

-   **Analytics integration**

    Reporting modules must be integrated to capture supervisor action data.

    Feature availability depends on product and license purchase.


## Workflow

The following steps define a typical workflow for a supervisor-initiated call monitoring:

1.  The supervisor views a dashboard of active calls and agent interactions. They can select an active interaction and choose to monitor, coach, or barge in, depending on the scenario and their permissions.
2.  If an agent submits a **Help Request**, the supervisor receives a notification and selects  **Confirm**  to accept it.
3.  After acceptance:
    -   Available actions are enabled.
    -   The **Help Request** status changes to  In Progress.
    -   The  HelpProvidedBy  field is set to the supervisor.
4.  The supervisor can disconnect from the call at any time.
5.  The agent can close the **Help Request** during the session and submit a new one as required.

**Note:** Silent monitoring isn’t visible to the agent.

## Scenarios

-   **Scenario 1: Supervisor accepts a __Help Request__:**

    After a supervisor accepts a Help Request:

    -   Monitor, Coach, and Barge In options are enabled in the Active Call window.
    -   The **Help Request** interaction flag in the system is set to false.
    -   The **Help Request** status updates to  In Progress.
    -   HelpProvidedBy  in the system is set to the accepting supervisor.
-   **Scenario 2: Agent closes a __Help Request__:**

    While a **Help Request** is in progress, the agent can close it:

    -   The **Help Request** button updates to enable agents to close the request.
    -   The system records the closed status.
    -   A confirmation alert displays.
    -   The agent can submit a new **Help Request** after closing a current one for additional help with the same call, or for a new one.

