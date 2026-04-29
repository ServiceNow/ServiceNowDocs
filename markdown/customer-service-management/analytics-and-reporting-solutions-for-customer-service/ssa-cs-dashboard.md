---
title: Self-Service Analytics dashboard for Customer Service Management
description: Measure and track the effectiveness of self-service content through user activities on self-service portals to enrich the content and address any self-service gaps.​
locale: en-US
release: australia
product: Analytics and Reporting Solutions for Customer Service
classification: analytics-and-reporting-solutions-for-customer-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Platform Analytics Solutions for Self-Service Analytics for Customer Service, Analytics and reporting, Customer Service Management]
---

# Self-Service Analytics dashboard for Customer Service Management

Measure and track the effectiveness of self-service content through user activities on self-service portals to enrich the content and address any self-service gaps.​

![Overview tab displaying different widgets such as self-service engagements, successful engagements, success rate, cost saved by channel, deflection activity, resolution by channel, and self-service demand by channel.](../../../product/customer-service-management/image/self-service-dashboard-overview.png "Overview tab")

![Knowledge tab displaying different widgets to analyse the engagements, success rates, and deflection activity.](../../../product/customer-service-management/image/self-service-dashboard-knowledge.png "Knowledge tab")

![Communities tab displaying different widgets to analyse the engagements, success rates, and deflection activity.](../../../product/customer-service-management/image/self-service-dashboard-communities.png "Communities tab")

![Catalog tab displaying different widgets to analyse the engagements, success rates, and deflection activity.](../../../product/customer-service-management/image/self-service-dashboard-catalog.png "Catalog tab")

![Virtual agent tab displaying different tab to analyse the engagements, success rates, and deflection activity.](../../../product/customer-service-management/image/self-service-dashboard-virtual-agent.png "Virtual agent tab")

You can access this dashboard by navigating to **All** &gt; **Platform analytics** &gt; **Library** &gt; **Dashboards**, and search for Self-Service Analytics dashboard. To edit this dashboard, you must set the application scope to **Self-Service Analytics for Customer Service** using the [application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Note:**

-   On the Knowledge tab, you can report knowledge gaps for unsuccessful searches. For more information, see [Report knowledge gaps based on unsuccessful searches](../../performance-analytics/task/report-knowledge-gap-unsucc-search.md).
-   The Communities tab is available when the Communities plugin \(com.sn\_communities\) is activated.
-   The Virtual Agent tab is available when the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) is activated.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Customer service manager: Can view case metrics like backlog, resolution rates, SLA, customer satisfaction, and KPIs to understand the current performance of self-service at an organization.|sn\_customerservice\_manager|

## Use case

-   **Example 1**

    A user faces an issue with a purchased product. To resolve the issue, the user logs in to the portal, and searches for and views content. However, the user does not find any content helpful and creates a case.​

-   **Example 2**

    A user faces an issue with a purchased product. To resolve the issue, the user logs in to the portal, searches for and views content, marks the content as helpful, and continues to do other activities without creating a case.​


The self-service content was available in both examples. However, in example 1, the user did not find the content helpful and therefore it did not help deflect the case creation.​ ​The Self-Service Analytics for Customer Service dashboard enables you to capture not deflected, deflected, or potentially deflected instances with details such as what the user was searching for using the searched terms, the content viewed, and the task created.

## Indicators

Indicators define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time.

When an administrator activates the Self-Service Analytics for Customer Service plugin \(com.snc.pa.self\_service\_analytics\_csm\), the Self-Service Analytics PA \(com.snc.pa.self\_service\_analytics\) is also activated. Both plugins include indicators for the Self-Service Analytics dashboard for customer service.

The Self-Service Analytics for Customer Service plugin includes the following indicators:

-   **Catalog: Deflections**

    A monthly count of catalog requests after which the primary activity \(case creation\) is either found \(no deflection\) or not found \(confirmed or potential deflection\) within an activity window.

-   **Communities: Deflections**

    A monthly count of community content types after which the primary activity \(case creation\) is either found \(no deflection\) or not found \(confirmed or potential deflection\) within an activity window.

-   **Knowledge: Deflections**

    A monthly count of knowledge articles after which the primary activity \(case creation\) is either found \(no deflection\) or not found \(confirmed or potential deflection\) within an activity window.

-   **Number of cases resolved**

    A monthly count of resolutions addressed by customer service agents.

    **Note:** The **Resolutions by Channel** widget on the Overview tab of the Self-Service Analytics dashboard for customer service displays this indicator as **Assisted**.

-   **Number of Deflections**

    A monthly count of deflections for all self-service channels \(Knowledge, Communities, Catalog, Virtual Agent\).

-   **Self-Service: Confirmed Deflections**

    A monthly count of deflections after which the primary activity \(case creation\) was not found depending on the activity type \(helpful knowledge articles, helpful community content, catalog requests\) within an activity window. An increase in value indicates better performance.

