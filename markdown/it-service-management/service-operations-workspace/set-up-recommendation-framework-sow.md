---
title: Setting up Recommendation Framework in Service Operations Workspace
description: You can enable an agent working on an incident to view predictions provided by Recommendation Framework.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Setting up Recommendation Framework in Service Operations Workspace

You can enable an agent working on an incident to view predictions provided by Recommendation Framework.

Recommendation Framework is now deprecated and no longer supported or available for new activation. Recommended Actions for ITSM feature provides the latest experience for this functionality. To get the advanced version, you must install the Advanced Recommended actions for ITSM \(com.snc.uib.sow\_itsm\_ra\_advanced\) plugin and you must procure ITSM Pro package subscription.

**Note:** The best practice to get the advanced version is to install the Task Intelligence for ITSM \(com.snc.itsm\_ml\_task\) plugin and procure the ITSM Pro package subscription. For more information, see [Exploring Recommended Actions for ITSM in Service Operations Workspace](exploring-recommended-actions-for-itsm-in-service-operations-workspace.md).

You must ensure that the following requirements are met:

-   Install the Service Operations Workspace ITSM Applications \(sn\_sow\_itsm\_cont\) application from [ServiceNow Store.](https://store.servicenow.com/sn_appstore_store.do#!/store/home) For information about this installation, see [Getting started with Service Operations Workspace for ITSM](getting-started-sow.md). With this installation, the following Recommendation Framework applications are also installed.

    |Application|Description|
    |-----------|-----------|
    |Recommendation Framework \(sn\_rf\)|Provides the framework for dynamic and contextual recommendations in a configurable workspace.|
    |Recommendations for Incident Management \(sn\_sow\_incident\_rf\)|Provides configurations, for example, recommendation rules, to predict recommendations for an incident in Service Operations Workspace.|

-   Install the Predictive Intelligence for Incident plugin \(com.snc.incident.ml\) to install the Relevant problems solution definition. For information about this plugin installation, see [Request Predictive Intelligence for Incident](../../incident-management/task/request-predictive-intelligence-for-im.md).
-   Install the Predictive Intelligence for Major Incident Management plugin \(com.snc.incident.mim.ml\_solution\) to install the following IT Service Management solution definitions. For information about this plugin installation, see [Request Predictive Intelligence for Major Incident Management](../../incident-management/task/request-pred-intelli-mim.md).
-   Install the Predictive Intelligence for Incident Management plugin \(com.snc.incident.ml\_solution\) to install the following IT Service Management solution definitions. For information about this plugin installation, see [Request Predictive Intelligence for Incident Management](../../incident-management/task/request-pred-intelli-inc-mgmt.md).
    -   Similar Knowledge Articles
    -   Similar Open Incidents
    -   Incident Service
    -   Incident Configuration Item
    -   Incident Assignment
    -   Similar Resolved Incidents
-   Train solution definitions to predict recommendations for an incident. For information about training solution definitions, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **[Configure Recommendation Framework for an incident in Service Operations Workspace](../task/configure-rf-properties.md)**  
Enable recommendations at field level or from the contextual sidebar for an incident in Service Operations Workspace.

**Parent Topic:**[Setting up integrations in Service Operations Workspace for ITSM](setting-up-sow-itsm.md)

