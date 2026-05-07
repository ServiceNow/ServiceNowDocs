---
title: Agent help request for voice calls
description: Agents can request supervisor assistance during active customer calls by submitting help requests with context and reason. They receive real-time notifications when supervisors coach or barge in to help them resolve customer issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Monitoring calls, ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Agent help request for voice calls

Agents can request supervisor assistance during active customer calls by submitting help requests with context and reason. They receive real-time notifications when supervisors coach or barge in to help them resolve customer issues.

## Agent help request overview

The help request feature lets agents request supervisor assistance during active calls. Agents can submit help requests with specific reasons and comments to provide context before the supervisors respond. They receive real-time notifications when supervisors join the call. Agents can cancel help requests anytime before a supervisor engagement. All help request events are recorded for reporting and analysis.

The following are some key functionality:

-   Submit help requests with customizable reasons and comments
-   Cancel help requests before supervisor engagement if the issue resolves
-   Receive notifications when supervisors coach or barge in on your call
-   View supervisor name and phone number with clear **Coaching** or **Barge In** labels
-   Track help-request metrics including reason, frequency, duration, and supervisor involvement
-   Automatically cancel help requests when completing Consult or Blind transfer actions
-   Configure phone directory to show or hide Agents, Queues, or External tabs based on CCaaS provider settings. Agents see tabs enabled by the CCaaS provider, preventing transfers to unsupported numbers.
-   While handling a customer call, agents can now see accurate availability status for other agents, supporting informed transfer decisions. Agent availability status updates in the transfer list and phone directory in real-time during call transfers.

## Dependencies

Enable the following capabilities to view and use the call monitoring features in the Active call and Global call windows:

-   Enable the call monitoring capability when integrating with the native call controls via Interaction Controls Component \(ICC\) and OpenFrame.
-   Engage in an active call.
-   Configure the integration with the CCaaS platform for voice controls and supervisor actions.
-   Enable real-time UI update capability.
-   Configure a reporting infrastructure to capture help request metrics.

Persona:

-   **Agent:**

    Submits help requests during active calls to receive supervisor assistance.

-   **Supervisor/Manager/Coach:**

    Responds to help requests and performs coaching or barge in actions with appropriate permissions.


See 

Review the following scenarios to understand how the feature works.

## Submitting a help request

Follow these steps to submit a help request to your supervisor when you require assistance during an active call:

1.  Select the **Help Request** button on the call interface.
2.  Provide a reason and brief description of the issue in the dialog screen.
3.  Select **Submit** to send the request to the supervisor.

## Canceling a help request

Follow these steps to cancel a help request, if the issue is resolved before the supervisor intervenes.

1.  Locate the **Help Request** button on the call interface.
2.  Select **Cancel**.
3.  Select **Yes** to confirm the cancellation in the dialog screen.

## Monitoring conversation

Supervisors may follow these steps to provide silent monitoring during voice calls:

1.  Receive a help request from the agent, which opens the Interaction to establish the voice connection.
2.  Select **Monitor** in the supervisor Workspace.
3.  Listen to the conversation between the agent and customer.

    **Note:** During silent monitoring, the agent and customer aren’t aware that the supervisor is in the listen-only mode.


## Supervisor coaching

Supervisors can follow these steps to provide coaching to agents during voice calls.

1.  Receive a help request from the agent, which opens the Interaction to establish the voice connection.
2.  Select **Coach** in the supervisor Workspace.
3.  Provide coaching by talking to the agent, as the agent is in a listen-only mode during the coaching.
4.  Select **Send** to deliver the coaching to the agent.

## Barge In participation

Supervisors can follow these steps to participate in a voice call when an issue requires immediate attention.

1.  Receive a help request from the agent, which opens the Interaction to establish the voice connection.
2.  Select **Barge In** in the supervisor Workspace.
3.  Join the call and provide the necessary assistance to the agent and the customer.
4.  Select **End Barge In** when the issue is resolved.

**Note:** Once a voice connection has been established with an Interaction, the supervisor can go through all or one of the preceding actions. An action must be completed before attempting a new one.

