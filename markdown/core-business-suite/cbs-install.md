---
title: Install Core Business Suite
description: Install the Core Business Suite set of applications to streamline core business workflows across parts of your organization such as Legal, Human Resources, Workplace Services, Health and Safety, Procurement, Finance, Supplier Lifecycle Operations, and Accounts Payable Operations.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 2
breadcrumb: [Configure, Core Business Suite]
---

# Install Core Business Suite

Install the Core Business Suite set of applications to streamline core business workflows across parts of your organization such as Legal, Human Resources, Workplace Services, Health and Safety, Procurement, Finance, Supplier Lifecycle Operations, and Accounts Payable Operations.

## Before you begin

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

The following items are installed with Core Business Suite:

-   Dependent store applications
-   Roles

For more information, see [Components installed with Core Business Suite](../reference/comp-inst-with-cbs.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Core Business Suite \(sn\_cbs\) application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    The available versions are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Install the Core Business Suite applications. For more information, see [Installing Core Business Suite applications](../concept/install-cbs-applications.md).

