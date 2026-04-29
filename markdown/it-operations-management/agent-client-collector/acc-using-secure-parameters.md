---
title: Secure parameters in Agent Client Collector
description: Secure parameters in Agent Client Collector \(ACC\) refers to securely passing sensitive data, such as user names, passwords, and API keys, during check execution, without exposing the sensitive data in the command line. Parameters are passed to the script through standard input \(STDIN\), hiding them from logs or any process that might capture command-line arguments.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Secure parameters in Agent Client Collector

Secure parameters in Agent Client Collector \(ACC\) refers to securely passing sensitive data, such as user names, passwords, and API keys, during check execution, without exposing the sensitive data in the command line. Parameters are passed to the script through standard input \(STDIN\), hiding them from logs or any process that might capture command-line arguments.

Depending on the coding language in use, implementation of secure parameters may vary. For example, in Linux’s Bash, the `read` command \(`read <variable_name>`\) is used, populating `<variable_name>` with the value entered in STDIN.

## Secure parameters data flow

1.  Create secure parameters: Define secure parameters in the instance, referencing credentials that need protection \(such as usernames and passwords\). For details, see [Create secure parameters for a check](../task/acc-create-secure-params.md).
2.  Configure secure parameters: Set an **Order** value to determine the sequence in which credentials are passed to the standard input.
3.  Pass credentials: Transfer credentials from the MID Server to the agent, based on the check to which they are assigned. When the check executes, the agent passes the secured parameters to the script using STDIN, in the order specified by the **Order** value configured in the instance.
4.  Execute the check: Upon execution, the agents send the secure parameters to the script via STDIN, following the specified order.
5.  Run the script: The script retrieves and uses the secure parameters from STDIN to execute with the secured credentials.

## Secure parameters benefits

-   Enhanced security: Passing sensitive data like usernames and passwords directly in the command line is a security threat, as they could be exposed to unauthorized access or malicious users. Secure parameters ensure that such data is securely handled and hidden from view.
-   Prevent data exposure: When using secure parameters, the credentials are not written in plain text in the command line, avoiding the risk of them being captured in logs or process listings.
-   Data flow control: Secure parameters enable controlled and customizable passing of credentials to the script, ensuring the correct handling and timing of sensitive information.

