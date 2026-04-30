---
title: Customize the banner logo for the AI Search Analytics dashboard
description: Add your own logo to the banner for the AI Search Analytics dashboard.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Search analytics dashboard, Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Customize the banner logo for the AI Search Analytics dashboard

Add your own logo to the banner for the AI Search Analytics dashboard.

## Before you begin

The Platform Analytics Solution for Advanced AI Search Management Tools must be activated on your instance. For details on activating this solution, see [Activate the Platform Analytics Solution for Advanced AI Search Management Tools](install-adv-ais-mgmt-tools.md).

Role required: admin

## About this task

The AI Search Analytics dashboard displays the ServiceNow logo in the banner. You can modify the UX theme assets for the dashboard to display your own logo instead.

## Procedure

1.  Switch to the Advanced AI Search Management Tools application.

    For details on switching applications, see [Switch between applications](https://www.servicenow.com/docs/access?context=t_SwitchBetweenApplications&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

2.  To replace the default **header\_for\_dashboard** UX theme asset with a version containing your logo, perform the following steps.

    1.  Navigate to the UX Theme Asset \[sys\_ux\_theme\_asset\] table's list view by selecting **All**, entering `sys_ux_theme_asset.list` in the **Filter** field, and pressing Enter.

    2.  Open the **header\_for\_dashboard** record.

    3.  Select **Delete**.

    4.  Select **New**.

    5.  On the UX Theme Asset form, enter the following field values.

        |Field|Value|
        |-----|-----|
        |Category|Image|
        |Name|header\_for\_dashboard|

    6.  In the form header, select the Manage Attachments icon ![](../../using-forms/image/UI14FormAttachments.png) and attach your logo image to the new record.

        To learn more about managing record attachments, see [Manage attachments](https://www.servicenow.com/docs/access?context=t_ManagingAttachments&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    7.  Select **Submit**.

3.  To link your new UX theme asset to the banner for the AI Search Analytics dashboard, perform the following steps.

    1.  Navigate to the UX Theme \[sys\_ux\_theme\] table's list view by selecting **All**, entering `sys_ux_theme.list` in the **Filter** field, and pressing Enter.

    2.  Open the **SearchAnalytics Dashboard Theme** record.

    3.  Select the **Legacy: Experience Theme** tab.

    4.  In the UX Theme Assets list, edit the existing asset record.

        **Note:** If you don't see the UX Theme Assets list, configure the form layout, adding **UX Theme Assets-&gt;Theme** to the list of selected fields. When prompted, switch to editing the form section in the Global application. For details on this procedure, see [Configuring the form layout](../../../administer/form-administration/concept/configure-form-layout.md#).

    5.  On the UX Theme Assets form, in the **Asset** field, enter the value `header_for_dashboard`.

    6.  Select **Update**.


## Result

Your custom logo image appears in the banner for the AI Search Analytics dashboard.

