---
title: Agent Client Collector release notes
description: The ServiceNow Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Agent Client Collector release notes

The ServiceNow® Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Xanadu release.

## Agent Client Collector highlights for the Xanadu release

-   Ensure secure agent connections by adding a self-signed certificate.
-   Enhance check functionality by using expanded Linux and Windows checks, enabling you to gather additional information on your Linux and Windows servers.
-   Upgrade the Cloud Native Operations for Visibility Informer from the ServiceNow instance.
-   Store Instance credentials in the Microsoft Azure Vault when Informer uses Azure Kubernetes Engine \(AKS\).
-   Enjoy multi-architecture support for docker image.

See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) for more information.

**Important:** Agent Client Collector is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Load the allow list only from a configuration file](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Enhance system security by loading the allow list from the file specified in the **allow-list** parameter of the configuration file while ignoring the allow lists that are bundled with the plugins.

-   **[Configure agent log level from the instance](https://www.servicenow.com/docs/access?context=set-agent-log-level&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Configure the agent log level from the ServiceNow instance without having to access the `acc.yml` configuration file.

-   **[Ensure secure agent connections](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Ensure that your agent connections are secure by adding a self-signed certificate to your operating system's truststore, which verifies that the certificate is authentic.

-   **[Update existing assets](https://www.servicenow.com/docs/access?context=agent-plugins-remove&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Update your Agent Client Collector \(ACC\) plugins to the latest version by removing your existing plugins before reinstalling.

-   **[Use expanded Linux and Windows checks](https://www.servicenow.com/docs/access?context=linux-checks-policies&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Enable enhanced check functionality by using the expanded Linux and Windows checks provided with the system.

-   **[Upgrade Agent Client Collector for Kubernetes – Visibility Informers remotely](https://www.servicenow.com/docs/access?context=cnov-informer-upgrade-remote&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, upgrade Informer pods in Kubernetes clusters remotely from the ServiceNow instance to avoid dependence on your Kubernetes admin.

-   **[Override Informer parameters from the Instance](https://www.servicenow.com/docs/access?context=cnov-params-override&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, control CNO for Visibility Informer execution parameters from the ServiceNow instance to avoid dependence on your Kubernetes admin.

-   **[Store Instance credentials in Microsoft Azure Vault when Informer uses Azure Kubernetes Service \(AKS\)](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, if your organization uses AKS, you can store the secret in the Microsoft Azure Vault. The Informer then pulls the ServiceNow credentials for accessing your instance from the Azure Vault.

-   **[Enable Informer to connect to the instance using OAuth2.0 authorization](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, the Informer can use OAuth2.0 authorization to connect to the ServiceNow instance for enhanced security.

-   **[Enable expanded processing for the MID server on Network Interface Controllers \(NICs\) during keepalive operation](https://www.servicenow.com/docs/access?context=acc-yml-options&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, benefit from enhanced stability when running a keepalive operation by using the enhanced MID Server capability to configure the number of Network Interface Controllers \(NICs\) that can be monitored by a keepalive operation.

-   **[Upgrade Agent Client Collector manually on a macOS system](https://www.servicenow.com/docs/access?context=acc-macos-upgrade-manual&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, run the consolidated upgrade procedure manually for the Agent Client Collector in a macOS environment.

-   **[Configure the Dynatrace connector instance](https://www.servicenow.com/docs/access?context=configure-dynatrace-connector&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.6.3, Event Management supports collecting raw metric data collection using the Dynatrace metric connector

-   **[Consolidate agent errors](https://www.servicenow.com/docs/access?context=view-agent-errors&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 4.1.0, view errors for all agents on the Agent Error Messages page. Additionally, you can view errors per individual agent by selecting the agent and selecting the **ACC Error Messages** tab .

-   **[Use Linux commands to enable additional system capabilities beyond your permission level](https://www.servicenow.com/docs/access?context=acc-installation&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 4.1.0, use Linux commands to grant enhanced permissions, which are enabled once the installation `.exe` file is executed. These enhanced capabilities are provided securely, ensuring that there is no security risk to your environment.

-   **[Use the new Windows event check for enhanced event details](https://www.servicenow.com/docs/access?context=windows-checks-policies&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.12.0, use the new Windows event check to collect and filter Windows event logs.

-   **[Use the network port check to determine port availability](https://www.servicenow.com/docs/access?context=network-port-checks-policies&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.12.0, use the Network port check to create events for all ports of a specified host address, which indicates whether each port is available or in use.

-   **[Enjoy multi-architecture support for docker image](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.9.0 \(Informer version 2.3.0\), the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one.

-   **[Change the Informer's extensibility settings from the instance](https://www.servicenow.com/docs/access?context=cnov-params-override&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.9.0 \(Informer version 2.3.0\), update the Informer's extensibility configuration directly from the Instance using the **Additional resources ConfigMap** parameter. By providing a JSON map with keys such as `resources`, `mappings`, and `mappings_oob`, you can instruct Cloud Native Operations for Visibility to retrieve additional information. If one of these keys exists and the system finds a change, it patches the ConfigMap and restarts the Informer.

-   **[View the OpenShift version in the Cluster version field on the Kubernetes Cluster CI](https://www.servicenow.com/docs/access?context=cnov-deploy-install&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 3.9.0 \(Informer version 2.3.0\), see the OpenShift version and the Kubernetes Cluster version in one place. OpenShift operates on top of Kubernetes, so there's an OpenShift version and a Kubernetes Cluster version. By installing the Informer with the **--set openShift=true** flag, the system adds the OpenShift version number to the **cluster\_version** field on the Kubernetes Cluster CI in addition to the Kubernetes Cluster version.


## Changed in this release

-   **Use the updated Windows event check**

    Starting in version 3.12.0, the Windows event check `os.windows.check-event-log` has been renamed `os.windows.check-event-log-count` and has enhanced data gathering capabilities.


-   **Updated plugin dependency**

    Starting in version 4.1.0, the Service Error Management plugin is dependent on the ACC-F scoped app. The plugin gets installed automatically when the customer installs the ACC-F scoped app from the ServiceNow store.

-   **[New allow list parameter for checks running in shell execution mode](https://www.servicenow.com/docs/access?context=check-definition-form&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Starting in version 4.1.0, when running a check in with execution mode \(**Exec Mode**\) set to **shell**, add the **allow\_shell** parameter and set it to **true** for the allow list entry corresponding to the check.


## Activation information

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

## Related ServiceNow applications and features

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Agent Client Collector works within an instance on which Event Management is installed to monitor infrastructure components. Agent Client Collector and Event Management share some connectors that pull metric data and events from the same data sources.

-   **[Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The Health Log Analytics application predicts IT issues before they impact users. The application helps you to solve issues faster by ingesting, analyzing, and correlating machine-generated log data in real time.


**Parent Topic:**[ITOM Health release notes](itom-health-rn.md)

