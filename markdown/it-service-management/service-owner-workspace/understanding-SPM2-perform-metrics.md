---
title: Service Owner Workspace performance metrics
description: Service Owner Workspace includes a metrics model in the platform Service Portfolio Management Premium application for measuring the performance of services offerings. These performance metrics are then aggregated to services and taxonomy nodes via a weighting mechanism.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Exploring Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Service Owner Workspace performance metrics

Service Owner Workspace includes a metrics model in the platform Service Portfolio Management Premium application for measuring the performance of services offerings. These performance metrics are then aggregated to services and taxonomy nodes via a weighting mechanism.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. Customers who opt in for the new standard portfolio structure use metrics calculated from key performance indicators \(KPIs\) in Digital Portfolio Management \(DPM\). For more information, see [Digital Portfolio Management](../../digital-portfolio-management/reference/dpm-landing.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Navigate](../image/SOWExploreBanner2.png "Navigate")

</td></tr></tbody>
</table>## Metric Definitions

When activated, Service Portfolio Management Premium collects service offering metrics which permit calculations to roll up to parent services and taxonomy nodes for performance scores and other metrics. All metric configurations are performed in the platform application. Service owners can view these performance scores and metrics via Service Owner Workspace. The following **Metric Definitions** are installed with the Service Portfolio Management Premium plugin \(com.snc.spm\):

-   **Activity**

    The metric indicator is from service portfolio-related catalog activity. The metric is calculated from fulfilled request items derived from catalog items, which are connected to service offerings.

-   **Availability**

    The metric indicator is Service Portfolio Management availability as calculated from outage records.

    **Note:** If more than one Availability commitment exists for a service offering, at least one must be set as the Primary for trending purposes. Only one availability commitment is considered for performance score calculation, determined by the **Use in performance score** flag. Additional features include:

    -   Creation of Availability definitions specific to describe Availabilities for service offerings.
    -   Directly link a service offering commitment to an Availability definition.
    -   Maintain Availability statistics regarding outages.
-   **Breached SLA**

    The metric indicator is from an SLA record, based on a breached SLA. Calculations depend on activation of the Service Portfolio Management SLA Commitments plugin \(com.snc.service\_portfolio.sla\_commitment\), which enables the following features:

    -   Creation of SLA definitions specific to describe the SLAs in place for service offerings.
    -   Directly link a service offering commitment to an SLA definition.
    -   Maintain SLA statistics regarding breaches.

        **Note:** If more than one SLA commitment exists for an offering, at least one must be set as the Primary for use in performance scoring. Only one SLA commitment is considered for performance score calculation, determined by the**Use in performance score** flag.

-   **Customer Satisfaction**

    Calculations are tabulated from surveys sent to unique subscribers to an offering.

-   **Critical Incidents**

    The metric indicator is calculated from a combination of daily P1 and major incident counts. You will need to update the lower and upper boundary for this metric. For details refer to [Service offering performance weighting](understanding-SPM2-perform-metrics.md#section_service-offering-perform-weighting).


**Note:** Prior to the Quebec release, the **Critical Incidents** metric was called **Stability** and was depicted as a single score widget on the **Trends** tab the workspace. The data currently appears as a time series chart. The default time frame for Service Owner Workspace metric performance is 30 days, except for the **Critical Incidents** metric, which shows all open major and P1 incidents per day.

## Service offering performance weighting

Service owners can vary the inclusion and weighting of service offering metrics to reflect the business needs and perspectives of their stakeholders. Metrics are normalized and weighted to determine the performance of an offering. Metrics are only maintained for service offerings with an operational status. Weights must equal 100 percent.

To disable a service offering metric with unavailable or unreliable data from performance calculations, you can set the metric weight to 0 in the platform Service Portfolio Management Premium application.

Click the **Edit Metric Weights** Related Link on the **Service Offering** form to edit the upper and lower boundaries for each metric. The **Maintenance** pop-up window appears for you to customize per service offering. The upper and lower boundaries define how a metric is measured against a 0 through 100 percent scale and normalized together. To obtain a 100% score for negative metrics, such as for Critical Incidents, the score must be below or equal to the lower boundary.

![Service offering Edit Metric Weights related link](../image/EditSOWMetricWeights.png "Service offering Edit Metric Weights")

## Service offering to service performance weighting

Service owners can vary the inclusion and weighting of the service offering in service performance to reflect the business needs and perspectives of their stakeholders. Service offering performance is weighted and combined to determine the performance of a service. Only offerings with an operational status are used to contribute to service performance.

Set a service offering weight to 0 to disable it from the performance calculations of its parent service.

Click the **Edit Weights** Related Link on the **Services** form to edit the weights for associated offerings. Weights are valued against a 0 through 100 percent scale and normalized together.

![Service Edit Weights related link](../image/EditServiceWeights.png "Service offering to service performance Edit Weights")

**Note:** Upper and lower weight boundaries can be anything, from negative numbers to thousands of numbers. They do not have to be 0 to 100. But the outcome of the linear ranging math is to use those boundaries to make a normalized number between 0% and 100%.

For example, the normalization process dictates, that if you choose -20 and 150 as lower and upper boundaries, then anything at -20 or below will get normalized to 0% and anything at or above 150 will get normalized to 100%. Every number in between -20 and 150 is scaled to within the 0 through 100 range.

Another way to describe the normalization process is, for example, if you choose 5 and 150 as lower and upper boundaries and the metric is negative \(minimize\). With this metric anything below or equal to 5 gets a normalized score of 100%. Therefore, for a negative metric, the lower the raw score is, the higher the normalized score, which is capped at 100%. If you choose 5 and 150 as lower and upper boundaries and the metric is positive \(maximize\), then anything below or equal to 5 will get a normalized score of 0%.

## Service to nodes performance weighting

Portfolio owners and editors can vary the inclusion and weighting of services in node performance to reflect the business needs and perspectives of their stakeholders. Service performance is weighted and combined to determine the performance of sublevel taxonomy nodes, also called child nodes.

Use the **Edit Weights** Related Link on the **Taxonomy Nodes** form to edit the associated service weights. Service weights are valued against a 0 through 100 percent scale and normalized together.

![Taxonomy node Edit Weights related link](../image/EditTaxoNodeWeights.png "Service to nodes Edit Weights")

## Node to node performance weighting

Portfolio owners and editors can vary the inclusion and weighting of node in node performance to reflect the business needs and perspectives of their stakeholders. Node performance is weighted and combined to determine the performance of taxonomy parent nodes.

## Performance scores

The performance score for services and offerings are highlighted with a different color in Service Owner Workspace based on the configured threshold limit defined on the portfolio record.

-   Red: Indicates the score is lower than the set threshold limit.
-   Amber: Indicates the score is within the set threshold.
-   Green: Indicates the score is higher than the set threshold limit.

![Performance score indicators](../image/PerformanceScoreIndicatorColors.png "Performance score indicators")

## Metrics configuration

To view or configure Service Owner Workspace metric definitions, refer to [Configure Service Owner Workspace metric definitions](../task/view-or-config-SPM2-metric-def.md).

To view or configure Service Owner Workspace portfolio metrics, refer to [Configure Service Owner Workspace portfolio metrics](../task/view-or-config-SPM2-portfolio-metrics.md).

