---
title: Exploring MID Server
description: MID Server acts as the mediator between the network and the instance. MID Servers are used by other applications to connect to the instance.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Exploring MID Server

MID Server acts as the mediator between the network and the instance. MID Servers are used by other applications to connect to the instance.

## MID Server overview

MID Servers are installed on hosts in a network by administrators, and the MID Servers are used by other applications to communicate with the instance or function within the network. For example, a MID Server configured with Discovery scans items in the network from that MID Server host. Once it collects the Discovery data, the MID Server securely transfers the data through the network firewall to the instance.

To set up a MID Server, the network must be prepared to access the instance and download site. There are several installation procedures depending on the host operating system and scale of deployment. Once installed, MID Servers can be configured with many capabilities and features to support applications.

After configuring your MID Server, you can add security by encrypting MID Server parameter values in the `config.xml` file. Encryption protects data that the MID Server returns to the ECC Queue. Other available security options include the authorization of SOAP requests, restricting access to the MID Server configuration file, and establishing secure socket layer \(SSL\) connections.

![MID Server overview diagram.](../image/mid-server-overview-diagram.png)

## Upgrading the MID Server

The MID Server checks with the instance periodically to see if an upgrade is necessary. If the MID Server detects that a new version is available for upgrade, it downloads the installer from `install.service-now.com` and runs the package automatically. You can also elect to upgrade the MID Server manually. See [MID Server upgrades](c_UpgradeAndTestMIDServer.md) for details.

## Resolving MID Server issues

You can search the HI Knowledge Base for troubleshooting articles or monitor the MID Server status and track active issues from within the instance. Many articles on resolved MID Server issues have been collected on [Servicenow MID Server Landing page \[KB0960404\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0960404). For more information about common resolution procedures, see [Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md).

## ServiceNow applications that use the MID Server

-   [Discovery](https://www.servicenow.com/docs/access?context=discovery-setup&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Orchestration](https://www.servicenow.com/docs/access?context=c_OrchestrationMID&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Service Mapping](https://www.servicenow.com/docs/access?context=service-mapping-setup&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Event Management](https://www.servicenow.com/docs/access?context=c_EMConfiguration&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Operational Intelligence](https://www.servicenow.com/docs/access?context=get-started-metrics&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Cloud Management](https://www.servicenow.com/docs/access?context=cloud-configuration&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Cloud Cost Management](https://www.servicenow.com/docs/access?context=cloud-insights-landing-page&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
-   [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

## External applications that use the MID Server

-   [Import Sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Microsoft SMS/SCCM](https://www.servicenow.com/docs/access?context=c_MicrosoftSCCMIntegration&version=australia&pubname=australia-platform-administration&ft:locale=en-US)
-   [LANDesk Maintenance Suite](https://www.servicenow.com/docs/access?context=c_CSDExtensionFramework&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Microsoft System Center Operations Manager \(SCOM\)](https://www.servicenow.com/docs/access?context=t_EMConfigureSCOMConnectorInstance&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Microsoft MIIS](https://www.servicenow.com/docs/access?context=c_UsingADAMSyncToPopulateADAM&version=australia&pubname=australia-platform-security&ft:locale=en-US)

## Begin MID Server installation

Continue to [Configuring MID Server](configure-mid-server.md) to find procedures on preparing the network, installing MID Servers, and configuring them.

