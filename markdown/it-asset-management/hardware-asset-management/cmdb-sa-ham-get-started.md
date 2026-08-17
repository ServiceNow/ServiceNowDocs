---
title: Getting started with HAM advisor dashboard setup
description: The HAM advisor dashboard can be configured automatically on installation or upgrade, or manually through the CMDB success advisor landing page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-get-started.html
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 2
keywords: [HAM advisor dashboard setup, automatic setup CMDB advisor, manual setup model categories, HAM advisor scope configuration, CMDB Advisor Auto Setup scheduled job]
breadcrumb: [Set up advisor, Use HAM advisor, Asset and CI management, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Getting started with HAM advisor dashboard setup

The HAM advisor dashboard can be configured automatically on installation or upgrade, or manually through the CMDB success advisor landing page.

The HAM scope defines which model categories CMDB success advisor monitors for HAM data quality. The selected categories determine the scope of the HAM advisor dashboard, including the KPIs, data integrations, and settings that are tracked.

**Important:** To determine which model categories to select, review the count of operational assets under each category in the Hardware Asset Workspace, or consult with your IT Asset Management \(ITAM\) or HAM administrator for guidance. See [Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/using-ham-workspace.md).

## Prerequisites

-   Obtain entitlement for HAM. See [Hardware Asset Management licensing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/ham-licensing.md).
-   Opt in HAM resource categories. See [Managing opt-in and opt-out resource categories for HAM in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-opt-categories.md).

## Roles required

Role required: sn\_cmdb\_admin

## Automatic setup

When you install or upgrade CMDB success advisor, the **CMDB Advisor - Auto Setup** on-demand scheduled job can automatically configure the HAM advisor dashboard if all eligibility conditions are met. Open the CMDB success advisor landing page to confirm the dashboard setup state before proceeding manually.

For more information about eligibility conditions and the auto-setup process, see [Automatic dashboard setup for HAM in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-auto-setup.md).

## Manual setup

If auto-setup did not run or the eligibility conditions were not met, configure the dashboard manually by selecting model categories on the CMDB success advisor landing page.

For instructions, see [Set up the HAM advisor dashboard manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-manual-setup.md).

