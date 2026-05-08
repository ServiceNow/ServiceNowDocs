---
title: Digital End-User Experience and Service Observability UI experience on investigate tab
description: Based on the Configuration Item \(CI\) selected in the Investigate tab, the user criteria and rules defined in the Investigate CI Experience Rules \(sn\_sow\_investigate\_ci\_ux\_rule\) table, the Investigate tab displays the CI metrics in different UI experience dashboard for the different CI classes.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Features of the Investigation tab, Incident Management in Service Operations Workspace reference, Incident Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Digital End-User Experience and Service Observability UI experience on investigate tab

Based on the Configuration Item \(CI\) selected in the **Investigate** tab, the user criteria and rules defined in the **Investigate CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table, the Investigate tab displays the CI metrics in different UI experience dashboard for the different CI classes.

The following UI experiences dashboard are supported on the Investigate tab:

-   Default view: The CI metrics are display in default dashboard view on the tab.
-   Digital End-User Experience \(DEX\) view: The CI metrics are displayed in DEX dashboard view on the tab.
-   Service Observability \(SO\) view: The CI metrics are displayed in SO dashboard view on the tab. For more information, see View overall service health.

You can navigate to the Investigate **CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table to configure user criteria, CI conditions, and rule order. You may also choose to match CI extensions, including subclasses. These configurations determine which UI experience view appears on the investigate tab when a specific CI class is selected.

You can select the CI from the list of affected CIs or caller CIs associated with the incident record. The caller CIs are the CIs that are assigned to the caller.

## DEX view in the Investigate tab

![Investigate tab - DEX view](../image/sow-investigation-tab-dex-view.png)

The Investigate tab displays a DEX UI experience dashboard, if the selected CI matches the following conditions:

-   DEX is installed and activated in the instance.
-   CI device is cmdb\_ci\_computer class.
-   Matches DEX related rule from the **Investigate CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table.
-   CI is supported by DEX.

For more information on DEX, see [Digital End-User Experience](../../digital-end-user-experience/concept/dex-landing.md).

## SO view in the Investigate tab

![Investigate tab - SO view](../image/sow-investigation-tab-so-view.png)

The Investigate tab displays SO UI experience dashboard, if the selected CI matches the following conditions:

-   CI is cmdb\_ci\_service class.
-   CI is configured with SO data mapping. For more information, see Create and manage data mappings.
-   Matches SO related rule from the **Investigate CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table.

The selected CI is retrieved from the following tables:

-   task\_ci
-   task\_cmdb\_ci\_service
-   task\_service\_offering

The investigate tab displays SO dashboard containing vendor generated metrics from sources such as AWS, Datadog, New Relic, Dynatrace and so on that are relevant to the service.

**Note:** The dashboard that appears on the Investigate tab is the same as the **Overview** dashboard in Service Observability. If the service has no data mapping, an empty state is displayed.

For more information on SO, see Service Observability.

**Parent Topic:**[Features of the Investigation tab](features-of-investigation-tab.md)

