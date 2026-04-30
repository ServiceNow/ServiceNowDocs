---
title: Classic HR Service Delivery Agent Workspace landing page
description: The first thing HR agents see when accessing HR Agent Workspace is the landing page. The landing page provides a personalized and engaging experience for the HR agent.In order to modify a landing page supplied by the base system, you must first make a copy.You can configure how your Create a new case form looks in HR Service Delivery Agent Workspace.Use the sn\_hr\_ws.case\_creation\_tabs system property to add or delete the tabs that appear at initial case creation.Use the Card List Configuration to configure the cards that appear on the HR Service Delivery Agent Workspace landing page.Use the Land Page Tag Configuration to define the tags to display on the cards list configuration.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Setting up HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Classic HR Service Delivery Agent Workspace landing page

The first thing HR agents see when accessing HR Agent Workspace is the landing page. The landing page provides a personalized and engaging experience for the HR agent.

![HR Agent WS - Landing page](../image/agent-ws-hr-landing-page2.png)

The landing page shows high priority cases, cases at risk for violating service level agreements \(SLA\), and cases with recent changes.

Information related to the teams your HR agents belong to display below the Overview section.

The bottom of the landing page provides company information, links, and tools available. This section is part of Content Delivery. For more information, see [Content Library](../../employee-center/concept/ec-streamline-content.md).

![HR Agent WS - Landing Page](../image/agent-ws-hr-landing-cont-delivery.png)

## Configuration

The base system provides two \(2\) landing pages:

-   HR Landing Page
-   HR Landing Page \(CD\)

The Landing Page \(CD\) is available when the Content Delivery \(com.sn\_content\_delivery\) plugin is activated. The base system provides the ability to configure your landing pages in a limited manner.

-   Card List Configuration: Determines which cards display in the middle section of the landing page.
-   Card Tag Configuration: Determines which tags appear on the cards.

For more information, see:

-   [Configure the Card List Configuration for the Classic HR Agent Workspace landing page](agent-ws-hr-landing-pg.md#)
-   [Configure the Tag Configuration for the Classic HR Agent Workspace landing page](agent-ws-hr-landing-pg.md#)

## Modifying your landing page

The base system landing pages can only be modified if you make a copy first.

**Note:** For more information on configuring a new landing page, see Setting up landing pages in a workspace.

## Classic HR Service Delivery Agent Workspace landing page

In order to modify a landing page supplied by the base system, you must first make a copy.

To make a copy of your landing page, use the UI Builder. For more information, see [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Classic HR Service Delivery Agent Workspace Create a new case form

You can configure how your **Create a new case** form looks in HR Service Delivery Agent Workspace.

The **Create a new case** form shows two tabs when creating a new HR case.![HR Agent WS New case form](../image/agent-ws-hr-new-case-form.png)

Use the sn\_hr\_ws.case\_creation\_tabs system property to add or delete the tabs that appear at initial case creation.

**Note:** The **Description** field in the sn\_hr\_ws.case\_creation\_tabs system property provides information on how to add a new array object for new tab entries. To delete a tab, remove the tab array object. For more information on, see [Add or delete tabs from the Create new case form](agent-ws-hr-landing-pg.md#).

After entering an employee or case number, the **Cases for opened for** tab appears if the employee has additional cases associated cases.

### Add or delete tabs from the Create new case form

Use the sn\_hr\_ws.case\_creation\_tabs system property to add or delete the tabs that appear at initial case creation.

#### Before you begin

Role required: admin

The **Description** field in the sn\_hr\_ws.case\_creation\_tabs system property provides information on how to add a new array object for new tab entries. To delete a tab, remove the tab array object.

#### Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Search for and display the **sn\_hr\_ws.case\_creation\_tabs** system property.

3.  In the **Value** field, scroll down to the **"title":"interactions"** object from the array.

    ![Sys property sn_hr_ws.case_creation_tabs](../image/sn_hr_ws.case_creation_tabs.png)

4.  Remove the text highlighted above.

5.  Select **Update**.


## Configure the Card List Configuration for the Classic HR Agent Workspace landing page

Use the Card List Configuration to configure the cards that appear on the HR Service Delivery Agent Workspace landing page.

### Before you begin

Role required: sn\_hr\_core.admin

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Landing Page** &gt; **Card List Configurations**.

    The base system provides three \(3\) pre-configured records:

    -   **SLAs at risk**
    -   **High priority cases**
    -   **All cases**
    ![HR Agent WS - Card List Configuration](../image/agent-ws-hr-card-list-config.png)

2.  Select one of the pre-configured records or **New**.

3.  Complete or edit the fields on the form.

<table id="table_tql_pxt_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

A description of the record.

</td></tr><tr><td>

Query

</td><td>

A set of conditions that when valid determine what appears on the landing page.For example, to show all high priority HR cases for the logged in agent:

-   Active is true
-   Select AND OR
-   Assigned to is \(dynamic\) Me
-   Select AND OR
-   Priority is one of 1 - Critical 2 - High
-   Select AND OR


</td></tr><tr><td>

Application

</td><td>

The application that contains this record.

</td></tr><tr><td>

Text to view all records

</td><td>

Text that appears when the record has data.

</td></tr><tr><td>

Text to display if list is empty

</td><td>

Text that appears when the list has no data.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


## Configure the Tag Configuration for the Classic HR Agent Workspace landing page

Use the Land Page Tag Configuration to define the tags to display on the cards list configuration.

### Before you begin

Role required: sn\_hr\_core.admin

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Landing Page** &gt; **Card Tag Configurations**.

    The base system provides three \(3\) pre-configured records:

    -   SLA
    -   Blue "VIP" if opened for or subject person is VIP
    -   Green "New" if created in last 24 hours
    ![HR Agent WS - Card List Configuration](../image/agent-ws-hr-card-tag-config.png)

2.  Select one of the pre-configured records or **New**.

3.  Complete or edit the fields on the form.

<table id="table_mrt_d35_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

A description of the tag configuration record.

</td></tr><tr><td>

Type

</td><td>

The type of tag configuration record:-   Highlighted value
-   SLA Timer


</td></tr><tr><td>

SLA timer configuration

</td><td>

The configuration of the SLA timer that determines which task SLA displays as part of the timer component.**Note:** For more information, see [SLA timer configurations](https://www.servicenow.com/docs/access?context=sla-timer-configurations&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

 Field appears when you select **SLA Timer** in the **Type** field.

</td></tr><tr><td>

Tag text

</td><td>

Text that appears for the tag on the card.Field appears when you select **Highlighted value** in the **Type** field.

</td></tr><tr><td>

Color

</td><td>

The color you want the tag to appear as. Each color has a meaning:-   critical = Red
-   high = Orange
-   warning = Yellow
-   moderate = Purple
-   positive = Green
-   info \(VIP\) = Blue
-   low = Gray


</td></tr><tr><td>

Condition

</td><td>

Applies this configuration when specific conditions are met.For example, conditions when to flag for a VIP are:

-   Opened for.VIP is true
-   Or
-   Subject person.VIP is true
 The fields available to you to create a condition are from the HR case \[sn\_hr\_case\] table.

 **Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Application

</td><td>

The application that contains this record.

</td></tr><tr><td>

Order

</td><td>

Order in which the configuration processes first. Configurations with lower numbers process first.

</td></tr><tr><td>

Icon

</td><td>

Use to display an icon for any non-SLA tag.**Note:** For more information, see [Icon](https://developer.servicenow.com/dev.do#!/reference/libraries/sandiego/now-components/now-icon/gallery).

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


