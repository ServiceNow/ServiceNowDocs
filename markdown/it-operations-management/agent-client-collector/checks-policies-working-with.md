---
title: Working with checks and policies
description: You can perform actions on checks and policies to enhance the monitoring of your system's devices.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Working with checks and policies

You can perform actions on checks and policies to enhance the monitoring of your system's devices.

-   **[Create secure parameters for a check](../task/acc-create-secure-params.md)**  
When creating a check definition or check instance, you can configure the parameters you want to be secured when the agent executes the check. During check execution, the secured parameters are obfuscated, securing their information. Only credential information is obfuscated.
-   **[Create a check type](../task/acc-api-check-type.md)**  
Create a check type to execute the `osquery` command on the Agent.
-   **[Create a check definition](../task/acc-api-check-def.md)**  
Create a check definition to execute the `osquery` command on the Agent.
-   **[Enable checks from the community for Agent Client Collector](../task/acc-custom-checks.md)**  
You can take checks from the github community and customize them for use in the Agent Client Collector \(ACC\), or you can compose your own scripts. Create a plugin with the customized Sensu check and install it on a ServiceNow instance.

**Parent Topic:**[Agent Client Collector Framework](acc-framework-landing-page.md)

