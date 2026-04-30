---
title: Migrate the existing charts to PAR dashboard in Service Operations Workspace for ITSM
description: You can migrate the common customizations and configurations of the existing dashboard to the Performance Analytics dashboard\(PAR dashboard\) using the on-screen migration utility. With this migration, you won't have to re-do the customizations for the PAR dashboard in Service Operations Workspace for ITSM to view the data.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-12-26"
reading_time_minutes: 1
breadcrumb: [Admin Center in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the existing charts to PAR dashboard in Service Operations Workspace for ITSM

You can migrate the common customizations and configurations of the existing dashboard to the Performance Analytics dashboard\(PAR dashboard\) using the on-screen migration utility. With this migration, you won't have to re-do the customizations for the PAR dashboard in Service Operations Workspace for ITSM to view the data.

## Before you begin

Ensure that the scope is set as Service Operations Workspace ITSM Common before you perform the migration.

**Note:** If you haven't customized the landing page, the system will be automatically migrated to the PAR dashboard. Once migrated, you can leverage the configuration options and features provided by the PAR dashboard.

The modifications made by overriding the `sys_ux_client_script_include` methods for `SowIncidentLandingPageUtilsSNC` and `SOWLandingPageTier2UtilsSNC` are considered for migration. These changes are applied to `SowIncidentLandingPageUtils` for Tier 1 and `SOWLandingPageTier2Utils` for Tier 2 dashboards. If you've created the scripts to override the methods in the SNC version, you must copy those changes to the corresponding non-SNC scripts.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  Select **Initial setup** &gt; **Landing page**.

3.  Select **Learn more** on the alert message that displays.

4.  Select **Preview migration** to preview the chart that will be migrated.

    ![Preview migration button on the Configurable chart migration](../image/sow-ac-charts-migration.png)

    The preview of the dashboard containing the customized charts opens in a new tab. Once you preview the dashboard, the label is updated from **Not previewed** to **Previewed**.

5.  Select **Migrate to configurable charts**.

    On the confirmation dialog box, select **Yes, migrate** to migrate the charts to the PAR dashboard.

    Upon successfully migration, the label is updated as **Complet**e. You can view the updated charts in the PAR dashboard in the SOW landing page.

    **Note:** You can perform the migration only once.


**Parent Topic:**[Admin Center in Service Operations Workspace for ITSM](../concept/admin-center-sow.md)

