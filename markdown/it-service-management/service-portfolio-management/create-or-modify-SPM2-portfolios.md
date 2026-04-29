---
title: Create portfolios in Service Portfolio Management
description: You can create a single service portfolio or multiple service portfolios, each with its own taxonomy structure. The service portfolio enables you to see an overall view of your current IT services. You can also see services that may be available in the future and services that existed in the past.
locale: en-US
release: australia
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, Service Portfolio Management, IT Service Management]
---

# Create portfolios in Service Portfolio Management

You can create a single service portfolio or multiple service portfolios, each with its own taxonomy structure. The service portfolio enables you to see an overall view of your current IT services. You can also see services that may be available in the future and services that existed in the past.

## Before you begin

Role required: portfolio\_admin

## About this task

Create a service portfolio before you define taxonomy nodes. After you create the service portfolio, you can edit it within the platform and monitor its performance in Digital Portfolio Management \(DPM\).

**Important:** Existing customers can opt in to the improved portfolio structure by navigating to **Service Portfolio Management** &gt; **Administration** &gt; **Configuration** &gt; **New Portfolio Opt-In**. The improved structure uses nodes and doesn't use layers and weighted scores from the Service Owner Workspace. After customers opt in for the improved portfolio structure, there isn’t an option to revert to the former structure. For more information, see [Service Portfolio Management portfolios](../concept/SPM2-service-portfolios.md). New customers have the improved portfolio structure by default.

**Note:** The following procedure reflects the **SPM Advanced** user view.

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service Portfolios** and select **New**.

2.  On the form, fill in the fields.

<table id="table_tdm_5n2_4gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name that reflects the nature of the service portfolio, for example, IT Service Portfolio.

</td></tr><tr><td>

Short description

</td><td>

Brief details about the service portfolio.

</td></tr><tr><td>

Description

</td><td>

Comprehensive details about the service portfolio, such as, Software and Network Support Tiers.

</td></tr><tr><td>

Market scope

</td><td>

Detailed service parameters that define the limits of a service. For example, who uses the portfolio services.

</td></tr><tr><td>

Service portfolio owner

</td><td>

Person who owns the portfolio, usually at the Chief Information Officer \(CIO\) level. This person has the portfolio\_editor role and can view and update owned portfolios only.

</td></tr><tr><td>

Service portfolio manager

</td><td>

Person who has the portfolio\_admin role and is authorized to manage the service portfolio. The portfolio\_admin can create, read, update, and delete portfolio records of all types, including: -   Portfolios
-   Taxonomy levels and nodes
-   Services and service offerings
-   Relationships
-   Performance criteria


</td></tr><tr><td>

Auto-create service offerings

</td><td>

When checked, the **Number of offerings per service** field displays, enabling you to select the number of service offerings to auto-create.

 Every service must have a service offering. When you create a service offering using the auto-create check box, the following happens:

-   Service offerings are created with the naming convention of **&lt;service name&gt; Offering1**. The number represents the number of offerings that you created. If you created two, then the second offering name is **&lt;service name&gt; Offering2**.
-   The service offering inherits the following fields from the parent service:
    -   Owned by
    -   Delivery manager
    -   Delegate
    -   State
    -   Service classification
-   The auto-created service offerings are located in the Offerings related link of the service.


</td></tr><tr><td colspan="2">

**Important:** The following performance fields only appear if you're using the deprecated Service Owner Workspace plugin. For more information on the deprecation of Service Owner Workspace, see .

</td></tr><tr><td>

Upper performance score threshold

</td><td>

Designated high threshold percentage point above which the indicators change from amber to green in Service Owner Workspace. In addition to the color change, the default percentage is **80**.

</td></tr><tr><td>

Lower performance score threshold

</td><td>

Designated low threshold percentage point below which the indicators change from amber to red in Service Owner Workspace. In addition to the color change, the default percentage is **60**.

</td></tr><tr><td>

Add default performance metrics

</td><td>

Option to add five metrics when you create a service portfolio. You can choose not to add the metrics by clearing the check box.Default metrics added include:

-   Availability
-   Customer Satisfaction
-   Critical Incidents
-   Activity
-   Breached service level agreement \(SLA\)
 **Note:** This field is hidden on Service Portfolio records. It only appears when you create a record.

</td></tr><tr><td>

Evenly weight performance metrics for new offerings

</td><td>

When active, each time an offering is created as part of this portfolio, the performance weight of each metric is evenly distributed. For example, each default metric is weighted at 20%.

</td></tr></tbody>
</table>    **Note:** If your instance is integrated with Financial Management and the **Estimated Spend** **Cost model** fields are configured on the Service Offering form, then you 'd see the **Estimated Spend** details for the portfolio.

3.  Select **Submit** to save your service portfolio or select **Update** after editing.

    The newly created service portfolio appears in the **Service Portfolios** module list.

4.  Select the newly created service portfolio name in the list.

    The Taxonomy Nodes, Portfolio Metrics, and Taxonomy Node Weights related lists appear on the Service Portfolio form. See [Service Portfolio Management taxonomy](../concept/SPM2-taxonomy.md) for detailed information regarding creating and adding taxonomy nodes within your service portfolio structure.


-   **[Service Portfolio Management taxonomy](../concept/SPM2-taxonomy.md)**  
Service Portfolio Management uses a taxonomy framework to organize and manage services in a portfolio.

**Parent Topic:**[Using Service Portfolio Management](../concept/SPM2-using.md)

