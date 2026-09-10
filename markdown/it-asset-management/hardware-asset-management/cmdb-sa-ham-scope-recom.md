---
title: HAM model category recommendations
description: CMDB success advisor analyzes hardware asset data in your instance to recommend which model categories should be in your HAM advisor scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/cmdb-sa-ham-scope-recom.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [model category recommendations, HAM scope selection logic, asset count ranking, ham\_scope\_recommendation\_criteria system property, HAM Pro resource categories]
breadcrumb: [Use HAM advisor, Asset and CI management, Explore, Hardware Asset Management, IT Asset Management, Asset Management]
---

# HAM model category recommendations

CMDB success advisor analyzes hardware asset data in your instance to recommend which model categories should be in your HAM advisor scope.

Recommendations are ranked by asset count: the number of hardware assets in the Hardware \[alm\_hardware\] table associated with each model category. Recommendations always total up to 10 model categories.

You aren't required to accept all recommendations. Recommendations are guidance, and your organization's priorities should drive the final advisor scope selection.

## Ranking logic

How recommendations are generated depends on whether the Hardware Asset Management plugin \(sn\_hamp\) is installed and, if so, which resource categories are opted in:

-   If the **sn\_cmdb\_advisor.ham\_scope\_recommendation\_criteria** system property is set to `PREDEFINED`, CMDB success advisor skips asset-count ranking entirely and recommends the default model categories. See [Default model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/cmdb-sa-ham-scope-recom.md).
-   If the sn\_hamp plugin isn't installed, CMDB success advisor recommends the Computer model category plus the top nine server model categories by asset count. If fewer than 10 model categories result, additional model categories are added from the remaining predefined resource categories to reach 10.
-   If the sn\_hamp plugin is installed but no resource categories are opted in, no recommendations are generated. Opt in at least one resource category to receive recommendations. See [Managing opt-in and opt-out resource categories for HAM in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/cmdb-sa-ham-opt-categories.md).
-   If the sn\_hamp plugin is installed and neither the Servers nor the End User Computers resource category is opted in, CMDB success advisor recommends the top 10 model categories by asset count across all opted-in resource categories.
-   If the sn\_hamp plugin is installed and the Servers or the End User Computers resource category is opted in, CMDB success advisor recommends the Computer model category \(if End User Computers is opted in\) plus the top nine server model categories by asset count \(if Servers is opted in\). If fewer than 10 model categories result, additional model categories are added from the remaining opted-in resource categories to reach 10.

**Note:** Model categories with zero assets are never recommended.

## Default model categories

If asset-count ranking produces no results, or if the **sn\_cmdb\_advisor.ham\_scope\_recommendation\_criteria** system property is set to `PREDEFINED`, CMDB success advisor recommends this fixed set of model categories instead:

-   Computer
-   Server
-   Linux Server
-   Windows Server
-   Network Gear

