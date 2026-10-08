---
title: Create AI Control Tower \(AICT\) policies
description: Create AICT policies to block personnel from using unauthorized AI tools. AICT polices are synchronized with the Agent Client Collector, which invokes the policies that run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/create-aict-policies.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 2
breadcrumb: [AI Proxy, AI Control Tower, Agent Client Collector, IT Operations Management]
---

# Create AI Control Tower \(AICT\) policies

Create AICT policies to block personnel from using unauthorized AI tools. AICT polices are synchronized with the Agent Client Collector, which invokes the policies that run.

## Before you begin

You must configure ACC with an ICS \(mid-less\) architecture to enable using an AICT policies. For details on configuring ACC without a MID Server, see [Configuring MID-less Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-configuring-without-mid.md).

Ensure that ITOM Shadow AI governance is installed in your enviornment.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **AI Assets**.

2.  In the filter on the left side of the page, expand **Govern** and select **Policies**.

3.  Select **Create policy**.

4.  Select a policy type in the **Choose a policy type** field.

    -   A threat response: Takes an agent offline when a security threat is detected.
    -   An explicit block: Blocks a user or department from using an AI agent, model, or domain.
5.  Configure the relevant parameters, based on the selected policy type.

    -   A threat response:
        1.  Select what will happen when a threat is detected.
        2.  In the **Which agents** cell, select the conditions by which the detected threat takes the agent offline.
        3.  In the **sensitivity** field, select whether the agent is to be taken offline on every detection, or only above a specified threshold.
        4.  Select a follow-up action in the **Do this** cell, after the agent is taken offline:
            -   Create a ticket: Opens a ticket in the indicated group's queue.
            -   Notify: Sends a notification to the user.
        5.  Select the **Publish** button to publish the policy.
    -   An explicit block:
        1.  Select whether the block is to apply to a user or a department in the **Who** field.
        2.  Select what is being blocked in the **What** field, either an AI agent, a model, or a domain.

            When selecting an AI agent, configure a filter for the field values that create the block, as needed.

        3.  Select a follow-up action of **Notify** to send a notification to the user, in the **Add follow-up** drop down.
        4.  Select the **Publish** button to publish the policy.

## Result

-   The action to be taken appears in the **Policy summary** cell.
-   The policy is synchronized with the Agent Client Collector policies, and appears in the list of Agent Client Collector policies. Agent Client Collector invokes the policy and takes the indicated action.

