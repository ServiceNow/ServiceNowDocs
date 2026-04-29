---
title: Resilience metrics
description: You can view resilience metrics for services or business services, and pillars on the landing page of the Operational Resilience Workspace.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Landing page and dashboard views, Operational Resilience, Governance, Risk, and Compliance]
---

# Resilience metrics

You can view resilience metrics for services or business services, and pillars on the landing page of the Operational Resilience Workspace.

## Services, Business services, and Pillars overview

The landing page displays a summary of the resilience metrics for the services or business services and pillars.

![Dashboard data.](../../grc-operational-res/image/dashboard-data.png)

The landing page of the Operational Resilience Workspace displays the following tabs:

-   **Services overview** tab—Displays an overview of the status of the services in your organization. The Service \(CMDB\) Main node configuration fetches service-related data. Resilience metrics for the services, including their operational status, completed activities, red flags, and suggestions for improvements, are displayed on this tab. For information on the resilience metric displayed on the **Services overview** tab, see [Services overview tab](ser-ov.md).
-   **Business services overview** tab—Displays the status of the business services in your organization. The Opres with CSDM header Main node configuration sets up the business services-related data. Resilience metrics for the business services, including their operational status, completed activities, red flags, and suggestions for improvements, are displayed on this tab. For information on the resilience metric displayed on the **Business services overview** tab, see [Business services overview tab](bs-ov.md).
-   **Pillars overview** tab—Displays the status and metrics of the pillars in your organization. For information on the resilience metric displayed on the **Pillars overview** tab, see [Pillars overview tab](pillars-ov.md).

Existing customers typically use the Service \(CMDB\) Main node configuration, while new customers use the OpRes with CSDM header Main node configuration. Depending on the setup done by your administrator, either the **Services overview** or the **Business services overview** tab, is shown on the landing page.

Administrators or UI Builder administrators can show or hide these tabs from the Workspace view based on organizational needs. For information on how to display or hide either the **Services overview** or **Business services overview** tab, see [Show Business services overview tab in Workspace view](../../grc-operational-res/concept/displaying-services-overview-tab.md).

## Third-party Risk Management \(TPRM\) integration

Starting with Operational Resilience, release 21.0.x, you can track third-party risk assessments as red flags in the Operational Resilience reports and the overview pages for business services, service offerings, and business processes.

TPRM risk assessments are integrated into Operational Resilience if they meet the following conditions:

-   The risk rating is Very High \(using the overridden risk rating if applicable\).
-   The risk rating is valid beyond the current date.
-   The state is one of the following: **Generating observations**, **Responses received**, or **Finalizing with third party**.
-   The risk assessment applies to either the Company or an engagement.

Opening a third-party risk assessment from Operational Resilience displays the same view as when accessed directly from the Vendor Management Workspace.

To view Related lists and Red flags data in the Operational Resilience Workspace, you must have appropriate user roles as explained in this section.

-   **TPRM is not installed**

    If TPRM is not installed, Operational Resilience users cannot access risk red flags without the IRM roles.

-   **TPRM is installed**

    However, if TPRM is installed, Operational Resilience users can access both risk red flags and Third-party Risk Management red flags because they are assigned the TPRM viewer role. The TPRM viewer role includes risk viewer capabilities, thus eliminating the need for IRM roles.


For information on the roles required to view the related lists and red flags data, see the "Roles to view elated lists and Red flags data" table in the [Create New Service form](../reference/service-form-lists-ws-reference.md) page.

## Displaying reports for different user roles

Separate reports are displayed in the Operational Resilience Workspace landing page for BCM Professional and IRM Professional users.

## Enhanced roles for accessing the reports

The roles installed with Operational Resilience now contain the relationship for BCM Professional and IRM Professional users.

All Operational Resilience users can access general reports on the landing page.

The roles required to access the BCM and IRM reports in the Operational Resilience Workspace are explained in the following table.

<table id="table_fry_wq4_bgc"><thead><tr><th>

Type of reports

</th><th>

Required roles

</th><th>

Information

</th><th>

Contains

</th></tr></thead><tbody><tr><td rowspan="3">

BCM reports

</td><td>

sn\_oper\_res.bcm\_opres\_admin

</td><td>

Users with this role can create and delete both operational resilience activities and BCM activities.

</td><td>

-   sn\_oper\_res.admin
-   sn\_bcm.bcm\_opres\_manager

</td></tr><tr><td>

sn\_oper\_res.bcm\_opres\_manager

</td><td>

Users with this role can create both operational resilience activities and BCM activities.

</td><td>

-   sn\_oper\_res.manager
-   sn\_bcm.bcm\_opres\_user

</td></tr><tr><td>

sn\_oper\_res.bcm\_opres\_user

</td><td>

Users with this role can participate in both operational resilience activities and BCM activities.

</td><td>

-   sn\_oper\_res.user
-   sn\_bcm.viewer

</td></tr><tr><td rowspan="3">

IRM reports

</td><td>

sn\_oper\_res.irm\_opres\_admin

</td><td>

Users with this role can create and delete both operational resilience activities and IRM activities.

</td><td>

-   sn\_oper\_res.admin
-   sn\_bcm.irm\_opres\_manager

</td></tr><tr><td>

sn\_oper\_res.irm\_opres\_manager

</td><td>

Users with this role can create both operational resilience activities and IRM activities.

</td><td>

-   sn\_oper\_res.manager
-   sn\_bcm.irm\_opres\_user

</td></tr><tr><td>

sn\_oper\_res.irm\_opres\_user

</td><td>

Users with this role can participate in both operational resilience activities and IRM activities.

</td><td>

-   sn\_oper\_res.user
-   sn\_compliance.reader
-   sn\_risk.reader

</td></tr></tbody>
</table>![IRM reports.](../../grc-operational-res/image/irm-reports.png)

