---
title: Configure Software Asset Management using the Configuration Console
description: Configure Software Asset Management to manage software licenses, compliance, integrations, and team setup from Configuration Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/configure-sam-from-config-console.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Configuration Console, SAM setup, software asset management]
breadcrumb: [Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Configure Software Asset Management using the Configuration Console

Configure Software Asset Management to manage software licenses, compliance, integrations, and team setup from Configuration Console.

## Before you begin

-   Install the Software Asset Management application. See [Install Software Asset Management from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-sam-product-hub.md).
-   Install the SAM Admin Experience - v1.0 \(sn\_samp\_admin\) application from theServiceNow Store. Without this application, the Configuration Console is not available.

Role required: To access the Configuration Console, you must have the sam\_admin and ia\_user roles.

Individual modules may require additional roles. For role requirements by module, see the Configuration Console modules for Software Asset Management table in [Configuration Console overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-overview.md).

## About this task

The Configuration Console organizes Software Asset Management setup into independent modules. Configure modules and setup items in any order. The Setup status section tracks overall progress.

**Note:** Setup items appear based on installed applications. If a dependent application is not installed, related setup items are hidden.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  In the **Manage your products** section, select the Software Asset Management tile.

    The Product Hub opens.

3.  In the Configure your product section, select **Configure**.

    The Configuration Console opens, displaying the Setup status section and Configuration Summary navigation menu.

    **Tip:** To find a specific setup item, enter a keyword in the **Search configurations** field.

4.  Select a module to configure.

    -   In the Configuration Summary navigation menu, select a module.
    -   In the Setup status section, select **Get started** on a module card.
    Configure modules and setup items in any order.

5.  Complete the setup items in the module.

6.  After completing a setup item, select **Mark as configured**.

    **Tip:** You can change the configuration status of any item at any time.

7.  Review the **Setup status** section to confirm overall progress.

8.  To bundle configuration changes for deployment, select **Package and download**.

    The update set downloads as an `.xml` file.


## Result

Configured items show a completed status. Progress cards update as you mark items configured. The system typically captures your changes in an update set that you can apply to other instances.

## What to do next

To replicate a configuration from another instance, upload an existing update set on the Product Hub page. You can upload one `.xml` file at a time.

-   **[Configure Software Asset Management using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)**  
Use the AI conversational experience to configure Content service setup, groups, and users in the Configuration Console as a guided alternative to manual configuration.
-   **[SSO integration in Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-sso-integration-config-console.md)**  
The SSO \(Single Sign-On\) module under the Software integrations module in the Configuration Console displays a tile for each supported SSO provider. Use these tiles to create SSO integration profiles that capture managed applications and their usage data for software asset tracking.
-   **[Direct connection integration in Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-direct-connection-config-console.md)**  
The Direct connection module under the Software integrations module in the Configuration Console displays tiles for supported SaaS providers. Use these tiles to create integration profiles that connect directly to SaaS portals and pull in user subscription, activity, and usage data for license management.
-   **[Monitoring content job progress](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/content-job-progress.md)**  
Track the first-time run of the content jobs that load the Software Asset Management Content Service data into your instance. View job status and completion details to confirm that the initial download completed and that delta runs are current.
-   **[Configure scheduled jobs in the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/manage-scheduled-jobs-sam-using-config-console.md)**  
Automate recurring SAM processes such as normalization, reconciliation, and cleanup operations by configuring scheduled jobs in the Configuration Console.

**Parent Topic:**[Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md)

