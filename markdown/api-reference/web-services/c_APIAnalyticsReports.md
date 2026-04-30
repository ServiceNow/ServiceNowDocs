---
title: View REST &amp; SOAP API analytics
description: View overall API analytics, analytics per API, or analytics per requesting user in the REST &amp; SOAP API Analytics dashboard.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Analyze REST and SOAP API usage, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# View REST &amp; SOAP API analytics

View overall API analytics, analytics per API, or analytics per requesting user in the REST &amp; SOAP API Analytics dashboard.

## Before you begin

Role required: api\_analytics\_read, web\_service\_admin, or admin

## About this task

The REST &amp; SOAP API Analytics dashboard contains Usage Overview, Usage by API, and Usage by Requestor analytics. From the Usage by API and Usage by Requestor tabs, you can filter by API and requestor get more specific insights.

![Usage Overview tab of the REST & SOAP API Analytics dashboard.](../image/analytics-usage-overview.png "REST & SOAP API Analytics dashboard")

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Analytics Usage Overview** to open the REST &amp; SOAP API Analytics dashboard.

    **Tip:** You can also access the dashboard from the context menu in the REST API Explorer or from the **API analytics** related link in custom web services forms.

2.  Select one of the following tabs in the dashboard.

<table id="choicetable_trp_2cg_z1c"><thead><tr><th align="left" id="d773013e108">

Option

</th><th align="left" id="d773013e111">

Action

</th></tr></thead><tbody><tr><td id="d773013e117">

**Usage Overview**

</td><td>

View general usage statistics for all REST and SOAP APIs.

</td></tr><tr><td id="d773013e126">

**Usage by API**

</td><td>

View detailed usage statistics for each API. 1.  From the **API Stats by API** menu, select one or more APIs.
2.  Move the selected APIs to the **Applied** list.
3.  Select **Apply**.


</td></tr><tr><td id="d773013e155">

**Usage by Requestor**

</td><td>

View detailed usage statistics for each requesting user. 1.  Specify the API requestor analytics to view.
    1.  From the **API Stats by Requestor** menu, select one or more requestors.
    2.  Move the selected requestors to the **Applied** list.
    3.  Select **Apply**.
2.  Specify the API analytics to view.
    1.  From the **API Stats by API** menu, select one or more APIs.
    2.  Move the selected APIs to the **Applied** list.
    3.  Select **Apply**.
If the selected user has not made requests to the selected API, no data is shown for that combination.

</td></tr></tbody>
</table>
**Parent Topic:**[Analyze REST and SOAP API usage](c_APIAnalytics.md)

**Related topics**  


[Use the REST API Explorer](../../inbound-rest/concept/use-REST-API-Explorer.md)

[Dashboards in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

