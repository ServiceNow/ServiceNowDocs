---
title: Create a new Agent Client Collector policy
description: Policies consist of the CIs monitored by the Agent Client Collector and the checks that run on those CIs. When creating a policy, you configure a filter which determines the CIs on which the checks are to run. For example, a policy to run checks on all Apache web servers. You can create new policies or edit the default policies.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Collect data from your system devices, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Create a new Agent Client Collector policy

Policies consist of the CIs monitored by the Agent Client Collector and the checks that run on those CIs. When creating a policy, you configure a filter which determines the CIs on which the checks are to run. For example, a policy to run checks on all Apache web servers. You can create new policies or edit the default policies.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

When associating a check definition with a policy, a copy of the definition is created as a check instance. These values appear on the **Check Instances** tab on the bottom of the **Policy** form. Any changes you make to a check instance affect only the instance in the policy; the original check definition remains unchanged. When changing the original check definition, the changes do not apply to already created check instances. It is recommended you make a copy of a check definition if you are changing its default parameters after having initiated one or more check definitions in a policy.

Some policy checks require credentials, while others do not. For example:

-   The Agent Client Collector does not require credentials for checks that run on its own server. However, when accessing software requiring root or administrator access \(such as MySQL\), credentials are required.
-   When the Agent Client Collector is used as a proxy:
    -   Credentials must be invoked to allow the agent to connect to the remote device over SNMP or other protocols.
    -   Increase the agent's **cpu\_percentage\_limit** value in the `acc.yml` file, as indicated in the blue box on the **Proxy Settings** tab.
-   When the Agent Client Collector uses the HTTP endpoint:
    -   If the URL does not require logging in \(such as with a public website\), no credentials are required.
    -   If the URL does require logging in \(such as with an API endpoint\), credentials are required.

You assign a credential alias in the policy's **Credentials** tab, as described in the following procedure.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Click **New**.

    The **Policy** page appears.

3.  Enter values in the fields on the page, as described in the following table:

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the policy.|
    |Description|Description of the policy.|
    |Publish status|Hard coded as **Draft**, which means that the policy has not yet been published. You cannot edit this field.|
    |Hierarchy|Hard coded as **None**. When a child policy is added to the policy, the value changes to **Parent**. Child policies have a value of **Child**.|

4.  On the **Monitored CIs** tab, select one of the following options:

    -   **Manual calculation**: Select to exclude the policy from scheduled policy calculation, ignoring any changes to the policy's impacted CIs.

        Select this option when the policy monitors a single CI. Otherwise, the Refresh and Publish Monitoring Policies scheduled job takes an abnormally long time to complete.

    -   **Monitored CI type by filter**: Configure the following sub-fields:
        -   **Monitored CI type**: Select the CI type which you want the policy's checks to monitor.
        -   **Filter**: Configure a filter so that the policy's checks monitor only CI types meeting the specified criteria. Included in the available criteria are a CI's **tags**.

            ![Policy tags](../image/ACC-tags-search.png "Tags")

    -   **Monitored CI type by script**: Enables you to specify the monitored CIs using a script. Using a script allows you to create a CI filter for tables related to each other, and not just for a single table. For example, you can set a filter in both a Linux servers table and an Oracle table when searching for a CI. You return an object containing the table and filter at the end of the script.

        An example of a script appearing in the **Monitored CI Script** field is:

        ![Monitored CI Script example](../image/ACC-Monitored-CI-Type-Script.png)

    -   **Monitored CI type by CMDB Group**: Enables you to specify the monitored CIs by using CMDB group queries. When selecting this option, the **Monitored CMDB group** field appears, where you select a CMDB group to associate with the policy.
        -   For details on CMDB groups, see [CMDB groups](https://www.servicenow.com/docs/access?context=cmdb-groups&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
        -   For details on building a CMDB query using the CMDB query builder, see [Build a CMDB query using the CMDB query builder](https://www.servicenow.com/docs/access?context=use-cmdb-query-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
5.  Select checks in the **Available** cell on the **Checks** tab, and move them to the **Selected** cell for them to be included in the policy.

    Checks can be selected multiple times, when you are monitoring more than one process. You can also select a group of checks in the **Filter checks by groups** field, which presents checks of the selected group in the **Available** cell.

6.  Configure a proxy server on the **Proxy Settings** tab.

    Configure a proxy server only when using the agent as a proxy to report data on remote machines. For details, see [Configure an agent on a proxy server](configure-agent-proxy-server.md).

7.  On the **Scheduling** tab, select one of the following:

    -   **Interval-based scheduling**: Configure the time interval \(in seconds\) to indicate the frequency with which the policy's checks will run.
    -   **Cron-based scheduling**: Enables configuring the policy to be active only during a specific time or time frames.
        1.  Select the unlock icon \(![Unlock icon](../image/acc-lock-icon.png)\) to enable selecting cron expressions.
        2.  Select the search icon \(![Search icon](../../event-management/image/search-icon.png)\) to select a cron expression. Select **New** to create a new cron expression, or select one of the cron expressions that come with the base system, which are:

            -   Every hour nightly 5:00pm-7:00am
            -   Every minute daily 8:00am-4:59pm
            -   Every minute Mon-Fri 8:00am-4:59pm
            When creating a new cron expression, you must enter it in valid cron format.

            The specified cron expression operates in the time zone of the machine hosting the agent.

    **Note:** If an **Interval** or **Cron** value was specified for the check definition, that value overrides the value configured in either of these fields.

8.  In the **How to send the check results** field, select the frequency with which check results are to be sent.

    -   When event severity changes \(default for event checks\)
    -   Always send check results \(default for non-event checks\)
    -   Do not send check results
    -   When the check results change
    -   \(Advanced\) Based on exit codes of the check: Send results only if the exit code is 240 \(OK\), 241 \(Warning\), or 242 \(Critical\). However, if the command output is empty, then even if one of these codes are part of the exit code, check results are not sent.
9.  On the **Credentials** tab, select one of the following:

    -   **Credential name**: Select credentials to be assigned to the policy. The available credentials are those displayed on the associated check definition's **Check Secure Parameter Definitions** tab.
    -   **Credential alias**: Select the search icon ![Search icon](../../event-management/image/search-icon.png) to select a credential alias to be used by the policy's checks to connect to the monitored CI. The available options are those created on the **Connection &amp; Credential Aliases** page. For details on credential aliases, see [Credential aliases for Discovery](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).
10. Click **Save**.

    The following buttons appear:

    -   **Publish**: Publishes the Draft policy, moving its **Publish status** to **Queued**. A queued policy is processed by the policy publishing job. The job calculates which agents run the policy and then sends the policy to the relevant MID Servers. The job then moves the policy's **Publish status** to **Published**. A published policy is active on the agent.
    -   **Delete**: Deletes the policy.

**Related topics**  


[Create a policy hierarchy](acc-create-policy-hierarchy.md)

