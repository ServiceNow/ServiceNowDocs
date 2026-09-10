---
title: Prepare for agent deployment on a non-persistent virtual desktop infrastructure machine
description: Configure the preliminary settings on an instance to enable using the agent with a non-persistent virtual desktop infrastructure machine \(NPVDI\) machine. NPVDI agents gather data more quickly than traditional agents not enabled for a VPVDI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/npvdi-agent-instance-prep.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Prepare for agent deployment on a non-persistent virtual desktop infrastructure machine

Configure the preliminary settings on an instance to enable using the agent with a non-persistent virtual desktop infrastructure machine \(NPVDI\) machine. NPVDI agents gather data more quickly than traditional agents not enabled for a VPVDI.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Configurations are set on a ServiceNow instance.

**Note:** These configurations need to be set only once per VDI setup. You can deploy multiple VDI agents on a single setup.

## Procedure

1.  Create a registration key marked for light registration.

    1.  Navigate to **All** &gt; **System definition** &gt; **Tables**.

    2.  Access the **sn\_agent\_registration\_key** table.

    3.  Select **New** to create a new registration key.

    4.  Set **light\_registration** to **true**.

2.  Add the static policies you want the VDI agent to run.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **VDI policies**.

    2.  Select **New**.

    3.  Select the policies to be added as a VDI policy in the **VDI policy** field.

        The available policies are published, non-proxy policies.

    4.  Select **Submit**.

3.  Add configuration files to the agent.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **VDI configuration files**.

    2.  Select **New**.

    3.  Select the configuration files to be added to the agent in the **Configuration file** field.

        Configuration files that aren't mapped to a check or policy are added to the agent.

    4.  Select **Submit**.

4.  Grant the user the role of **agent\_client\_collector\_user\_rest**.

    These credentials are used when enabling an NPVDI agent.


## What to do next

Enable an agent to run as an NPVDI agent, as described in [Enable a non-persistent virtual desktop infrastructure \(NPVDI\) agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/enable-npvdi-agent.md).

