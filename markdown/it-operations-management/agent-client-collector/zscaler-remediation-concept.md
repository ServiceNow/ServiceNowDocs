---
title: Perform Zscaler remediation
description: If the Zscaler application installed on your Windows or macOS agent is not running efficiently, you can stop and start the app. This process is called remediation. Running remediation automatically creates an incident on the agent. You can also view Zscaler statuses on the Zscaler dashboard as a graph.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Perform Zscaler remediation

If the Zscaler application installed on your Windows or macOS agent is not running efficiently, you can stop and start the app. This process is called **remediation**. Running remediation automatically creates an incident on the agent. You can also view Zscaler statuses on the Zscaler dashboard as a graph.

By default, the **Zscaler Monitoring Policy** monitoring check runs every 30 minutes to check the status of the Zscaler app running on your agent. The Zscaler monitoring policy contains the following checks:

-   **zscaler-monitoring-check**: Checks the status of the Zscaler app running on your agent.
-   **zscaler-remediation-check**: Invoked only when the Zscaler app is not running efficiently. This check shuts down and restarts the app, and automatically creates an incident.

    Only one incident is created every 24 hours for a Zscaler app that does not remediate properly. For example, if the remediation check runs multiple times on an agent, new remediation records are created which are associated with the same incident until 24 hours have passed, at which time a second incident is created. When the Zscaler app restarts successfully, the incident closes.

    Zscaler remediation produces the following output:

    -   Amount of data produced per remediation: 2KB
    -   Maximum number of remediations that can run in a day: 48 \(one every 30 minutes\)
    -   Maximum amount of data produced by a single agent, per day: 96KB
    -   Maximum amount of data produced by a 20K agents, per day: 1.92GB

-   **[Check Zscaler remediation](../task/zscaler-check-remediation.md)**  
Verify that Zscaler remediation stops and starts the Zscaler app after the remediation monitoring check fails.
-   **[Use the Zscaler dashboard](../task/zscaler-dashboard.md)**  
Use the Zscaler dashboard to view Zscaler monitoring and remediation statuses in graph format.

**Parent Topic:**[Agent Client Collector Framework](acc-framework-landing-page.md)

