---
title: Managing opt-in and opt-out resource categories for HAM in CMDB success advisor
description: You can opt in to Hardware Asset Management \(HAM\) license resource categories to make the corresponding model categories available for selection in CMDB success advisor for HAM.Select HAM resource categories to make their model categories available for configuration in CMDB success advisor.When a resource category is opted out in HAM, its model categories remain in CMDB success advisor until you manually remove them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-opt-categories.html
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-02-27"
reading_time_minutes: 3
keywords: [HAM resource category opt-in, opt-out resource categories, model category availability, HAM license resource category, hardware asset advisor scope, opt in HAM resource categories, HAM license resource category management, model category availability, opt out HAM resource categories, remove opted-out model categories, HAM advisor scope reduction]
breadcrumb: [Set up advisor, Use HAM advisor, Asset and CI management, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Managing opt-in and opt-out resource categories for HAM in CMDB success advisor

You can opt in to Hardware Asset Management \(HAM\) license resource categories to make the corresponding model categories available for selection in CMDB success advisor for HAM.

Before you can set up or update the HAM advisor scope in CMDB success advisor, at least one HAM license resource category must be opted in. Resource categories define the hardware types, such as Servers, Storage, or Mobile Device, covered by your HAM subscription. Only model categories belonging to opted-in resource categories appear in the CMDB success advisor for HAM.

The opted-in resource categories are set to `true` in the HAM Resource Category \[sn\_hamp\_resource\_category\] table. For more information, see [Opt-in or opt-out of HAM license resource categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/optin-optout-ham-license-resource-categories.md).

## Model category availability based on opt-in status

The opt-in status of resource categories determines which model categories are available in the HAM advisor.

The following table describes the HAM advisor behavior based on opt-in status.

|Status|Advisor behavior|
|------|----------------|
|No resource categories opted in|The Select model categories dialog box displays a message indicating that no categories are currently available. You must opt in to at least one resource category before you can configure or update the HAM advisor scope.|
|Resource categories opted in|The corresponding model categories appear in the **Available resource and model categories** column of the Select model categories and Edit dashboard scope dialog boxes and can be selected for the HAM advisor scope.|
|Resource category opted out after selection|Model categories from that resource category are no longer available in the advisor. If those categories were previously selected for the HAM advisor scope, they may become unavailable and the dashboard scope may be reduced.|

## Opt in HAM resource categories

Select HAM resource categories to make their model categories available for configuration in CMDB success advisor.

### Before you begin

Role required: ham\_admin

### Procedure

1.  On the CMDB success advisor landing page, select **Select model categories** within the HAM card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/cmdb-sa-landing-page.md).

2.  If the dialog box displays **No model categories available**, select **Opt in categories**.

    The HAM license resource categories management page opens.

3.  Select the resource categories included in your HAM subscription and opt them in.

4.  Return to CMDB success advisor and proceed with selecting model categories.

    For more information, see [Getting started with HAM advisor dashboard setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/cmdb-sa-ham-get-started.md).


## Remove opted-out HAM resource categories

When a resource category is opted out in HAM, its model categories remain in CMDB success advisor until you manually remove them.

### Before you begin

A message is displayed in the advisor indicating that opted-out resource categories are part of the current scope.

Role required: ham\_admin

### Procedure

1.  On the CMDB success advisor landing page, select **Edit dashboard scope** within the HAM card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/cmdb-sa-landing-page.md).

2.  In the **Available resource and model categories** column, locate the opted-out resource category and clear its check box.

3.  Select **Save**.


### Result

Removing an opted-out resource category excludes all model categories associated with it from the HAM advisor scope and reduces the scope of your HAM advisor dashboard accordingly.

