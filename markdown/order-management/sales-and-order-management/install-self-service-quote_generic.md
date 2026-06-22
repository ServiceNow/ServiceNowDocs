---
title: Install Quote Self-Service
description: Quote Self-Service is automatically installed when you install the Quote Management application. If you install a different application, you must add the Quote Self-Service as a plugin dependency before installation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/install-self-service-quote\_generic.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 1
breadcrumb: [Quote creation via Self-Service, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Install Quote Self-Service

Quote Self-Service is automatically installed when you install the Quote Management application. If you install a different application, you must add the Quote Self-Service as a plugin dependency before installation.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Depending on your entitlements, you must install demo data after installation.

Role required: admin

## About this task

The following items are installed with Self-service quote.

-   Plugins
-   Store applications

For more information on viewing components that are installed with an application, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/find-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Quote Self-Service application \(`com.snc.quote_self_service`\) using the filter criteria and search bar.

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they are already installed or require installation.

4.  Install demo data based on your entitlements.

<table id="choicetable_tsz_f2h_jjc"><thead><tr><th align="left" id="d122003e148">

Demo data install task

</th><th align="left" id="d122003e151">

Description

</th></tr></thead><tbody><tr><td id="d122003e157">

**If demo data is available and you want to install it**

</td><td>

1.  Select the **Load Demo Data** option.
2.  Select **Install**.
 **Warning:** If you don't load the demo data during installation, it's unavailable to load later.

</td></tr><tr><td id="d122003e184">

**If the Load Demo Data option isn't available but you want demo data**

</td><td>

Load the demo data after installing.

 1.  Install ``com.sn_quote_self_service`.`.
2.  In the filter, enter `v_plugin.list` and press Enter.
3.  Under Related Links, select **Install Demo Data Only**.


</td></tr></tbody>
</table>
