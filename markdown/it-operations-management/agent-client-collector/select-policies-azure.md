---
title: Select the Azure policies to activate for metric collection
description: Activate the Azure policies that come with the Agent Client Collector base system so that Azure virtual machines can collect metrics. These metrics help you monitor the configuration items \(CIs\) in the CMDB.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Select the Azure policies to activate for metric collection

Activate the Azure policies that come with the Agent Client Collector base system so that Azure virtual machines can collect metrics. These metrics help you monitor the configuration items \(CIs\) in the CMDB.

## Before you begin

-   Prepare an instance with an active MID Server and metric base.
-   Install Agent Client Collector Framework and Agent Client Collector Monitoring.
-   Run Discovery on the Azure cloud account to populate the CMDB with CIs to be monitored.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Prepare and configure the proxy agent to be used by the policy.

    For details on configuring a proxy agent, see [Using proxy agents in Agent Client Collector](../concept/proxy-agent.md).

2.  Assign the credentials to the Azure policy.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

    2.  Select the relevant policy.

        For details on the policies that are available with the base system, see [Azure cloud metrics](../concept/azure-cloud-metrics.md).

    3.  Select the **Credentials** tab.

    4.  In the **Credential name** field, select the credentials to be invoked for the policy.

        To see the available credentials, go to the Credentials page by navigating to **All** &gt; **Discovery** &gt; **Credentials**.

        Ensure that you select the **Type=Azure** credentials. If you need to create credentials, select **New** and select **Azure Service Principal** credentials.

    5.  In the **Credential alias** field, assign an alias to the credentials.

3.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Policies** and select the relevant policy to activate.

4.  Select the application scope icon ![Application scope icon.](../image/application-scope-icon.png) and verify that you are in the Agent Client Collector Monitoring scope to edit the policy.

5.  Enable the policy in Edit mode by selecting **Edit in Sandbox**.

6.  Enable the proxy agent to be used to execute the check.

    1.  Select the **Proxy Settings** tab.

    2.  Select **Single proxy agent** and select the proxy agent to be used to execute the check from the **Proxy agent** field.

7.  Select **Save**.

8.  Republish the policy by selecting **Republish**.


**Parent Topic:**[Deploying Agent Client Collector on servers](../concept/acc-server-deployment.md)

