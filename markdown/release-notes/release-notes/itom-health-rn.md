---
title: ITOM Health release notes
description: The ServiceNow ITOM Health product includes the Event Management, Agent Client Collector, Health Log Analytics, and Service Reliability Management applications. With ITOM Health, you can track and maintain the health of the services in your organization. ITOM Health was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
---

# ITOM Health release notes

The ServiceNow® ITOM Health product includes the Event Management, Agent Client Collector, Health Log Analytics, and Service Reliability Management applications. With ITOM Health, you can track and maintain the health of the services in your organization. ITOM Health was enhanced and updated in the Xanadu release.

## ITOM Health highlights for the Xanadu release

[Agent Client Collector](agent-client-collector-rn.md) highlights:

-   Configure the agent log level from the instance without needing to access the `acc.yml` configuration file.
-   Ensure secure agent connections by adding a self-signed certificate.
-   Gather expanded information on your Linux and Windows servers by using expanded Linux and Windows checks.

[Health Log Analytics](health-log-analytics-rn.md) highlights:

-   Enhance your system with the latest updates: Security fixes; Filebeat, Elasticsearch, and Microsoft Azure Event Hubs data input updates; Java JDK 17 update and support, and dependency upgrades.
-   Stream system logs from Glide to Health Log Analytics using the Glide Syslog data input.

[Event Management release notes](event-management-rn.md) highlights:

-   View configuration item \(CI\) information on the preview panel in Express List.
-   Optimize alert resolution with Now Assist AI-driven investigation of past related incidents.
-   Generate an alert group description in Express List using Now Assist.
-   Launch an alert analysis from the Now Assist panel.

**Important:** [Agent Client Collector](agent-client-collector-rn.md) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ITOM Health to Xanadu

Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

## New in the Xanadu release

-   **[Load the allow list only from the configuration file](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Enhance your security by loading the allow list from the configuration file and ignoring the allow-list parameters.

-   **[Configure the agent log level from the instance](https://www.servicenow.com/docs/access?context=set-agent-log-level&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Configure the agent log level directly from the ServiceNow® instance without needing to access the `acc.yml` configuration file.

-   **[Ensure secure agent connections](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Ensure that your agent connections are secure by adding a self-signed certificate to your operating system's truststore. Adding a certificate to the truststore verifies that the certificate is authentic.

-   **[Use the new application Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Use the Service Reliability Management application to respond, collaborate, track, and self-remediate when working on alerts and incidents.

-   **[Configure the Dynatrace connector instance](https://www.servicenow.com/docs/access?context=configure-dynatrace-connector&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, Event Management supports collecting raw metric data collection using the Dynatrace metric connector.

-   **[Enable expanded processing for the MID server on Network Interface Controllers \(NICs\) during keepalive operation](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, benefit from enhanced stability when running a keepalive operation. You can use the enhanced MID Server capability to configure the number of Network Interface Controllers \(NICs\) that can be monitored by a keepalive operation.

-   **[Stream log data from the System Log table in Glide to the Health Log Analytics AI engine](https://www.servicenow.com/docs/access?context=hla-data-input-glide-syslog&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Use the Glide Syslog data input to stream log messages from the System Log table \(Glide Syslog\) in Glide to the Health Log Analytics AI engine \(Occultus\).

    **Note:** Only a single Glide Syslog data input can exist in the system. This data input doesn't run on a MID Server.

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Map current alert fields values to specified new values through the **Change alert values** option, in the "If these conditions are met, don't add an alert in ServiceNow" section.

-   **[Group automation](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Track and optimize alert grouping efficiency through a new header displaying key details from the Test Automation section, including total alerts, alert groups, ungrouped alerts, and compression.

-   **[View data on configuration items on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-ci-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents related to the current alert. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


## UI changes

-   **[Integrations Launchpad enhancements](https://www.servicenow.com/docs/access?context=review-integration-config-health&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The **Related events** tab has been renamed **Events**.

    The banner message has been updated, with a highlighted background added to emphasize the change.

    The Health state has been renamed Integration Stats.

    The Alert compression rate has been renamed Grouping ratio.

-   **[Alert automation enhancements](https://www.servicenow.com/docs/access?context=sow-itom-alert-automation&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The text on the landing pages for all automations has been updated to provide clearer context for each automation.

    The text below the "If these conditions are met, don't add an alert in ServiceNow" section has been removed.

    In Group automation, in the Simulation section, **Re-run test** has been renamed **Re-run simulation**.


## Changed in this release

-   **Alert automation enhancements**

    In Group automation, in the Simulation section, **Re-run test** has been renamed **Re-run simulation**.

    The **Active** toggle switch has been replaced with a check box.

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    A new section, **And finally**, featured two radio buttons, **Run other enrich alert automations** and **Don't run other enrich alert automations**, which replace the previous **Continue running automations of this type** toggle switch. Although this section is new, the functionality is unchanged. Selecting **Run other enrich alert automations** continues running automations with the same filter conditions, while **Don't run other enrich alert automations** halts additional automations after execution except for those owned by other assignment groups.

-   **[Associate services to use in Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-add-service&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    System admins can select any supported service and associate it to use in Service Reliability Management regardless of the owner or support group configurations.


## Deprecations

The following dashboards have been deprecated:

-   Event Management scorecards
-   Event Management insights
-   Event Management overview
-   Health Log Analytics Overview

Service Management Dashboard is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process \[KB0867184\] article in the Now Support knowledge base.

## Activation information

ITOM Health is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). To work with Health Log Analytics, you must purchase ITOM Predictive AIOps, a more comprehensive ITOM Health package. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The ITOM Visibility product consists of [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US), [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US), Certificate Inventory and Management, Service Graph Connectors, CMDB 360, and Firewall Audits and Reporting. Discovery and Service Mapping provide a unified, connected view of your entire IT network and the services that it supports.

-   **[ITOM Optimization](https://www.servicenow.com/docs/access?context=itom-optimization-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    ITOM Optimization contains the [Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) feature. By using this feature, you can provision a private and public cloud infrastructure and services to achieve consistent management and cost visibility.

-   **[Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Service Operations Workspace ITSM and ITOM are integrated to streamline incident and operations management. ITSM focuses on managing service incidents, requests, and changes, while ITOM is responsible for operational tasks like monitoring infrastructure, handling alerts, and maintaining system health. Together, they provide a unified workspace that enables seamless collaboration between service management and operations teams, improving efficiency in resolving issues and maintaining service performance.

-   **[Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The ServiceNow® Now Assist for IT Operations Management \(ITOM\) application analyzes alerts in Event Management. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.


-   **[Event Management release notes](event-management-rn.md)**  
The ServiceNow® Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management provides alert aggregation for discovered services, application services, and automated alert groups. Event Management was enhanced and updated in the Xanadu release.
-   **[Health Log Analytics release notes](health-log-analytics-rn.md)**  
The ServiceNow® Health Log Analytics application helps you predict IT issues before they impact users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you of a possible issue. Health Log Analytics was enhanced and updated in the Xanadu release.
-   **[Agent Client Collector release notes](agent-client-collector-rn.md)**  
The ServiceNow® Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Xanadu release.
-   **[Service Reliability Management release notes](service-reliability-management-rn.md)**  
The ServiceNow® Service Reliability Management \(SRM\) application helps your organization to respond, collaborate, track, and self-remediate when working on alerts and incidents. Service Reliability Management is a new application in the Xanadu release.

**Parent Topic:**[IT Operations Management release notes](it-operations-management-rn-landing.md)

