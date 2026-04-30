---
title: Integration architecture for McAfee ePO
description: The following topic is an overview of the system architecture and lists key features of the integration. This section also provides information about the setup steps that you are required to complete in your ServiceNow AI Platform instance and in the McAfee ePolicy Orchestrator \(McAfee ePO\) console prior to installing the application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Integration architecture for McAfee ePO

The following topic is an overview of the system architecture and lists key features of the integration. This section also provides information about the setup steps that you are required to complete in your ServiceNow AI Platform instance and in the McAfee ePolicy Orchestrator \(McAfee ePO\) console prior to installing the application from the ServiceNow Store.

## Key terms for the McAfee ePO integration

The following terms are used throughout the installation and configuration documentation for the integration.

-   **ServiceNow AI Platform**

    An enterprise ServiceNow product. The ServiceNow AI Platform is the base upon which individual components, such as Security Incident Response \(SIR\), IT Service Management, \(ITSM\), and other products are built.

-   **Security Incident Response \(SIR\)**

    A ServiceNow AI Platform application that tracks the progress of security incidents from discovery and initial analysis, through containment, eradication, and recovery, and into the final post incident review and closure.

-   **Plugin**

    Plugins are software components that provide specific features and functionalities within your ServiceNow AI Platform instance. For more information on the installation and configuration of the integration plugins, see [Install the application and configure a server for the McAfee ePO integration](../task/mcaffe-epo-install.md).

-   **ePolicy Orchestrator \(McAfee ePO\)**

    The user console where you manage the McAfee services, products and settings.

-   **McAfee extension plugin**

    This ServiceNow extension plugin is required for this integration. This plugin resides on your McAfee ePO console and connects your McAfee ePO console to your ServiceNow AI Platform instance.

-   **Capability**

    An automatic activity initiated from your ServiceNow AI Platform instance that is run in the McAfee ePO console to conduct enrichment queries and perform actions on your assets.

-   **Profile**

    Settings for McAfee ePO capabilities that you configure to specify when and under what conditions capabilities conduct enrichment queries and perform actions on your assets.

-   **MID server**

    An application that facilitates communication and the movement of data between the ServiceNow AI Platform and external applications, data sources, and services.

-   **ServiceNow administrator \(admin\)**

    A user with this role downloads and installs the SIR and McAfee ePO plugins to your ServiceNow AI Platform instance. A user with this role also assigns the security incident administrator role as required.

-   **ServiceNow Security incident administrator \(sn\_si.admin\)**

    A user with this role performs the configuration of the McAfee ePO integration with the Security Incident Response \(SIR\) product in your ServiceNow AI Platform instance as required. A user with this role also assigns the security incident analyst role as required.

-   **ServiceNow security incident analyst \(sn\_si.analyst\)**

    A user with this role interacts with and analyzes security incidents in the SIR product.


## System connection and data flow

The following figure is an example of a customer environment. A ServiceNow AI Platform MID server is required so that your ServiceNow AI Platform instance can connect to a McAfee ePO server \(console\) via a ServiceNow extension plugin. After you are connected, you invoke capabilities from your ServiceNow AI Platform to initiate malware scans, isolate host machines and restore them to your network, retrieve last scan results, and gather system details on your assets. When these capabilities return results from your assets that match your search criteria, data is pulled via the MID server into your ServiceNow AI Platform instance. Data is displayed on the related lists of a ServiceNow AI Platform Security Incident Response \(SIR\) security incident. The following figure illustrates the data flow for one group of endpoints managed by one McAfee ePO console.

![Configuration one.](../image/mcafee-canvas-1.png "Single endpoint configuration")

As shown in the following figure, this integration can support more than one McAfee ePO console. You can have one group of endpoints managed by one McAfee ePO console, and another group of endpoints managed by another McAfee ePO console. Data from multiple McAfee ePO consoles is pulled via a single MID server. However, you also may prefer to configure multiple MID servers if required by your organization.

![Multiple configurations.](../image/mcafee-canvas-2.png "MID servers configuration")

## Workflows for the McAfee ePO integration

This integration includes the following workflows. These workflows are pre-configured and are designed specifically for this integration. You can edit these workflows to meet the needs of your organization as required. For more general information about workflows and using the workflow editor, see [Getting started with workflows](https://www.servicenow.com/docs/access?context=getting-started-workflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

-   Security Operations McAfee EPO integration - Get Host Details
-   Security Operations McAfee EPO integration - Initiate Malware Scan
-   Security Operations McAfee EPO integration - Isolate Host
-   Security Operations McAfee EPO integration - List Threat Events
-   Security Operations McAfee EPO integration - Remove Isolation

## External systems connection

The integration requires that the MID server communicates via HTTPS protocol connection to the McAfee ePO console.

**Parent Topic:**[McAfee ePO integration](mcaffee-epo-overview-arch.md)

**Previous topic:**[McAfee ePO integration](mcaffee-epo-overview-arch.md)

**Next topic:**[Checklist for the McAfee ePO integration](../task/mcafee-epo_checklist.md)

