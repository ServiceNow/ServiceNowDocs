---
title: Checks and policies
description: A check is a combination of a command and its configuration. The check is executed on the Agent Client Collector's devices to gather data from those devices.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Checks and policies

A check is a combination of a command and its configuration. The check is executed on the Agent Client Collector's devices to gather data from those devices.

## Checks

Checks are provided with the base system, and their commands execute scripts which provide monitoring data for your operating systems and applications. A check's default name indicates what is being monitored and measured, the entity, and the monitoring data. For example, a check named **os.linux.check-system-cpu** checks the CPU data on a Linux system. The identified command in the check runs on the monitored device, providing an output and status. Each individual check is referred to as a **check definition**. After being associated with policies, check definitions are then referred to as **check instances**.

You can customize check instances to meet your needs. For example, customize the running interval or the parameters specific to the policy, such as the login credentials to access a MySQL database. Customization of a check instance takes effect only on the check instance associated with the policy, which does not affect the original check definition or already created check instances in other policies.

The following check types are provided with the Event Management base system:

-   **Event**: The check's result is transformed into an Event Management event.
-   **Metric**: The values from the check result are transformed to metrics.

For details on the Agent Client Collector Framework default checks, see [Agent Client Collector Framework default checks](../reference/acc-framework-checks-policies.md).

For details on the Agent Client Collector Monitoring default checks and policies, see [Agent Client Collector Monitoring default checks and policies](../reference/agent-policies-checks.md).

For details on the Agent Client Collector for Visibility - Content default checks and policies, see [Agent Client Collector for Visibility - Content default checks and policies](../reference/acc-visibility-checks-policies.md).

If checks are not running on the agent's devices, your agent may be in CPU protection mode. CPU protection mode is activated when a device's CPU consumption is too high. To view a list of all disabled checks related to the agent, navigate to the agent record on the Agent Client Collectors page \(**All** &gt; **Agent Client Collector** &gt; **Agents**\), select an agent and select the **Disabled Checks** tab at the bottom of the page.

In the `acc.yml` configuration file, you can modify the CPU protection mode thresholds which determine when a check is disabled. To re-enable a check, select the check and select **Re-enable disabled check** in the **Actions on selected rows...** drop-down. For details on the CPU protection mode thresholds, see [Agent Client Collector CPU protection thresholds](../reference/acc-set-silent-reference.md). For details on manually turning off data collection, see [Pause Agent Client Collector data collection](../task/acc-enable-silent-mode.md).

Configure the cpu\_protection\_behavior property to determine whether all checks enter CPU protection mode, or only the check that crosses the configured cpu\_percentage\_limit value with the highest CPU usage within the monitoring interval. For details, see [Agent Client Collector CPU protection thresholds](../reference/acc-set-silent-reference.md).

A check is marked as **Stale** if it is no longer associated with a policy. To remove a stale check, renable it by selecting the box next to the check and selecting **Re-enable disabled checks** from the **Actions on selected rows...** cell.

In the base system, the event's exit status indicates its severity, as follows:

-   0 = OK
-   1 = WARNING
-   2 = CRITICAL

You can add additional severities \(such as MAJOR and MINOR\) by running a customized script. The following exit statues indicate these severities:

-   13 = MAJOR
-   14 = MINOR

## Privileges for running check commands

If the servicenow base system user does not have privileges to run specific check commands, do the following for the relevant operating systems:

-   In a Linux system: Enable the servicenow user to run the command with `sudo` permissions. Ensure that the following sudo configuration requirements are met:

    -   Disable tty and password requirements
    -   Preserve all environment variables
    -   Support dynamic PATH for executing commands
    Example configuration in the `/etc/sudoers` file:

    ```
    Cmnd_Alias ACC_F = /usr/sbin/dmidecode -s baseboard-serial-number, /usr/sbin/dmidecode -s chassis-serial-number, /usr/sbin/dmidecode -s system-serial-number, /usr/sbin/dmidecode -s system-uuid, /usr/sbin/ss -tanp 
    servicenow ALL=(root) SETENV: /var/cache/servicenow/agent-client-collector/osquery/bin/osqueryi *, ACC_F
    Defaults:servicenow !requiretty
    Defaults exempt_group += servicenow
    
    ```

    **Note:** Command paths may vary. Consult the sudoers manual for special considerations.

    -   The `SETENV:` string enables the servicenow user to preserve environment variables.
    -   The `!requiretty` string disables tty.
    -   Adding the servicenow user to the `exempt_group` bypasses password requirements and enables dynamic PATH for executing sudo commands.
    Ensure that you configure the **must\_sudo** check parameter with a value of **true** in the check command parameters section of the check definition.

-   In a macOS system: Ensure that the user running the agent service belongs to a user group with privileges to query all tcp connections on the host.
-   In a Windows system: Using Windows User Management, add the servicenow user to the groups with the relevant privileges, enabling the user to execute the required commands.

## Executing checks that missed their execution time

A check doesn't execute if the laptop or agent is down during its scheduled execution time. When this happens, the system behavior depends on whether the check has executed previously.

-   Check that never executed: The check runs at the agent reconnect time + X \(where X = 0-60 minutes\), and this is the permanent run time of the check.

    For example: Policy X was synced to an agent. Check A in the policy never ran previously and was scheduled to run at 2am. However, the laptop was asleep at that time. The laptop wakes up at 9:09am. After the agent is restored, it notices that check A never ran. Check A is scheduled to run between 9:09am-10:09am and ends up running at 9:54am. The check A interval is every 24 hours, so check A now is scheduled to run daily at 9:54am.

-   Check that missed an existing execution time: The previously run check runs at the agent reconnect time + X \(where X = 0-60 minutes\), but in the future, the check reverts to its originally scheduled run time.

    For example: Check A runs once a day and is scheduled to run daily at 9:54am. The laptop was asleep or the agent was not connected from 9am until 1pm. At 1:17pm, the laptop is awake and the agent starts and connects. The agent noticed that check A did not run at 9:54am and schedules it to run between 1:17pm-2:17pm. The check ends up running at 1:37pm. However, the next time check A runs is at 9:54am, its originally scheduled time.

    This scenario takes effect only for checks running at an interval of every 60 minutes or more frequently. Checks that run less often than every 60 minutes run at their previous interval time.


## Policies

A **policy** is a combination of the CIs being monitored by the Agent Client Collector and the check definitions that run on those CIs.

To enable a single policy to support multiple credentials, assign a credential alias to the policy. For example, if you have MySQL servers for both Linux and Windows with different credentials, you must create separate policies for each credential type. However, if you use a credential alias, you can assign a single policy to the alias. The agent then matches the relevant credential to the application being monitored. For details on credential aliases, see [Create a Connection and Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md).

Alerts generated by policies with an event-type check are automatically closed when the CI monitoring stops due to any of the following:

-   De-activating the policy
-   De-activating the check that caused the alert
-   Deleting the check from the policy
-   Deleting the policy
-   Modifying the policy filter that determines the monitored CIs

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](acc-shared-deployment.md)

