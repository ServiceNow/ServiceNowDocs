---
title: Enable Usage Insights for Interaction Controls Component \(ICC\) enabled call events
description: Configure Usage Insights to enable tracking of call events that are captured for agents. Admins and managers can view agent call events, inspect event payloads, and diagnose issues directly within the ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/enable-usage-insights-for-icc-call-events.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 2
breadcrumb: [Usage insights for call events enabled using Interaction Controls Component \(ICC\), ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Enable Usage Insights for Interaction Controls Component \(ICC\) enabled call events

Configure **Usage Insights** to enable tracking of call events that are captured for agents. Admins and managers can view agent call events, inspect event payloads, and diagnose issues directly within the ServiceNow instance.

## Before you begin

Role required: admin

To enable this capability complete the following independent configuration steps:

1.  Enable analytics for agents.
2.  Add agents to a system property that controls event logging.

Confirm the following prerequisites before you begin configuration:

-   **Admins**

    You must have system administrator access to the ServiceNow instance to modify system properties.

-   **Usage Insights access**

    Confirm that **Platform Analytics** &gt; **Usage Insights** is available in your instance. The module is provided out-of-box.

-   **ICC configuration**

    The agents you're enabling must assigned to the instance enabled via ICC.

-   **Agent availability**

    Agents must log in and update their own presence.


## Procedure

1.  Enable analytics in agent preferences.

    Each agent whose events you want to track must enable analytics in their own profile preferences. Repeat the following sub steps for each agent.

    \[Omitted image "enable-analytics-in-agent-preferences.png"\] Alt text: Enable analytics for agents

    1.  Log in to the ServiceNow instance as the agent.

    2.  Select the agent profile icon in the upper-right corner of the Workspace and select **Preferences**.

    3.  Navigate to the **User Experience** section.

    4.  Locate the **Enable Analytics** toggle and set it to **ON**.

    5.  Save the preferences.

    This setting must be configured individually for each agent as it is not applied globally.

2.  Configure the **sn\_openframe.logger.enabled.users** system property.

    To log events for specific agents at the platform level, add their **sys\_ids** to the **sn\_openframe.logger.enabled.users** system property.

    \[Omitted image "configure-openframe-logger-enabled-user-sys-property.png"\] Alt text: Configure sn\_openframe\_logger\_enabled\_users

    1.  Log in to the ServiceNow instance as a system administrator.

    2.  Navigate to **System Properties** &gt; **All Properties**, or search for **sn\_openframe\_logger\_enabled\_users** CSMFSin the filter.

    3.  Open the **sn\_openframe\_logger\_enabled\_users** property record.

    4.  In the **Value** field, enter the **sys\_ids** of the agents, separated by commas.

        Use the following format:

        ```
        <sysID1>,<sysID2>,<sysID3>
        ```

    5.  Select **Update** to save the property.

        To find a **sys\_id**, navigate to the **sys\_user** list, locate the agent record, right-click the **sys\_id** field, and select **Copy sys ID**.

3.  Register custom events.

    Perform this step only if agents use custom buttons added to the active call component. Out-of-box call events do not require additional registration.

    1.  Identify any custom call control buttons added to the active call component that are not part of the standard ICC event set.

    2.  Work with the development team to instrument each custom button using the **Usage Insights** event registration APIs.

    3.  Submit the new event registrations for approval and inclusion to the **Usage Intelligence Dashboard**.


## Result

After completing this configuration, **Usage Insights** begins capturing events for the agents you enabled. You can verify the setup as follows:

-   Navigate to **Platform Analytics** &gt; **Usage Insights** and filter by CSM/FSM Configurable Workspace.
-   Select the **Users** or **Sessions** view. The enabled agents’ sessions should appear after they log in and perform call actions.
-   Select a session and confirm that ICC triggered **NVC events** appear with complete payloads.

If no events appear after an agent has completed a call action, verify that the **Enable Analytics** toggle is set to **ON** in the agent’s preferences and that their **sys\_id** is correctly entered in the **sn\_openframe\_logger\_enabled\_users** property.

**Note:** Users are displayed as \#IDs in **Usage Insights**.

