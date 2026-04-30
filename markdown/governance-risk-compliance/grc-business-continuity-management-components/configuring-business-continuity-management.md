---
title: Configuring Business Continuity Management
description: Configure the Business Continuity Management application to perform the business continuity tasks for your organization.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Business Continuity Management, Governance, Risk, and Compliance]
---

# Configuring Business Continuity Management

Configure the Business Continuity Management application to perform the business continuity tasks for your organization.

## Configuration overview

Configuring Business Continuity Management involves installing the application from ServiceNow® Store and setting it up by the administrators.

**Note:** If you have the BCM role, you can perform the setup tasks that are described in this section.

-   Install the Business Continuity Management application from store. For more information, see [Install Business Continuity Management from ServiceNow Store](../task/install-business-continuity-management.md).

    **Note:** Installing GRC: Business Impact Analysis, GRC: Business Continuity Planning, or GRC: Crisis Management automatically installs GRC: Business Continuity Management – Core and GRC: Business Continuity Management – Components.

-   Verify that you have assigned users with the required roles. For detailed instructions and a list of roles, see [Components installed with Business Continuity Management](../reference/installed-with-bcm.md#).
-   Set up the Business Continuity Management application by performing the administrative tasks with the BCM administrator role. For more information, see [General administration setup for BCM](set-up-bcm-bcmadmin-tasks.md).

    **Note:** You can view **My tasks page configurations** and **Properties** in the **General Administration** setup.

-   Complete the setup for a business impact analysis by performing the administrative tasks with the BIA administrator role. For more information, see [Setup for a business impact analysis](bcm-admin-tasks.md).

    **Note:** When you create a business impact analysis in BCM UIB Workspace, you can assign a BCM lead to the analysis in the BIA form itself.

-   Complete the setup for a business continuity plan by performing the administrative tasks with the BCP administrator role. For more information, see [Setup for a business continuity plan](bcp-admin-tasks.md).

    **Note:** When you create a business continuity plan in BCM UIB Workspace, you can assign a BCM lead to the plan in the BCP form itself.

-   Format the PDF templates for a business impact analysis, a business continuity plan, or an event. For more information, see [Format PDF templates for BIAs, BCPs, and events](../task/update-pdf-format-for-bia-bcp-event.md).
-   Configure the 360° relationship registries and views. For more information, see [Configure 360° relationship registries and views](../task/configure-relationship-registries-views.md).
-   Set up the notifications with Everbridge. For more information, see [Setup for Everbridge notifications](setup-steps-for-emergency-notification-uib-ws.md).
-   Set up the Crisis map. For more information, see [Setup for Crisis map](crisis-map-admin-tasks.md).
-   Review the setup tasks that are performed by an administrator. For more information, see [Setup by system administrators](set-up-bcm-sys-admin-tasks.md).
-   Review the setup information for UI Builder. For more information, see [Setup for the UI Builder](configuring-bcm-workspace-by-using-ui-builder.md).

**Note:**

Both BCM classic Workspace and BCM Configurable Workspace use the Workspace view. If you have made any customizations in other UI views, you must apply the same customizations before or after upgrading from a prior release to the Xanadu release.

For information on the custom components configuration in BCM classic Workspace, see the [KB1442692](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1442692) article.

For information on how to migrate reports and custom changes to BCM Configurable Workspace, see the [KB1444397](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1444397) article.

