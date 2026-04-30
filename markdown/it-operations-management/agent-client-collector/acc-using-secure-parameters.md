---
title: Secure Parameters in the Agent Client Collector
description: Secure parameters can be invoked during check execution to enhance the agent's security and avoid passing sensitive data, such as user name and password, on the command line. To use secured parameters, the check’s script must read from the standard input \(STDIN\).
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Secure Parameters in the Agent Client Collector

Secure parameters can be invoked during check execution to enhance the agent's security and avoid passing sensitive data, such as user name and password, on the command line. To use secured parameters, the check’s script must read from the standard input \(STDIN\).

Depending on the coding language in use, implementation of secure parameters may vary. For example, in Linux’s Bash, the `read` command \(`read <variable_name>`\) is used, populating `<variable_name>` with the value entered in STDIN.

-   **Secure parameters data flow**
    1.  Create a secure parameter in the instance. The secure parameter references credentials to be secured, such as user name and password.

        You configure the secure parameters with an **Order** value, which determines the order in which credentials are sent to the standard input. For details, see [Create secure parameters for a check](../task/acc-create-secure-params.md).

    2.  Credentials are passed via the MID server to the agent, using the check to which the credentials are assigned.
    3.  When the check executes, the agent passes the secured parameters to the script using STDIN, in the order specified by the **Order** value configured in the instance.
    4.  The script retrieves the secure parameters from STDIN.
    5.  The script runs the secure parameters.

