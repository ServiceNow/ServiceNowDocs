---
title: Automatic dashboard setup for HAM in CMDB success advisor
description: CMDB success advisor can automatically configure the HAM advisor dashboard after installation or upgrade, providing immediate access to pre-configured hardware asset insights without selecting model categories manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-auto-setup.html
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 2
keywords: [auto-setup, automatic dashboard setup, HAM advisor dashboard, model categories]
breadcrumb: [Get started with dashboard setup, Set up advisor, Use HAM advisor, Asset and CI management, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Automatic dashboard setup for HAM in CMDB success advisor

CMDB success advisor can automatically configure the HAM advisor dashboard after installation or upgrade, providing immediate access to pre-configured hardware asset insights without selecting model categories manually.

## Auto-setup process

When you install or upgrade CMDB success advisor, the **CMDB Advisor - Auto Setup** on-demand scheduled job configures the Hardware Asset Management \(HAM\) advisor dashboard automatically. The job checks eligibility conditions, applies the model category scope, creates the HAM content template, and triggers initial data collection.

After data collection completes, users with the sn\_cmdb\_admin role receive a notification with a link to the configured dashboard.

The dashboard card on the CMDB success advisor landing page displays a badge with the number of model categories that auto-setup selected.

## Eligibility conditions

Auto-setup runs only when all the following conditions are met:

-   The instance has a HAM Pro entitlement. See [Hardware Asset Management licensing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/ham-licensing.md).
-   The CMDB success advisor for HAM setup isn't yet complete.
-   The total number of CIs on the instance is fewer than 65 million.
-   If the Hardware Asset Management plugin \(sn\_hamp\) is installed, at least one HAM resource category is opted in. See [Managing opt-in and opt-out resource categories for HAM in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-opt-categories.md).

**Note:** If any condition isn't met, you can configure the HAM advisor dashboard manually.

## Scope selected by auto-setup

Auto-setup selects the top five recommended HAM model categories. Rankings are based on the asset financial value and footprint of each model category in your environment.

For each selected model category, auto-setup also marks the corresponding CI class as a principal class so the class appears in CI selection filters on incident, change, and problem forms.

## Data collection and notifications after auto-setup

After auto-setup completes, data collection begins automatically. Data collection runs monthly and changes to daily after you open the dashboard for the first time.

The **CMDB Advisor - Check Job Completion and Notify** scheduled job checks whether data collection has completed. When collection completes, the job sends a notification to users with the sn\_cmdb\_admin role that includes a link to the configured dashboard. After all notifications are sent, the job is deactivated.

When you first open the HAM advisor after auto-setup completes, a notification indicates that the advisor is ready and shows the number of model categories automatically selected based on asset financial value and footprint.

## Reviewing and modifying the auto-setup scope

You can review and update the model categories selected by auto-setup at any time.

For instructions on updating model categories, see [Optimize the HAM advisor dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-optimize-dashboard.md).

