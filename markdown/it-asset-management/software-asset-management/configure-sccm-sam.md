---
title: Configure SCCM for Software Asset Management
description: Set up Microsoft SCCM for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with client software found in your environment. You can also set up SCCM for Client Software Distribution to reclaim unused and underused software.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Configure SCCM for Software Asset Management

Set up Microsoft SCCM for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with client software found in your environment. You can also set up SCCM for Client Software Distribution to reclaim unused and underused software.

## Before you begin

Role required: sn\_client\_sf\_dist.csd\_admin or admin

**Tip:** Sign up for the [Software Asset Management: Integration with SCCM for Reclamation and Distribution](https://nowlearning.service-now.com/lxp?id=overview&sys_id=bfd3d509db9eb300de3cdb85ca961972&type=course) course to learn about SCCM setup, reclamation, and more.

## Procedure

1.  [Activate the SCCM integration plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/activate-microsoft-sccm-plugin.md) for your version of SCCM.

    -   Integration — Microsoft SCCM 2012 v2 \(com.snc.integration.sccm2012v2\)
    -   Integration — Microsoft SCCM 2016 \(com.snc.integration.sccm2016\)
    If you want to pull software usage data from SCCM, activate the software usage plugin for your version of SCCM.

    -   Integration — Microsoft SCCM 2012 v2 Software Usage \(com.snc.samp\_usage\_sccm\) plugin
    -   Integration — Microsoft SCCM 2016 Software Usage \(com.snc.samp.usage\_sccm\_2016\) plugin
    **Important:** These Microsoft SCCM plugins will be deprecated in the Tokyo release. If you are integrating with SCCM for the first time, request and install the Service Graph connector for Microsoft SCCM application from the[ServiceNow Store](https://store.servicenow.com/) instead. If you have already activated one of the Microsoft SCCM plugins on your ServiceNow instance, use the Migration Readiness Tool for Service Graph Connector for SCCM store application to prepare your instance for migration from the Microsoft SCCM plugin to the Service Graph connector. See [Service Graph connector for Microsoft SCCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-integration-sccm.md) for more information on the Service Graph connector.

2.  If you want to reclaim unused and underused software, set up SCCM for Client Software Distribution \(CSD\).

    1.  Request the [Client Software Distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_ActivateClientSWDistribution.md) \(com.snc.orchestration.client\_sf\_distribution\) plugin.

        Client Software Distribution requires a subscription to [Orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/r-orchestration.md).

    2.  In SCCM, create an application, install collection, and uninstall collection for any software that you have not already created these items for.

        After you create these items, you can then deploy the application for both the install and uninstall collection. For detailed instructions, see [Create and deploy an application with SCCM](https://docs.microsoft.com/en-us/configmgr/apps/get-started/create-and-deploy-an-application) and [Create collections in SCCM](https://docs.microsoft.com/en-us/configmgr/core/clients/manage/collections/create-collections) from the Microsoft SCCM product documentation.

        To reclaim software, an application, install collection, and uninstall collection must exist for the software. If you installed software manually or using an SCCM legacy package, you must still create these items so that you can reclaim the software.

        **Note:** If you installed software using an SCCM legacy package, you can use [Microsoft Package Conversion Manager](https://docs.microsoft.com/en-us/configmgr/apps/pcm/package-conversion-manager) to create the application.

3.  [Setup the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md).

4.  [Configure SCCM and the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_RetrieveSCCMDataClientSWDist.md).

5.  To offer an application from the Service Catalog, [create a catalog item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateCatItemSCCMApp.md).


## What to do next

Once you've configured SCCM and discovered your software applications, you can [create reclamation rules](create-reclamation-rule-sccm.md) to identify unused or underused software, [view software usage](view-sw-usage-workspace.md), and [reclaim software](t_AddAReclCandidate.md).

**Parent Topic:**[Configuring Software Asset Management](../concept/Config-sam-workspace.md)

