---
title: Executive insights into KPIs using the Asset Management Executive dashboard
description: Use the Asset Management Executive dashboard to gain visibility into critical KPIs for the Software Asset Management application, Hardware Asset Management application, and the Cloud Cost Management application via a single dashboard.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Executive insights into KPIs using the Asset Management Executive dashboard

Use the Asset Management Executive dashboard to gain visibility into critical KPIs for the Software Asset Management application, Hardware Asset Management application, and the Cloud Cost Management application via a single dashboard.

To access the Asset Management Executive dashboard, you must either have the Software Asset Management application or the Hardware Asset Management application in your ServiceNow instance.

To view the Asset Management Executive dashboard, navigate to **Asset Executive Workspace** &gt; **Asset Management Executive Dashboard**. A user with the role of sn\_itam\_common.asset\_exec can access the dashboard.

![Asset Management Executive Dashboard.](../image/itam-exec-dboard.png "Asset Management Executive Dashboard")

You can filter the results in the dashboard by product, domain, or by both product and domain. If you filter by domain, the filter gets applied to all the widgets. If you filter by product, since some widgets are specific to certain products, the filter is not applied to all the widgets.

After you select a filter, a blue box appears on the right side of each widget, displaying one of the following numbers:

-   0: Indicates that no filter is applied to a widget.
-   1: Indicates that only one filter is applied to a widget.
-   2: Indicates that both the filters are applied to a widget.

**Note:** To use the domain filter, you must activate the plugins: com.glide.domain.msp\_extensions.installer and com.snc.pa.domain\_support.

The scheduled job, **Asset Management - Populate KPI aggregate table**, runs daily to update the data on the dashboard. To view the latest data for a widget, click the widget to display the list view page.

The dashboard widgets vary depending on the application plugins that you've activated in your instance. The widgets available with each application are listed in the following table:

<table id="table_qcw_ypq_4tb"><thead><tr><th>

Widget

</th><th>

Software Asset Management

</th><th>

Hardware Asset Management

</th><th>

Cloud Cost Management

</th></tr></thead><tbody><tr><td>

Total spend

</td><td>

Total cost of all entitlements for all products.

 Source table: License Metric Results \[samp\_license\_metric\_result\].

</td><td>

Total cost of all hardware assets whose status is either **In stock**, **In use**, **In maintenance**,or **In transit**.

 Source table: Hardware \[alm\_hardware\].

</td><td>

Total active cost of all cloud resources.

 Source table: Spend Report Daily Aggregated Cost \[sn\_cld\_spend\_core\_daily\_aggregated\_cost\].

</td></tr><tr><td>

Actual savings

</td><td>

Total yearly savings for all products. This value is calculated as the total savings from closed complete reclamation candidates.

 Source table: Removal Candidate \[samp\_sw\_reclamation\_candidate\].

</td><td>

Not applicable.

</td><td>

This value is calculated as the monthly savings on cloud resources.

**Note:** This widget appears only if you have the Software Asset Management application installed on your instance.

 Source table: Cloud Insights Rightsizing Recommendation Automatics \(sn\_clin\_core\_rs\_recommendation\_automatic\) where State = Completed.

</td></tr><tr><td>

Potential savings

</td><td>

Cost saved if removal candidates are reclaimed.

 Source table: Removal Candidate \[samp\_sw\_reclamation\_candidate\].

</td><td>

Not applicable.

</td><td>

Total of potential savings on a monthly basis on cloud rightsizing, cloud unused machines, cloud reservations, and cloud business hours.

**Note:** This widget appears only if you have the Software Asset Management application installed on your instance.

 Source tables:

-   Cloud Insights Rightsizing Recommendation Automatics \[sn\_clin\_core\_rs\_recommendation\_automatic\].
-   Cloud Insights Unused Recommendation \[sn\_clin\_core\_rs\_unused\_recommendation\].
-   Reserved Instance Recommendation \[sn\_clin\_core\_ri\_recommendation\].

