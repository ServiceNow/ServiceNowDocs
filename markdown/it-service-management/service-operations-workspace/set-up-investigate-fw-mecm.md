---
title: Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation
description: Set up the Investigation Framework in Service Operations Workspace using Microsoft Endpoint Configuration Manager for Investigation to enable the display of the CI metrics information on the Investigation tab of the Incident records.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation

Set up the Investigation Framework in Service Operations Workspace using Microsoft Endpoint Configuration Manager for Investigation to enable the display of the CI metrics information on the **Investigation** tab of the Incident records.

You must ensure that the following requirements are met:

-   Service Operations Workspace for ITSM \(sn\_sow\_itsm\_cont\) application set up is complete and configured as per your requirement. For more information, see [Getting started with Service Operations Workspace for ITSM](getting-started-sow.md)
-   Install and configure Microsoft Endpoint Configuration Manager Spoke \(sn\_ms\_epcfgmgr\_spk\) application. For more information, see [Microsoft Endpoint Configuration Manager spoke](https://www.servicenow.com/docs/access?context=ms-endpoint&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) and [Microsoft SCCM integration](https://www.servicenow.com/docs/access?context=c_MicrosoftSCCMIntegration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Install the Microsoft Endpoint Configuration Manager for Investigation application.

    For more information, see [Install Microsoft Endpoint Configuration Manager for Investigation](../task/install-mecm-adapter.md).


-   **[Install Microsoft Endpoint Configuration Manager for Investigation](../task/install-mecm-adapter.md)**  
You can install the Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.
-   **[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](config-ci-metrics-mecm-adapter.md)**  
Configure the display of the metrics for Microsoft Endpoint Configuration Manager for Investigation.

**Parent Topic:**[Setting up Investigation Framework in Service Operations Workspace](set-up-investigate.md)

