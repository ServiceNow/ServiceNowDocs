---
title: Configuring Recommended Actions for ITSM in Service Operations Workspace
description: Enable an agent working on the relevant recommendations provided by Recommended Actions for ITSM.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Contextual side panel configurations in SOW for ITSM, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Configuring Recommended Actions for ITSM in Service Operations Workspace

Enable an agent working on the relevant recommendations provided by Recommended Actions for ITSM.

The standard version of Recommended Actions for ITSM is provided as a new feature in Incident Management for the Service Operations Workspace application that is a part of Service Operations Workspace 3.0.

Existing users who upgrade to Service Operations Workspace 3.0 get the standard version of Recommended Actions for ITSM by default as a new feature. New users get the standard version of Recommended Actions for ITSM after installing the Service Operations Workspace ITSM Applications \(sn\_sow\_itsm\_cont\) application from the ServiceNow Store.

Users on Service Operations Workspace 6.0 will receive the new standard plugin, Recommended Actions for ITSM \(sn\_itsm\_ra\), which includes its standard features.

For more information, see [Getting started with Service Operations Workspace for ITSM](getting-started-sow.md). This plugin enables the standard recommended actions and offers the following recommendations:

-   Open incidents \(CI &amp; Service\)
-   Similar Resolved incidents \(CI &amp; Service\)
-   Open PRBs \(CI &amp; Service\)
-   AI Search Recommendation

    **Note:** AI Search Recommendation is available for users using Service Operations Workspace version 5.0 and above versions.


To get the advanced version of Recommended Actions for ITSM, you must install the Advanced Recommended actions for ITSM \(sn\_sow\_itsm\_ra\_adv\) plugin, and you must procure the ITSM Pro package subscription.

**Note:** The best practice to get the advanced version is to install the Task Intelligence for ITSM \(com.snc.itsm\_ml\_task\) plugin and procure the ITSM Pro package subscription.

This plugin provides two Task Intelligence-based recommendations for Incidents: **Incident Fields value prediction \(TI\)** and **Similar Incidents \(TI\)**.

**Note:** The Advanced Recommended actions for ITSM \(sn\_sow\_itsm\_ra\_adv\) and Task Intelligence Admin Console \(com.sn\_ti\_admin\) plugins are installed as a dependency.

Additionally, to get Predictive Intelligence -based recommendations, install the following plugins:

-   Install the Predictive Intelligence for Incident \(com.snc.incident.ml\) plugin to install the Relevant problems solution definition-Similar open PRBs \(Similarity\). For information about this plugin installation, see [Request Predictive Intelligence for Incident](../../incident-management/task/request-predictive-intelligence-for-im.md).
-   Install the Problem Management for Service Operations Workspace \(**com.snc.uib.sow\_problem**\) plugin to install the solution definition-Create Problem for Major incident.
-   Install the Predictive Intelligence for Major Incident Management \(com.snc.incident.mim.ml\_solution\) plugin to install the following IT Service Management solution definitions.

    -   Propose major incident \(Trend\)
    -   Similar major incident \(Trend\)
    For information about this plugin installation, see [Request Predictive Intelligence for Major Incident Management](../../incident-management/task/request-pred-intelli-mim.md).

-   Install the Predictive Intelligence for Incident Management \(com.snc.incident.ml\_solution\) plugin to install the following IT Service Management solution definitions.

    -   Assignment group \(Classification\)
    -   Configuration item \(Classification\)
    -   Service \(Classification\)
    -   Similar open incidents \(Similarity\)
    -   Similar KB articles \(Similarity\)
    -   Similar resolved incidents \(Similarity\)
    -   Similar Incidents \(TI\)

        **Note:** Similar Incidents \(TI\) recommendation is available only from Service Operations Workspace version 6.0.

    For more information, see [Request Predictive Intelligence for Incident Management](../../incident-management/task/request-pred-intelli-inc-mgmt.md).


Train solution definitions to predict recommendations for an incident. For information about training solution definitions, see [Predictive Intelligence for Incident Management](../../incident-management/concept/predictive-intelligence-for-incident.md)

For information about the training solution definition of Incident Fields value prediction \(TI\), see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md).

-   **[Recommendation Framework Deprecation](recommendation-framework-deprecation.md)**  
Recommendation Framework is now deprecated and no longer supported or available for new activation. Recommended Actions for ITSM feature provides the latest experience for this functionality. To get the advanced version, you must install the Advanced Recommended actions for ITSM \(com.snc.uib.sow\_itsm\_ra\_advanced\) plugin and you must procure ITSM Pro package subscription.
-   **[Setting up Recommended Actions for ITSM](setting-up-recommended-actions-for-itsm.md)**  
Set up recommended actions to display relevant recommendations in Service Operations Workspace.

**Parent Topic:**[Contextual side panel configurations in SOW for ITSM](contextual-side-panel-configurations-sow-itsm.md)

