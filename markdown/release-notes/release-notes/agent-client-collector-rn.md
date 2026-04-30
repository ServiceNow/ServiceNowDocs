---
title: Agent Client Collector release notes
description: The ServiceNow Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Agent Client Collector release notes

The ServiceNow® Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Zurich release.

## Agent Client Collector highlights for the Zurich release

-   Discover TLS/SSL certificates using Agent Client Collector for Visibility - Content certificate Discovery.
-   Enhance data collection by disabling only those checks with high resource usage, allowing data collection to continue for other checks.
-   Improve troubleshooting capabilities by viewing errors that occur before and after the registration process in the ServiceNow instance.
-   Use file-based Discovery in a macOS environment.

See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** Agent Client Collector is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

**Agent Client Collector Framework**

-   **Upgrade MID-less agents**

    Starting in version 6.0.0, perform selective and high-volume upgrades on ACC agents when not using a MID Server by using products such as DEX and ACC-VC.

-   ****

    Starting in version 6.0.0, verify that an agent is functioning properly by performing a self-test on the agent.

-   ****

    Starting in version 6.0.0, view a list of agents and their statuses on the ACC Workspace dashboard.

-   **Use improved debug logging**

    Starting in version 6.0.0, benefit from enhanced debug logging by sending all debug statements to a log file

-   **[Manage Agent Client Collector certificates](https://www.servicenow.com/docs/access?context=acc-yml-options&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 5.0, configure a schedule by which to rotate Agent Client Collector certificates which enable communication between agents and ITOM Cloud Services. Rotating certificates ensures that when a certificate expires, a new certificate is in place.

-   **[Perform high-volume Agent Client Collector upgrade in a macOS environment](https://www.servicenow.com/docs/access?context=acc-high-volume-upgrade&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 5.0, upgrade large numbers of Agent Client Collector agents at a time that are running on macOS. This extends the existing high-volume upgrade capabilities available for Windows and Linux in the 4.3.0 release.

-   **[Use an IMDSv2 endpoint for metadata discovery](https://www.servicenow.com/docs/access?context=acc-configure-websocket-endpoint&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 5.0, the IMDSv2 endpoint for metadata discovery is invoked when using Agent Client Collector in an AWS EC2 environment.

-   **[Use enhanced errors and diagnostics to troubleshoot issues with servers and endpoints](https://www.servicenow.com/docs/access?context=view-agent-errors&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 5.0, view errors that occur before or after the registration process when Agent Client Collector connects to the instance. This provides enhanced debugging capabilities by enabling you to view issues in the instance, without requiring direct access to the agent logs.

-   **[Disable checks using heavy system resources while in CPU protection mode](https://www.servicenow.com/docs/access?context=checks-policies&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 5.0, disable only those checks that are causing high CPU usage while in CPU protection mode. It is still possible to disable all checks and completely stop data collection while in CPU protection mode.

    In a Windows environment, Agent Client Collector has improved the accuracy of how check CPU usage is monitored.

-   **[Configuration data files size limit](https://www.servicenow.com/docs/access?context=acc-config-data-files&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 5.0, configuration data files have a maximum size of 10MB.

-   **[Configure Agent Client Collector with proxy auto-configuration \(PAC\) files](https://www.servicenow.com/docs/access?context=proxy-agent&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 5.0, enable easier connection of Agent Client Collector to a proxy server by using a proxy auto-configuration \(PAC\) file.


**Agent Client Collector Monitoring**

-   ****

    Starting in version 3.15.0, GCP checks provide added support to configure metrics through a configuration file in JSON format.


-   **Monitor Linux events**

    Starting in version 3.15.0, monitor Linux events using Linux event checks.


**Agent Client Collector for Visibility - Content**

-   **Discover MSSQL components using ACC-VC**

    Starting in version 1.5.0, use ACC-VC to discover MSSQL components in your environment.

-   **Discover software information with ACC-VC using SWID tags**

    Starting in version 1.5.0, gather software information with ACC-VC using software identification \(SWID\) tags on an agent and a ServiceNow® instance.

-   **[Run certificate Discovery using Agent Client Collector for Visibility - Content](https://www.servicenow.com/docs/access?context=run-cert-discovery-accvc&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 1.3.0, use the Agent Client Collector for Visibility - Content to discover TLS/SSL certificates used by the ports running on the server's configuration items \(CIs\). Certificate Inventory and Management uses the certificate data to manage the TLS/SSL certificate life cycle.

-   **[File-based Discovery is supported in a macOS environment](https://www.servicenow.com/docs/access?context=file-based-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 1.3.0, use File-based Discovery in a macOS environment.

-   **[Collect metrics using non-osqueryd data collection](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 1.3.0, collect data more efficiently by invoking non-osqueryd data collection.


## Deprecations

Agent Client Collector Security Incident Response is no longer supported. For details on replacement options, see the [Deprecation guidance for Agent Client Collector Security Incident Response \[KB2249776\] article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2249776) in the Now Support Knowledge Base.

## Activation information

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

## Related ServiceNow applications and features

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Agent Client Collector works within an instance on which Event Management is installed to monitor infrastructure components. Agent Client Collector and Event Management share some connectors that pull metric data and events from the same data sources.

-   **[Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The Health Log Analytics application predicts IT issues before they impact users. The application helps you to solve issues faster by ingesting, analyzing, and correlating machine-generated log data in real time.


**Parent Topic:**[ITOM AIOps release notes](itom-health-rn.md)