</td></tr><tr><td>

Assessment fulfillment time

</td><td>

Fulfillment time bar graph of software requests from the Service Catalog. The graph shows the number of requests and the number of days taken to close those requests in the ranges of 0-5, 6-10, 11-20, 21-30, or 31+ days.

 Source table: Asset fulfillment time \[asset\_fulfillment\_time\].

</td><td>

Fulfillment time bar graph of hardware requests from the Service Catalog. The graph shows the number of requests and the number of days taken to close those requests in the ranges of 0-5, 6-10, 11-20, 21-30, or 31+ days.

 Source table: Asset fulfillment time \[asset\_fulfillment\_time\].

</td><td>

Not applicable.

</td></tr><tr><td>

Completed software success goals

</td><td>

Number of success goals completed for the Software Asset Management application.

 Source table: SAM Success Goal \[samp\_success\_goal\].

**Note:** This widget is available only when the Software Asset Workspace \(com.sn\_sam\_workspace\) plugin is installed.

</td><td>

Not applicable.

</td><td>

Not applicable.

</td></tr><tr><td>

Software success savings

</td><td>

Actual savings from completed success goals.

 Source table: SAM Success Goal \[samp\_success\_goal\].

**Note:** This widget is available only when the Software Asset Workspace \(com.sn\_sam\_workspace\) plugin is installed.

</td><td>

Not applicable.

</td><td>

Not applicable.

</td></tr><tr><td>

Missing hardware assets

</td><td>

Not applicable.

</td><td>

Count of missing, lost, or stolen hardware assets.

 Source table: Missing Hardware Assets \[missing\_hardware\_assets\].

</td><td>

Not applicable.

</td></tr><tr><td>

Software true-up cost

</td><td>

Cost of the products actually being used.

 Source table: Product Results \[samp\_product\_result\].

</td><td>

Not applicable.

</td><td>

Not applicable.

</td></tr><tr><td>

Expiring contracts in 90 days

</td><td>

Count of software contracts that are going to expire in the next 90 days.

**Note:** If the Software Asset Management application and the Hardware Asset Management application both exist in your instance, then this widget shows the total number of software and hardware contracts together; not individual contracts for software and hardware.

</td><td>

Count of hardware contracts that are going to expire in the next 90 days.

**Note:** If Software Asset Management application and the Hardware Asset Management application both exist in your instance, then this widget shows the total number of software and hardware contracts together; not individual contracts for software and hardware.

</td><td>

Not applicable.

</td></tr><tr><td>

Assets pulled from pool vs net new purchase

</td><td>

Bar charts representing the number of requests for software assets being fulfilled from your inventory versus creating purchase orders for new assets.

**Note:** Ensure that the Procurement \(com.snc.procurement\) plugin is activated in your instance to view software-related data for this widget.

 Source tables:

-   Pool assets: Assigned Allocations \[alm\_licenses\_assigned\].
-   Net new assets: Purchase order line items \[proc\_po\_item\].

</td><td>

Bar charts representing the number of requests for hardware assets being fulfilled from your inventory versus creating purchase orders for new assets.

 Source tables:

-   Pool assets: Consume Asset Task \[consume\_asset\_task\].
-   Net new assets: Purchase order line items \[proc\_po\_item\].

</td><td>

Bar charts representing the number of assets used from your inventory versus new assets being procured via purchase orders.

 Source tables:

-   Pool assets: Spend Report Monthly Cost \[sn\_cld\_spend\_core\_monthly\_cost\].
-   Net new assets: Purchase order line items \[proc\_po\_item\].

</td></tr><tr><td>

End of life models in next 90 days

</td><td>

Number of software models that are reaching their end of life in the next 90 days.

-   End of life
-   End of support
-   End of extended support

 Source table: Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\].

</td><td>

Number of hardware models that are reaching their end of life in the next 90 days.

-   End of life
-   End of support
-   End of extended support

 Source table: Hardware model \[cmdb\_hardware\_model\_lifecycle\].

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

