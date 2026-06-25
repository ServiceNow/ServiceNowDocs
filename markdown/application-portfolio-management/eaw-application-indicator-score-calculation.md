---
title: Application indicator score calculation in Enterprise Architecture Workspace
description: Enterprise Architecture Workspace calculates a composite score for each business application and business capability by running data from configured indicators through a multi-step pipeline that normalizes raw values, applies weighted contributions, and aggregates the results into a final score per fiscal period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-application-indicator-score-calculation.html
release: australia
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 6
breadcrumb: [Rationalization of business applications, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Application indicator score calculation in Enterprise Architecture Workspace

Enterprise Architecture Workspace calculates a composite score for each business application and business capability by running data from configured indicators through a multi-step pipeline that normalizes raw values, applies weighted contributions, and aggregates the results into a final score per fiscal period.

## Scoring pipeline overview

An indicator is a single metric or measure of a particular aspect of a business application or business capability. Indicators can be subjective, such as assessment responses, or objective, such as operational or risk data from the CSDM service graph — for example, the number of incidents linked to an application.

By running indicators through a consistent scoring pipeline, Enterprise Architecture Workspace confirms that applications assessed on different data types—such as assessment responses, change counts, or custom script outputs—can be compared meaningfully on a single score. Scores are stored per application per fiscal period, so historical data is preserved across scoring runs.

Administrators control which indicators contribute to a profile, how they are weighted, and whether fixed or dynamic value ranges are used during normalization.

## Key tables

|Table|Label|Role|
|-----|-----|----|
|apm\_application\_profile|Scoring Profile|Groups indicators together. One profile is assigned to each business application.|
|apm\_application\_profile\_indicator|Profile Indicator|Maps an indicator to a profile and stores the weight value for that profile.|
|apm\_metric|Indicator|Defines the data source, direction, and normalization settings for each indicator.|
|apm\_app\_indicator\_score|Indicator Score|Stores the per-indicator, per-application, per-fiscal-period score after the pipeline runs.|
|apm\_app\_score|Application Score|Stores the final aggregated score per application per fiscal period.|

## Raw weight collection by indicator type

Each indicator has a data source that determines how the raw weight is collected for each business application.

|Indicator type|Data source value|How the raw weight is collected|
|--------------|-----------------|-------------------------------|
|Performance Analytics|pa|Pulls a value from the configured Platform Analytics indicator for the fiscal period. The breakdown must target the same CI class as the profile \(for example, Business Application\).|
|Custom script|script|Executes the script defined on the indicator. The script must return a JSON object that contains the application sys\_id and the corresponding weight.|
|Query condition|condition|Runs a GlideAggregate query on the configured table and filter, then aggregates results using the selected method: SUM, COUNT, AVERAGE, MIN, or MAX.|
|Assessment|assessment|Aggregates assessment metric results for the fiscal period across all assessment groups that are associated with the application.|
|Composite \(parent indicator\)|indicators|Sums the normalized values of all child indicators for each application. Only the parent indicator's weightage is counted in the profile score.|

## Normalization

After the raw weight is collected for each application, the system normalizes the value to a 1–10 scale so that indicators using different units and ranges can be combined meaningfully. Regardless of direction, a normalized value of 10 always represents the best-performing application for that indicator, and 1 represents the worst. The Direction setting controls how the raw value maps to this scale.

<table id="table_szl_ys5_hjc"><thead><tr><th>

Condition

</th><th>

Formula

</th></tr></thead><tbody><tr><td>

All applications have the same raw weight \(max equals min\)

</td><td>

```
normalizedValue = 10
```

</td></tr><tr><td>

Direction = Maximize \(the application with the highest raw value scores 10; the application with the lowest raw value scores 1; for example, Business Valu\)

</td><td>

```
normalizedValue =
  (((appWeight − minWeight) /
    (maxWeight − minWeight)) × 9) + 1
```

</td></tr><tr><td>

Direction = Minimize \(the application with the lowest raw value scores 10; the application with the highest raw value scores 1; for example, Incident Count\)

</td><td>

```
normalizedValue =
  10 − (((appWeight − minWeight) /
          (maxWeight − minWeight)) × 9)
```

</td></tr></tbody>
</table>In the formulas:

-   `appWeight` is the raw value for this application.
-   `minWeight` and `maxWeight` are the lowest and highest raw values across all applications for this indicator in the fiscal period. If **Consider absolute values** is selected on the indicator, the system uses the **Target minimum** and **Target maximum** values from the indicator record instead.

**Note:** Assessment-type indicators don't support **Target maximum** and **Target minimum** fields. The system uses 1 as the minimum and 10 as the maximum automatically for assessments.

If a **Normalization script** is defined on the indicator record, it overrides the standard formulas preceding.

## Indicator score

The indicator score represents the contribution of one indicator to the overall application score, proportional to its weightage in the profile.

```
indicatorScore =
  normalizedValue × indicatorWeightage / totalProfileWeightage
```

`totalProfileWeightage` is the sum of weightage values across all indicators in the same scoring profile. All values are rounded to two decimal places.

## Assessment-based indicator example

This example shows how an indicator score is calculated for a single business application using an assessment-based indicator in one fiscal period.

Setup: A scoring profile has three indicators, each with a weightage of 33 \(total profile weightage = 99\). One indicator is a Business Fit assessment indicator. Two assessment groups fall within the fiscal period for this application.

|Calculation step|Value|How it is calculated|
|----------------|-----|--------------------|
|Assessment group 1 — average rating|4.7|SUM of metric results for the application ÷ number of results in the assessment group.|
|Assessment group 1 — application weight|9.46|\(scaleFactor × rating\) + 1, where scaleFactor = 9 ÷ 5 = 1.80. Result: \(1.80 × 4.7\) + 1.|
|Assessment group 2 — average rating|4.5|Calculated the same way as assessment group 1.|
|Assessment group 2 — application weight|9.10|\(1.80 × 4.5\) + 1.|
|Normalized value|9.28|Total application weight ÷ number of assessment groups: \(9.46 + 9.10\) ÷ 2.|
|Indicator weightage|33|Configured on the profile indicator record.|
|Total profile weightage|99|33 + 33 + 33 \(sum of all indicator weightages in the profile\).|
|Indicator score|3.09|9.28 × 33 / 99, rounded to two decimal places.|

The overall application score is the sum of all indicator scores where **Use in app score calc** is selected. If all three indicators in this profile each returned a score of 3.09, the application score would be 9.27.

## Business capability score calculation

Business capability scoring uses the same indicator and profile infrastructure as application scoring. The key difference is that scores are calculated directly only for leaf capabilities \(capabilities with no children\), and parent scores are derived by roll-up.

|Aspect|Behavior|
|------|--------|
|Which capabilities are scored directly|Leaf capabilities only \(leaf\_node = true\). The indicator pipeline runs against leaf nodes the same way it runs against business applications.|
|Parent score roll-up|Each parent capability score is the arithmetic mean of its direct children's scores. Capabilities with a score of –1 \(not assessed\) are excluded from the mean.|
|Indicator-level roll-up|Individual indicator scores — such as People, Process, and Technology — are also averaged across children at each level of the hierarchy.|
|Score storage|Stored in the Application Score \[apm\_app\_score\] table, the same table as application scores. The profile uses `ci_class = cmdb_ci_business_capability`.|

## Capability heat map color thresholds

The capability heat map translates numeric scores into color-coded gap ratings. The default thresholds are as follows.

|Score range|Color|Interpretation|
|-----------|-----|--------------|
|7 to 10|Green|No gap|
|4 to less than 7|Orange|Medium gap|
|0 to less than 4|Red|Major gap|
|–1 or empty|Gray|Not assessed|

**Note:** The **No gap threshold** and **Mid gap threshold** values are configurable per widget in the Capability map widget instance \[apm\_capability\_map\_instance\] table.

**Parent Topic:**[Rationalization of business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-rationalize-business-applications.md)

**Related topics**  


[Manage indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-configure-indicators.md)

[Manage scoring profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-configure-scoring-profiles.md)

[Tech debt indicator score for application rationalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/trm-tech-debt-indicator-for-app-rat.md)

[Regenerate application indicator scores on-demand in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-regenerate-indicator-score.md)

[Regenerate capability indicator scores on-demand in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-regenerate-capability-indicator-scores-in-eaw.md)

