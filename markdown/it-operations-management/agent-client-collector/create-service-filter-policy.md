---
title: Create a service filter for a policy
description: Configure a service filter so that the policy monitors only those services that match the filter.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a new Agent Client Collector policy, Collect data from your system devices, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Create a service filter for a policy

Configure a service filter so that the policy monitors only those services that match the filter.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

    The **Policies** page appears.

2.  Select a policy.

    The details page of the policy appears.

3.  Select the **Edit in Sandbox** button to enable editing the form.

4.  On the Monitored CIs tab, select the **Filter Monitored CIs by service** check box.

    The **Application Service filter** section appears.

    ![Application service filter section](../image/app-service-filter.png "Application Service filter section")

5.  Configure conditions in the fields and select **Save** at the bottom of the page.

    The policy is configured with the indicated service filter. Only CIs matching the service filter are included in the policy's logs.


