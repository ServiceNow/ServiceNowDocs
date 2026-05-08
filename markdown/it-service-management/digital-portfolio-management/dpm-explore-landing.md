---
title: Digital Portfolio Management Workspace homepage
description: The Digital Portfolio Management \(DPM\) Workspace homepage is the starting point where you navigate to all aspects of your solutions and portfolios. You’re encouraged to personalize your Digital Portfolio Management \(DPM\) homepage so you can view and track the solutions that matter to you most.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Digital Portfolio Management, IT Service Management]
---

# Digital Portfolio Management Workspace homepage

The Digital Portfolio Management \(DPM\) Workspace homepage is the starting point where you navigate to all aspects of your solutions and portfolios. You’re encouraged to personalize your Digital Portfolio Management \(DPM\) homepage so you can view and track the solutions that matter to you most.

## DPM Workspace overview

The DPM homepage \(![Home.](../image/home-polaris-primary2x.png)\) is the central area where you see the status of all your solutions. To access DPM, log in to your provided ServiceNow instance and then select **Workspaces &gt; Digital Portfolio Management**. When you first log in to the DPM Workspace, the system uses certain fields to generate a set of default solution cards that display on your homepage. After you personalize your homepage, the system remembers your updates in the **dpm\_home\_page\_item** table so that next time you log in to the workspace, your personalized homepage displays. For information on the first login solution cards, see [Digital Portfolio Management homepage default solution cards](../reference/dpm-oob-solution-card-fields.md).

The homepage includes the following main areas.

-   A personalized message that welcomes you and a link to an overview video about DPM.
-   A Current status section that contains solution cards with solutions that you’re associated with based on system-defined fields. You're encouraged to personalize the solutions in this section. The layout enables you to see a holistic picture of all solutions you care about.

    **Tip:** If you don't see any solution cards \(an empty state\), select **Add items** to add solutions to your homepage.

-   Solution cards list needs attention attributes, which vary depending on the type of solution. At a glance, you can see each attribute name and the number of times it affects the solution. Also, the color and status icon determine if the needs attention attribute marks the solution as good, moderate, or critical.

    **Note:** The data on each solution card reflects current data at the time that you view the page. Refresh the page \(![Refresh icon](../../site-reliability-ops/image/icon-refresh.png)\) to update the data.

-   Fields to enable you to search, filter, and personalize what you see on your DPM Workspace homepage. For more information, see [Personalize the Digital Portfolio Management Workspace home page](../task/dpm-personalize-homepage.md).
-   A Personal portfolios section that shows personal portfolios that you recently visited in DPM. You can also select the link to go to the personal portfolios page.
-   An Enterprise portfolios section that shows enterprise portfolios that you recently visited in DPM. You can also select the link to go to the enterprise portfolios page.
-   A Recently viewed section that shows items that you recently visited in DPM.

## Current status solution cards

You're encouraged to personalize the Current status section to see those solutions that matter to you most. Each solution card provides you with detailed information about your solutions. See the image and corresponding numbers for more information.

![DPM homepage solution card overview](../image/dpm-homepage-solution-card-overview.png)

**Important:** For the Australia release and later, the labels for the items in the \[cmdb\_ci\_service\_technical\] table and \[service\_offering\] table are Technology Management Service and Technology Management Service Offering, respectively. Prior to the Australia release, the labels are technology management service and technology management service Offering.

1.  Solution name and type \(service, service offering, business application, or service instance\).
2.  Actions menu ![Actions menu icon](../../../administer/on-call-scheduling/image/icon-actions.png) to view the solution's details, its relationship map, or remove the item from your homepage. For more information, see [Personalize the Digital Portfolio Management Workspace home page](../task/dpm-personalize-homepage.md).
3.  Needs attention attributes that determine the status of each card. Needs attention attributes differ based on the solution type.

## Needs attention default thresholds

DPM comes with default thresholds for Needs attention attributes. You’re encouraged to personalize the thresholds to define your metrics for good, moderate, and severe. See [Personalize the Digital Portfolio Management Workspace home page](../task/dpm-personalize-homepage.md).

<table id="table_gnb_ls5_bzb"><thead><tr><th>

Color

</th><th>

Symbol

</th><th>

Meaning

</th><th>

Default threshold

</th></tr></thead><tbody><tr><td>

Green

</td><td>

![Green circle](../image/dpm-na-green-check.png)

</td><td>

Good

</td><td>

No value \(empty\)

</td></tr><tr><td>

Orange

</td><td>

![Orange circle](../image/dpm-na-amber-circle.png)

</td><td>

Moderate

</td><td>

-   Critical incidents: Empty
-   Outages: Empty
-   Changes: Empty
-   Alerts: 3
-   Risks: 1
-   Audits: Empty

</td></tr><tr><td>

Red

</td><td>

![Red circle](../image/dpm-na-red-triangle.png)

</td><td>

Severe

</td><td>

-   Critical incidents: 1
-   Outages: 1
-   Changes: Empty
-   Alerts: 10
-   Risks: 3
-   Audits: Empty

</td></tr></tbody>
</table>## Browser support for workspaces

**Important:** Due to significant performance issues, ServiceNow recommends that customers migrate away from Internet Explorer 11. For more information, refer to [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275).

**Related topics**  


[Digital Portfolio Management homepage default solution cards](../reference/dpm-oob-solution-card-fields.md)

[Personalize the Digital Portfolio Management Workspace home page](../task/dpm-personalize-homepage.md)

[bundle-platux.list-of-workspaces]

