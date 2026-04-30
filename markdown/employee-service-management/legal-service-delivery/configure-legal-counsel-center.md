---
title: Configure Legal Counsel Center Classic
description: Configure the Legal Counsel Center Classic to enable legal department members to quickly resolve legal requests and legal matters.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legal Counsel Center Classic, Legal Service Delivery, Employee Service Management]
---

# Configure Legal Counsel Center Classic

Configure the Legal Counsel Center Classic to enable legal department members to quickly resolve legal requests and legal matters.

## Before you begin

**Important:**

-   The legacy Legal Counsel Center was renamed as Legal Counsel Center Classic.
-   Legal Counsel Center Classic is being prepared for deprecation. It will be hidden and no longer available for activation for new customers but will continue to work and be supported for existing customers. For enhanced workspace experience, use [Legal Counsel Center](../concept/legal-counsel-center-landing.md). For details, see the Deprecation Process \[KB0867184\] article in the Now Support knowledge base.
-   If you are upgrading Legal Counsel Center Classic to the latest Xanadu release versions, make sure you have first upgraded it to the Washington DC release version of 6.3.8 or 6.4.1.
-   If you are using Legal Counsel Center Classic and want to upgrade to the Xanadu family release, ensure you upgrade to the Washington DC release first.

Legal Counsel Center Classic is built using the ServiceNow® Agent Workspace, so make sure you're familiar with the [Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) basics.

Role required: admin

## Procedure

1.  Configure landing page and lists in the Legal Counsel Workspace.

    1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **All Workspaces**.

    2.  Open the **Legal Counsel Workspace** record to configure.

    3.  On the Legal Counsel Workspace form, update fields as required.

        For more information about the fields, see Get started setting up your workspace.

        **Note:** You can also customize the workspace in the UI Builder by clicking **Open in UI Builder**.

    4.  In the Workspace Lists related list, click **New** to set up filtered lists.

        List filters display a subset of the records in a table. For more information, see Setting up list view in a workspace.

    5.  In the Landing Pages related list, open the **Legal Workspace Default Landing Page** record to customize and set up the landing page.

        For more information about creating a landing page, see Creating custom landing pages for workspaces, and about customizing a landing page, see Set up supplied landing pages in workspace.

    6.  On the Landing Page form, in the UX Page Element Permissions related list, click **New** to set up landing page permissions.

        These landing page permissions enable users to see the page based on their roles or groups they belong to. For more information, see Set up landing page permissions.

2.  Create an action that enables legal team to perform functions on the records in the list in the Legal Counsel Center Classic.

    1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Action &amp; Components** &gt; **List Actions**.

    2.  Open a base system action to modify or create new custom list actions by clicking **New**.

        For more information on the field descriptions, see Create custom list operations in a workspace.


