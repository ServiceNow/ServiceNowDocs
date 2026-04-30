---
title: Configure Agent Client Collector for use with Service Mapping
description: Configure Agent Client Collector to discover and map application services without having to configure credentials for the MID Server.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-08-03"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure Agent Client Collector for use with Service Mapping

Configure Agent Client Collector to discover and map application services without having to configure credentials for the MID Server.

## Before you begin

Confirm that you have installed both Agent Client Collector for Visibility - Content version 3.5.0 and the Kubernetes Visibility Agent \(KVA\) from the ServiceNow® Store.

Ensure that Agent Client Collector has been configured. For more information, see [Application patterns for the Agent Client Collector](../../agent-client-collector/concept/application-patterns-acc.md).

Verify that agents have the necessary privileges to execute the required application pattern commands for successful completion of top-down discovery. For more information, see [SSH commands requiring a privileged user during probe-based discovery](../../discovery/reference/discovery-ssh-command-require-priv.md) and [SSH commands not requiring a privileged user during probe-based discovery](../../discovery/reference/discovery-ssh-probe-commands.md).

**Important:** This configuration requires a MID Server that is up and running to work correctly. Service Mapping selects the MID Server to which the target agent connects, in order to run commands through the agent.

Role required: service\_mapping\_admin

## About this task

Agent Client Collector enables the discovery and mapping of application services without requiring you to set up credentials for the MID Server. You can deploy both top-down and machine learning-based Service Mapping and benefit from a simplified approach to mapping application services.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  In the System Properties \[sys\_properties\] table, search for the **sa.topdown.mapping\_with\_acc\_mode** property.

3.  Set the property to configure Agent Client Collector for Service Mapping and define the MID Server selection mode for top-down discovery.

    1.  Confirm that the **Type** field value is set to integer.

    2.  Determine how top-down discovery should run by setting the **Value** field value.

        Possible values are:

        -   `0` \(the default\) - Top-down discovery runs using the MID Server exclusively.
        -   `1` - Top-down discovery initially attempts to run using Agent Client Collector. If no agent is available, then it defaults to using the MID Server.
        -   `2` - Top-down discovery runs using Agent Client Collector exclusively. If unsuccessful, the process terminates.

