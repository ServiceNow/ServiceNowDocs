---
title: ITOM Visibility release notes
description: The ServiceNow ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# ITOM Visibility release notes

The ServiceNow® ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Yokohama release.

## ITOM Visibility highlights for the Yokohama release

-   Discovery and Service Mapping Patterns: Gain enhanced visibility into your AWS cloud services with 27 additional patterns starting with store version 1.25.0.
-   Starting with store version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility - Content. The CNO for Visibility feature has been extracted from Agent Client Collector for Visibility - Content and is now a separate application.
-   Starting with Service Graph Connector for GCP store release 1.8, Service Graph Connector for AWS store release 2.9, and Service Graph Connector for Microsoft Azure store release 1.11, you can use Service Graph Connectors to ingest data into the Configuration Management Database \(CMDB\) from third-party sources.
-   Starting with store version 1.8.0, Discovery admins gain improved visibility into discovery issues and can address root causes using anomaly detection in the Discovery Admin Workspace.

See [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** Discovery and Service Mapping Patterns is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ITOM Visibility to Yokohama

3DES support is planned for permanent removal from the MID Server for MID Servers with SSH-based Discovery or SSH-based integrations. For more information, see [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950).

After upgrading to Yokohama, a Fix Script named "Add Explicit Public SNMP Credential" might create a public SNMP credential in Production instances. This could lead to unnecessary records via Discovery. The Fix Script is present in Yokohama instances, including OOB. Before applying the upgrade of Discovery core, Yokohama version, verify the fix script behavior in a sandbox environment. Remove the public SNMP credentials if not required.

## New in the Yokohama release

-   **[Discover additional AWS Services using Patterns](https://www.servicenow.com/docs/access?context=aws-service-discovery-pattern&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**
    -   Starting with store version 1.25.0, Discovery and Service Mapping Patterns discovers 27 additional AWS cloud services.
    -   Starting with store version 1.27.0, Discovery and Service Mapping Patterns discovers 7 additional AWS cloud services.
-   **[Discover products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=available-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Discover the following products using Discovery and Service Mapping Patterns version 1.27.0:

    -   [NVIDIA GPUs](https://www.servicenow.com/docs/access?context=nvidia-gpu-discovery-pattern&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [Microsoft SQL Always On availability groups](https://www.servicenow.com/docs/access?context=mssql-data-collected-pattern&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [Azure tenants and management groups](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [AWS Application Load Balancer targets](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [AWS web ACL](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [AWS Systems Manager \(SSM\) agents](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   [Tag collection for Azure VM instance - Uniform scale set](https://www.servicenow.com/docs/access?context=AzureVMScaleSetInstance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
-   **[Automatically generate a Certificate Signing Request](https://www.servicenow.com/docs/access?context=request-new-csr-automated&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Generate a Certificate Signing Request and a private key with the Employee Center experience, starting with version 3.6.0 of Certificate Inventory and Management.

-   **[Use Service Graph Connectors for extended discovery](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Service Graph Connectors are a collection of predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources.

    -   Discover device details from Chromebook and ingest them into the CMDB by using Service Graph Connector for Google Console store version 1.8.
    -   Discover data from public cloud instances and resources in AWS, Azure, and GCP environments and ingest them into the CMDB by using Service Graph Connector for Wiz. 
-   **[Detect anomalies in Discovery schedules](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-diagnostics&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting with Discovery Admin Workspace version 1.8.0, machine learning \(ML\) or statistical methods can detect anomalies in Discovery schedules and display this data in dashboards for admins. It identifies unusual behaviors like failed runs, significant deviations from user-defined thresholds for high error counts, longer discovery status duration, and fewer discovered Configuration Items \(CIs\) or Cloud resources. The ML-based approach to this feature is enabled by default. Thresholds are configurable via the new Settings page, and the results will be shown throughout the workspace.

-   **[Cloud-based Discovery schedules](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-schedules&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting with version 1.8.0, Cloud-based discovery scheduling and reporting is available in Discovery Admin Workspace.

-   **[Configure Discovery to use Event Framework](https://www.servicenow.com/docs/access?context=t_ConfigureDiscoveryEventFramework&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting with version 1.9.0, Discovery jobs can be configured to use an event-based system, reducing database activity by queuing and processing events at regular intervals with priority and memory monitoring.


## Changed in this release

-   **[Name suggestions for application service candidates](https://www.servicenow.com/docs/access?context=app-services-name-suggestions&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Experience more accurate name suggestions for application service candidates based on Service Fingerprints in Service Mapping Plus store version 1.15.0.

-   **[Limits in Service Mapping](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Limits in Service Mapping prevent the disabling or deletion of jobs scheduled for the Checkpoint Reaper or the Service Model's Blob Reaper.

-   **[Limits in tag-based Service Mapping](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping-plus&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting with version 1.15.2, experience improved performance in Service Mapping. A new property limits the creation of tag-based service candidates to 200 per service family.

-   **[Name update in Service Mapping](https://www.servicenow.com/docs/access?context=create-it-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**
    -   Application Services in the navigation menu has been renamed Service Instances.
    -   The label for the \[cmdb\_ci\_service\_auto\] table has been changed from Application Service to Service Instance.
-   **[Discovery status monitoring](https://www.servicenow.com/docs/access?context=c_DiscoveryStatus&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Discovery schedules that have no status updates for over a defined number of minutes are analyzed automatically by the Discovery Status Monitor job. By default, this job applies to Discovery schedules that discover configuration items.


## Deprecations

-   **[Application/Plugin Deprecation Process \[KB0867184\]Discovery CLI](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)**

    Starting with version 3.5.0, Discovery CLI is no longer available in the Pattern Designer Enhancements Store App.


## Activation information

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

## Related ITOM applications and features

-   **[ITOM Health](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The ServiceNow® ITOM AIOps product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

    Event Management gathers alerts from infrastructure events that both third-party monitoring tools and the ServiceNow® internal agent capture. Event Management uses IT-related information that ServiceNow® Discovery gathers so it can map alerts to configuration items. Based on the collected information, Event Management then provides dashboards that show a consolidated view of all service-impact events.

    The Agent Client Collector application enables you to do the following:

    -   Monitor your service availability.
    -   Examine the health and performance of your environment.
    -   Ensure that your infrastructure and its applications are running properly.
    Agent Client Collector collects events and metrics. It runs in either a Windows or Linux environment.

-   **[ITOM Optimization](https://www.servicenow.com/docs/access?context=itom-optimization-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    ITOM Optimization provides automation for the cloud workflows used to manage the cloud resources throughout their life cycle. It enables certified and enterprise-compliant cloud deployment, cost visibility, and other cloud management processes.

-   **[ITOM Licensing](https://www.servicenow.com/docs/access?context=itom-su-licensing-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    ITOM SU Licensing has been rebranded as ITOM/OT SU Licensing. ITOM/OT SU Licensing calculates and displays the usage of ITOM subscriptions based on subscription units. It enables you to access a comprehensive overview of the total number of licenses allocated to applications and configuration items \(CIs\), while offering an advanced feature set that provides visibility into the specific CIs covered by your licenses. You can view the subscription breakdown for ITOM AIOps, ITOM Visibility, ITOM Optimization, and ITOM Cloud Accelerate. For more details, see [View which CIs have an ITOM license](https://www.servicenow.com/docs/access?context=itom-licensing-count&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).


**Parent Topic:**[IT Operations Management release notes](it-operations-management-rn-landing.md)

