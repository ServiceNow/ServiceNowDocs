---
title: ITOM Visibility release notes
description: The ServiceNow ITOM Visibility application provides a unified, connected view of your entire IT network and the services that it supports. ITOM Visibility was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
---

# ITOM Visibility release notes

The ServiceNow® ITOM Visibility application provides a unified, connected view of your entire IT network and the services that it supports. ITOM Visibility was enhanced and updated in the Xanadu release.

## ITOM Visibility highlights for the Xanadu release

-   Elevate the Discovery Admin experience with Discovery Admin Workspace. Benefit from a unified workspace for configuring Discovery, tracking progress, and managing errors, with diagnostic tools that provide insights into discovered data.
-   Enrich your CMDB with a larger number of configuration items using ITOM Content Service.
-   Create application services with CMDB based mapping.
-   Avoid dependence on your Kubernetes admin by upgrading Cloud Native Operations Informer pods and modifying Informer execution parameters directly from the instance.
-   Enjoy multi-architecture support for docker image in Cloud Native Operations for Visibility.

See [IT Operations Management](https://www.servicenow.com/docs/access?context=r_ITOMApplications&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) for more information.

**Important:** Discovery and Service Mapping Patterns is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ITOM Visibility to Xanadu

For an improved Service Mapping experience, install Service Mapping Plus version 1.13.0 from the ServiceNow® Store.

Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

## New in the Xanadu release

-   **[Use Discovery Admin Workspace features to jumpstart discovery implementation.](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**
    -   View discovery trends and tasks and access relevant ITOM Visibility apps and information through Discovery Admin Workspace Home.
    -   Gain insights into the performance of all your discoveries through the information in the **Schedules** tab.
    -   Analyze discovery errors and troubleshoot them using information in the **Diagnostics** tab.
    -   Access on-demand reports and optimize discovery operations using information in the**Insights** tab.
-   **[Discover products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=r_SupportedApplications&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Discover the following products through Discovery and Service Mapping Patterns:

    -   [Dell EMC Data Domain storage](https://www.servicenow.com/docs/access?context=emc-data-domain-pattern&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
    -   [Dell EMC PowerMax storage](https://www.servicenow.com/docs/access?context=emc-powermax-discovery-pattern&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
    -   [AWS services in the China region](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\) on the ServiceNow AI Platform Xanadu Patch 3 instance.
    -   [REST-based Fortinet firewall and FortiGate VDOMs](https://www.servicenow.com/docs/access?context=fortinet-fw-vdoms-rest-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\).
    -   [Azure Marketplace](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\). The pattern supports the discovery of the following Azure Marketplace products:
        -   Virtual Machine
        -   SaaS
        -   Azure Application
-   **[Oracle Java process discovery](https://www.servicenow.com/docs/access?context=oracle-glas-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Discover Java processes to comply with Oracle licensing agreements- Use the ITOM Oracle GLAS plugin \(1.8.4\) November 2024 store version to track Java installations and usage.

-   **[MID Server features for better discovery performance](../now-platform-capabilities/mid-server-rn.md)**
    -   Run other applications without storing any credentials on the instance with the Microsoft Azure Key vault.
    -   MID Server supports log file compression. The new log file handler settings are available as MID Server properties on the instance. The compression mode isn't enabled out of the box.
-   **[Use CMDB based mapping to create new application services](https://www.servicenow.com/docs/access?context=cmdb-based-mapping&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Use Automated Service Suggestions and CMDB data instead of the MID Server, to create new application services.

-   **[Use the latest CNO for Visibility features](https://www.servicenow.com/docs/access?context=cnov-configuring&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, benefit from new features in Cloud Native Operations for Visibility.

    -   Upgrade the CNO for Visibility Informer from the ServiceNow instance.
    -   Control Informer execution parameters from the instance.
    -   Store instance credentials in the Microsoft Azure Vault when Informer uses the Azure Kubernetes Engine \(AKS\)
    -   Enable Informer to connect to the instance using OAuth2.0 authorization
-   **[Enjoy multi-architecture support for docker image](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.9.0 \(Informer version 2.3.0\), the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one.

-   **[Change the Informer's extensibility settings from the instance](https://www.servicenow.com/docs/access?context=cnov-params-override&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.9.0 \(Informer version 2.3.0\), update the Informer's extensibility configuration directly from the Instance using the **Additional resources ConfigMap** parameter. By providing a JSON map with keys such as `resources`, `mappings`, and `mappings_oob`, you can instruct Cloud Native Operations for Visibility to retrieve additional information. If one of these keys exists and the system finds a change, it patches the ConfigMap and restarts the Informer.

-   **[View the OpenShift version in the Cluster version field on the Kubernetes Cluster CI](https://www.servicenow.com/docs/access?context=cnov-deploy-install&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.9.0 \(Informer version 2.3.0\), see the OpenShift version and the Kubernetes Cluster version in one place. OpenShift operates on top of Kubernetes, so there's an OpenShift version and a Kubernetes Cluster version. By installing the Informer with the **--set openShift=true** flag, the system adds the OpenShift version number to the **cluster\_version** field on the Kubernetes Cluster CI in addition to the Kubernetes Cluster version.

-   **[Use Service Fingerprints to refine the selection of application service candidates](https://www.servicenow.com/docs/access?context=auto-serv-suggest&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Explore unique, classified components of application service candidates provided by Automated Service Suggestions. By supplying specific information such as the product name and description, gain deeper insights into the most suitable candidate to convert to an application service.


## Changed in this release

-   **[Use the enhanced Shazzam probe to collect data](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-insights&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    View the extended data collected by the Shazzam probe in the Discovery Admin Workspace **Insights** tab.

-   **[Revised Service Mapping roles](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Gain improved visibility of ML-powered candidates in Service Mapping with updated roles:

    -   service\_mapping\_admin replaces sm\_admin.
    -   service\_mapping\_user replaces sm\_user.
-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://www.servicenow.com/docs/access?context=r_SupportedApplications&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Note the following new Pattern extensions and improvements:

    -   [Pure Storage FlashArray](https://www.servicenow.com/docs/access?context=flasharray-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
    -   [Azure SQL license information](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
    -   [Google Cloud Platform \(GCP\) resource inventory discovery](https://www.servicenow.com/docs/access?context=gcp-resource-inventory-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
-   **[Scale up your Azure change processing](https://www.servicenow.com/docs/access?context=azure-change-processing&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Update your CMDB in real time with your Azure cloud resource changes. After upgrading to the enhanced November 2024 Patterns \(1.21.0\) version, run an Azure cloud discovery on all service accounts to ensure receiving all updates.

-   **[Stay informed about Cloud Discovery patterns updates](https://www.servicenow.com/docs/access?context=r_SupportedApplications&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Download and use the Cloud Discovery patterns spreadsheet with the latest up-to-date information on Cloud Discovery patterns, including REST-API permissions.

-   **[Run top-down discovery using Service Mapping integrated with Agent Client Collector](https://www.servicenow.com/docs/access?context=service-mapping-with-acc&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Top-down Service Mapping and Automated Service Suggestions are supported with Agent Client Collector.


## Deprecations

Starting with the Xanadu release, the Discovery Dashboard is no longer part of the Discovery plugin. Use [Discovery Admin Workspace](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) instead.

## Activation information

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

## Related ITOM applications and features

-   **[ITOM Health](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The ServiceNow® ITOM Health product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

    Event Management gathers alerts from infrastructure events that both third-party monitoring tools and the ServiceNow® internal agent capture. Event Management uses IT-related information that ServiceNow® Discovery gathers so it can map alerts to configuration items. Based on the collected information, Event Management then provides dashboards that show a consolidated view of all service-impact events.

    The Agent Client Collector application enables you to do the following:

    -   Monitor your service availability.
    -   Examine the health and performance of your environment.
    -   Ensure that your infrastructure and its applications are running properly.
    Agent Client Collector collects events and metrics. It runs in either a Windows or Linux environment.

-   **[ITOM Optimization](https://www.servicenow.com/docs/access?context=itom-optimization-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    ITOM Optimization provides automation for the cloud workflows used to manage the cloud resources throughout their life cycle. It enables certified and enterprise-compliant cloud deployment, cost visibility, and other cloud management processes.

-   **[ITOM Licensing](https://www.servicenow.com/docs/access?context=itom-su-licensing-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    ITOM SU Licensing has been rebranded as ITOM/OT SU Licensing. ITOM/OT SU Licensing calculates and displays the usage of ITOM subscriptions based on subscription units. It enables you to access a comprehensive overview of the total number of licenses allocated to applications and configuration items \(CIs\), while offering an advanced feature set that provides visibility into the specific CIs covered by your licenses. You can view the subscription breakdown for ITOM Health, ITOM Visibility, ITOM Optimization, and ITOM Cloud Accelerate. For more details, see [View which CIs have an ITOM license](https://www.servicenow.com/docs/access?context=itom-licensing-count&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).


**Parent Topic:**[IT Operations Management release notes](it-operations-management-rn-landing.md)