-   **Self-Service: Cost Saved**

    A monthly calculation of the cost saving for a deflection. The score is calculated according to the formula `([[Self-Service: Confirmed Deflections]] + [[Self-Service: Potential Deflections]]) * 20`.

    **Note:** By default, the cost saved by each deflection is set to $20. However, you can modify the formula and set a different cost. To edit the formula, navigate to **Performance Analytics** &gt; **Formula Indicators**, search for and click the **Self-Service: Cost Saved** indicator, and edit the numeric value in the **Formula** field. For more information, see [Create a formula indicator](https://www.servicenow.com/docs/access?context=t_CreateAFormulaIndicator&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

-   **Self-Service: Potential Deflections**

    A monthly count of deflections after which the primary activity \(case creation\) was not found depending on the activity type \(knowledge articles views, community content views, Virtual Agent conversations\) within an activity window. An increase in value indicates better performance.

-   **VA: Deflections**

    A monthly count of Virtual Agent conversations after which the primary activity \(case creation\) is not found \(potential deflection\) within an activity window.


The Self-Service Analytics PA plugin includes the following indicators:

-   **Catalog: Percentage of requests**

    A monthly calculation of the percentage of catalog usage compared with the use of other self-service channels. The score is calculated according to the formula `[[Number of Catalog requests]] / ([[Knowledge: Articles viewed this month]] + [[Communities: Views this month]] + [[Number of Catalog requests]] + [[VA: Conversations this month]]) * 100`.

-   **Catalog: Success Rate**

    A monthly calculation of the percentage indicating the success of the catalog as a self-service channel. The score is calculated according to the formula `[[Number of Catalog requests]] / [[Catalog: Views this month]] * 100`.

-   **Catalog: Views this month**

    A monthly count of catalog item views. An increase in value indicates better performance.

-   **Communities: Helpful Feedback**

    A monthly count of helpful Community content types.

-   **Communities: Percentage of community viewed**

    A monthly calculation of the percentage of Community content types usage compared with the usage of other self-service channels. The score is calculated according to the formula `[[Communities: Views this month]] / ([[Communities: Views this month]] + [[Knowledge: Articles viewed this month]] + [[Number of Catalog requests]] + [[VA: Conversations this month]]) * 100`.

-   **Communities: Views this month**

    A monthly count of Community content type views. An increase in value indicates better performance.

-   **Knowledge: Articles viewed this month**

    A monthly count of knowledge articles views. An increase in value indicates better performance.

-   **Knowledge: Helpful Feedback**

    A monthly count of knowledge articles marked as helpful or rated either 4 or 5.

-   **Knowledge: Percentage of articles viewed**

    A monthly calculation of the percentage of knowledge articles usage compared with the usage of other self-service channels. The score is calculated according to the formula `[[Knowledge: Articles viewed this month]] / ([[Knowledge: Articles viewed this month]] + [[Communities: Views this month]] + [[Number of Catalog requests]] + [[VA: Conversations this month]]) * 100`.

-   **Number of Catalog requests**

    A monthly count of catalog requests.

-   **Percentage of helpful Community Content**

    A monthly calculation of the percentage indicating the success of Communities as a self-service channel. The score is calculated according to the formula `[[Communities: Helpful Feedback]] / [[Communities: Views this month]] * 100`.

-   **Percentage of helpful Knowledge Articles**

    A monthly calculation of the percentage indicating the success of Knowledge as a self-service channel. The score is calculated according to the formula `[[Knowledge: Helpful Feedback]] / [[Knowledge: Articles viewed this month]] * 100`.

-   **Self-Service: Engagements**

    A monthly calculation of the total of views from all self-service channels. The score is calculated according to the formula `[[Knowledge: Articles viewed this month]] + [[Communities: Views this month]] + [[Catalog: Views this month]] + [[VA: Conversations this month]]`.

-   **Self-Service: Success Rate**

    A monthly calculation of the percentage indicating the success of self-service channels. The score is calculated according to the formula `[[Self-Service: Successful Engagements]] / [[Self-Service: Engagements]] * 100`

-   **Self-Service: Successful Engagements**

    A monthly count of helpful content from all self-service channels. The score is calculated according to the formula `[[Knowledge: Helpful Feedback]] + [[Communities: Helpful Feedback]] + [[Number of Catalog requests]] + [[VA: Successful Conversations]]`.

-   **VA: Conversations this month**

    A monthly count of Virtual Agent conversations. An increase in value indicates better performance.

-   **VA: Percentage of Conversations**

    A monthly calculation of the percentage of Virtual Agent conversation usage compared with the usage of other self-service channels. The score is calculated according to the formula `[[VA: Conversations this month]] / ([[Knowledge: Articles viewed this month]] + [[Communities: Views this month]] + [[Catalog: Views this month]] + [[VA: Conversations this month]]) * 100`.

-   **VA: Success Rate**

    A monthly calculation of the percentage indicating the success of Virtual Agent as a self-service channel. The score is calculated according to the formula `[[VA: Successful Conversations]] / [[VA: Conversations this month]] * 100`

-   **VA: Successful Conversations**

    A monthly count of Virtual Agent conversations that were not directed to live agents. An increase in value indicates better performance.


## Breakdowns

Breakdowns enable you to group or filter indicator scores by a qualitative attribute.

This dashboard includes the following breakdowns:

-   **Channel**

    Enables you to view indicator scores by a self-service channel such as Knowledge, Communities, Catalog, or Virtual Agents.

-   **Communities Content Type**

    Enables you to view indicator scores by a Community content type such as answer, blog, comment, document, event, question, or video.

-   **Knowledge Base**

    Enables you to view indicator scores by knowledge base.

-   **Knowledge Category**

    Enables you to view indicator scores by knowledge article category.

-   **Type of Deflection**

    Enables you to view indicator scores by deflection type: no deflection, confirmed deflection, and potential deflection.


## Data visualization

|Title|Type|Description|
|-----|----|-----------|
|Unsuccessful Searches|Bar ![Bar icon.](../../performance-analytics/image/column-icon.png)|A monthly collection of searches for knowledge articles with no results or results with no clicks.|

**Related topics**  


[Self-Service Analytics](https://www.servicenow.com/docs/access?context=self-service-analytics&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

