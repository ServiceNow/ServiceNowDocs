---
title: Select apps during product installation
description: Use the app selection modal to review mandatory and optional apps, customize your installation by selecting optional components, and complete the product installation through product hub installation flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ia-select-app-prod-install.html
release: australia
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 3
breadcrumb: [Mandatory and optional app selection modal, Administer, ServiceNow Otto for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Select apps during product installation

Use the app selection modal to review mandatory and optional apps, customize your installation by selecting optional components, and complete the product installation through product hub installation flow.

## Before you begin

Before you begin:

-   Your instance must have the Product Hub product available for installation.
-   Your system must have active licensing for at least the mandatory apps in the bundle.

Role required: admin

## About this task

When installing a new product bundle, the app selection modal displays which apps are required and which are optional. Use this procedure to customize your installation by selecting which optional apps to include.

## Procedure

1.  Navigate to the product bundle installation on the Product Hub page.

    Look for the Install option or product bundle installation entry point.

2.  Select the product bundle you want to install.

    The system enforces the selection of mandatory apps defined for the product bundle. These apps can't be deselected during installation. After reviewing the selected apps, proceed to the next step.

3.  Review the mandatory apps section in the app selection modal.

    Apps that are defined as mandatory and included in the user's entitlement are displayed with selected, disabled checkboxes and can't be deselected. Optional apps remain selectable and can be included or excluded during installation.

4.  Review the optional apps section and decide which optional components to include.

    The system retrieves the apps that are entitled and available in the instance. Apps are then presented as either mandatory or optional based on the product bundle configuration. Mandatory apps can't be deselected, while optional apps can be selected or cleared during installation.

    Select the checkboxes for optional apps you want to include in this installation.

5.  Select or deselect optional apps and observe the item count update.

    As you select or deselect optional apps, the install button count updates in real-time. The count displays total selected items, including mandatory apps plus your selected optional apps. For example, if a bundle has 3 mandatory apps and 5 optional apps, and you select 2 optional apps, the install button shows "Install 5 selected items" \(3 mandatory + 2 optional\).

6.  Verify the total count of apps being installed before proceeding.

    The install button displays text similar to "Install X selected items" where X represents the total. The button remains inactive if zero apps are available for installation \(for example, if all mandatory apps are unavailable\).

7.  Select the install button to begin the installation.

    The system submits an install request containing all mandatory apps and only the optional apps you selected. App Manager validates the request and executes the installation.

    The installation begins and the system displays progress updates. On completion, a confirmation message appears listing all installed apps.

    If the installation fails with an error message, verify the following:

    -   You have the appropriate admin role or permissions.
    -   Your instance has sufficient disk space for all selected apps.
    -   No dependency conflicts exist between selected apps \(consult with your implementation team if you're unsure\).
    If issues persist, contact your ServiceNow implementation team or support.


## Result

The selected product bundle and all mandatory plus chosen optional apps are installed on your instance. The apps are then available for use by users with the appropriate roles.

## What to do next

After installation completes, consider the following next steps:

-   Verify that the installed apps are accessible from the appropriate menu or navigation area.
-   Assign roles to team members who need to use the new apps.
-   For additional optional apps installed later, repeat this procedure to install additional components if needed.
-   Refer to the concept topic for more information about how licensing and app availability work.

**Parent Topic:**[Mandatory and optional app selection modal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-mandatory-optional-select-modal.md)

