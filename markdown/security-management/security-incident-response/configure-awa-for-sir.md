---
title: Configure Advanced Work Assignment for SIR Workspace
description: Improve security incident routing for the security analysts by configuring the Advanced Work Assignment \(AWA\) for Security Incident Response Workspace.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-11-26"
reading_time_minutes: 2
breadcrumb: [Advanced Work Assignment for SIR, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Advanced Work Assignment for SIR Workspace

Improve security incident routing for the security analysts by configuring the Advanced Work Assignment \(AWA\) for Security Incident Response Workspace.

## Before you begin

-   The AWA \[com.glide.awa\] feature must be installed.
-   Other security incident assignment methods should be disabled.
-   Certain roles are required to work with AWA that aren’t included with the SIR application:

    -   Administrators who will be configuring AWA must be assigned the AWA admin \(awa\_admin\) role.
    -   Security analysts who are using AWA to manage security incidents must be assigned the awa\_agent role.
    For more information, see [Components installed with Security Incident Response](../../security-incident-response/reference/installed-with-sir.md).

-   Role required: awa\_admin


## Procedure

1.  Configure a service channel.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Service Channels**.

    2.  Select the **Security Incident** service channel.

        This service channel is available in the base system. For information about customizing the channel, see [Create or configure a service channel](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

2.  Configure assignment rules for assigning security incidents.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Assignment Rules**.

    2.  Select **Security Incident assignment rule**.

        The **Security Incident assignment rule** is available in the base system. For information about how to customize assignment rules, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    3.  Enable auto-assignment of analysts by selecting **Enable auto-assign work items**.

    4.  Enable security analysts to reject a security incident by navigating to the **Rejection handling** tab and selecting **Allow agent to reject**.

3.  Determine which incidents to route to a particular security analyst through a given service channel by configuring queues.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  Select **Security Incident Queue**.

        The Security Incident Queue is available in the base system. You can customize the queue as needed.

        Create additional queues if you need. For each new queue, define **Work Item Routing Conditions** to ensure that security incidents are directed to the appropriate queue. For more information, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    3.  In the Assignment Eligibility section, select **New**.

    4.  On the form, fill in the fields.

<table id="table_ecb_1hc_f3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent assignment rule

</td><td>

Assignment rule for the security analysts.**Security Incident assignment rule** is available in the base system.

</td></tr><tr><td>

Eligible at

</td><td>

The delay before a specific group becomes eligible to receive a work item

</td></tr><tr><td>

Groups

</td><td>

Option to enable security analyst groups to be assigned.

</td></tr></tbody>
</table>    5.  Select **Submit**.

4.  Configure presence states for security analysts to enable them to indicate whether they’re available to receive work.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  Add or update available presence states for an analyst.

        By default, the Available state is inactive. If the Available state isn’t enabled, AWA doesn’t route incidents to security analysts. For more information, see [Configure agent presence states](https://www.servicenow.com/docs/access?context=awa-configure-agent-presence&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

5.  Configure reject reasons for an analyst to select when rejecting a security incident.

    **Note:** If you don’t enable rejection handling, security incidents are auto-assigned to analysts based on the configured service channel, queues, assignment rules, and analyst's availability.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Reject Reasons**.

    2.  Add or update rejection reasons available to a security analyst.

        For more information, see [Configure reasons for rejecting work items](https://www.servicenow.com/docs/access?context=awa-configure-reject-reasons&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


