---
title: Use case: How indicator scores appear on the bubble chart
description: Understand how application indicator scores are calculated and displayed as bubbles on the Application Rationalization bubble chart.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-bubble-chart-use-case.html
release: australia
topic_type: concept
last_updated: "2026-04-21"
reading_time_minutes: 21
keywords: [bubble chart, indicator scores, normalized value, application rationalization, scoring profile]
breadcrumb: [Use bubble chart view, Working with application rationalization, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Use case: How indicator scores appear on the bubble chart

Understand how application indicator scores are calculated and displayed as bubbles on the Application Rationalization bubble chart.

## Scenario

Acme Corp's enterprise architecture team wants to rationalize its application portfolio using the TIME framework — a model developed by Gartner that classifies applications into four disposition categories:

-   Tolerate — keep the application running for now, but do not invest further.
-   Invest — actively develop and grow the application.
-   Migrate — move the workload to a better alternative platform or application.
-   Eliminate — retire or decommission the application.

In EA Workspace, these dispositions surface as Sustain \(Tolerate/Invest\), Migrate, and Retire \(Eliminate\) labels on the bubble chart quadrants.

Acme Corp evaluates five business applications on two dimensions:

-   **Business Value** — how much value the application delivers to the business, gathered from stakeholder surveys.
-   **Technical Risk** — how much technical risk the application carries, gathered from stakeholder surveys.

The bubble chart in EA Workspace plots these two dimensions on the X and Y axes, letting architects visually identify rationalization decisions.

**Note:** The bubble color reflects the planned disposition set for each application. The legend at the bottom of the chart shows what each color means. The bubble color settings cannot be modified.

**What is a scoring profile?**

A scoring profile \(apm\_application\_profile\) is the central configuration object that defines how business applications are evaluated. It acts as the bridge between your indicators and your applications.

**Note:** The sn\_apm\_ws.app\_indicator\_scoring\_profile system property accepts only a single sys\_id. Comma-separated values are not supported. If you enter multiple values, the bubble chart falls back to the Default Application Profile and ignores your custom profile.

## Step 1: Set up indicators

As an EA admin user, navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Setup** &gt; **Indicators** and confirm that two default indicators are active:

|Indicator|Data source|Direction|Frequency|
|---------|-----------|---------|---------|
|Business Value|Assessment|Maximize|Quarter|
|Technical Risk|Assessment|Minimize|Quarter|

**Business Value** uses *Maximize* because a higher score is better. **Technical Risk** uses *Minimize* because a higher risk score is worse — the system inverts the normalized value so that riskier applications appear lower on the chart axis.

\[Omitted image "bubblechart-indicators.png"\] Alt text: Application indicators

**Note:** No new indicators need to be created for this use case. Both are available by default in the Default Application Profile. For information on how to create custom indicators, see [Add or edit an application indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-indicator.md).

**How Minimize Direction Affects Chart Position**

For Minimize-direction indicators, the score is inverted before being plotted. A raw score of 0 \(zero risk\) results in a normalized value of 1.0, which after inversion is set to 10.0 — the highest position on the axis. A raw score at the maximum \(highest risk\) inverts to 1.0 — the lowest position. The value 10 on the Y-axis means least risky, and 1 means most risky, for a Minimize indicator.

<table id="table_j5j_d2q_cjc"><thead><tr><th>

Maximize direction \(Business Value\)

</th><th>

Minimize direction \(Technical Risk\)

</th></tr></thead><tbody><tr><td>

Higher raw score → higher normalized value → higher position on axis.

 A Business Value raw score of 85 normalizes to 10.0 — the top of the axis.

</td><td>

Higher raw score = worse condition. The system inverts the normalized value.

 A Technical Risk raw score of 90 \(most risky\) normalizes to 10.0 first, then inverts to 1.0 — the bottom of the axis

</td></tr><tr><td>

Formula: Normalized Value = \(\(\(raw - min\) / \(max - min\)\) × 9\) + 1

</td><td>

Formula: Adjusted = \(10 - Normalized Value\) + 1 ← inversion step

</td></tr><tr><td>

Raw = 0 → Normalized = 1.0 \(lowest on chart\) Raw = max → Normalized = 10.0 \(highest on chart\)

</td><td>

Raw = 0 → Normalized = 1.0 → Inverted = 10.0 \(highest on chart — zero risk is best!\) Raw = max → Normalized = 10.0 → Inverted = 1.0 \(lowest on chart — maximum risk is worst\)

</td></tr></tbody>
</table>**Indicator data sources**

This use case uses Assessments as the data source, but EA Workspace supports five data source types. The choice of data source depends on what data is available and how frequently it is updated:

|Data source|How it works|Example indicators|Best used for|
|-----------|------------|------------------|-------------|
|Assessments|Survey-based ratings collected from stakeholders via the Service Portal. Assessors rate each application on a defined scale.|Business Value, Technical Risk, and Functional Fit|This use case|
|Performance Analytics \(PA\)|Scorecard data from an existing PA indicator \(For example: incident count, change volume\). Automatically sourced — no manual surveys are needed.|Number of Incidents via Service and Number of Changes via Service|Operational health indicators|
|Custom Script|A script that returns a per-application weight. Useful for complex calculations or external data lookups.|Portfolio TCO and Overall Score|Financial and composite indicators|
|Query Condition|A configurable table query \(For example: count open vulnerabilities per app\). No code required.|Usage \(active users\)|Simple count-based indicators|
|Indicators|Aggregates scores from child indicators into a parent indicator score.|Application Operational Metrics, and Business impact|Roll-up and composite scoring|

\[Omitted image "bubblechart-indicator-data-source.png"\] Alt text: Indicator data source

**Note:** Indicators from different data source types can coexist in the same scoring profile. For example, a profile might combine an Assessments indicator \(Business Value\), a Performance Analytics indicator \(Number of Incidents\), and a Custom Script indicator \(Portfolio TCO\). Each indicator type feeds into the same normalization and scoring pipeline regardless of its data source.

Applications Not Assessed — Visibility on the chart

If a business application has not been assessed for one or both axis indicators for the selected fiscal period, it will not appear on the bubble chart. A bubble requires indicator scores for both the X-axis and Y-axis indicator for the same fiscal period.

Applications with scores for only one axis are silently excluded. This applies regardless of data source type — an application that was not included in a PA breakdown, not assessed in a survey, or not returned by a custom script will have no score record and therefore no bubble is displayed.

To identify applications that are scored on one axis but not the other:

-   Navigate to apm\_app\_indicator\_score.list
-   Filter by fiscal period = the period shown on the chart Filter by indicator = your X-axis indicator
-   Compare the configuration item list to the same filter for your Y-axis indicator

Applications missing from either list will not render a bubble.

**Note:** When an application is newly added to the portfolio after assessments have been generated, its assessment questions are not automatically included in existing assessment instances. You must regenerate assessments from the indicator's record to include new applications in the next assessment cycle.

## Step 2: Set up the scoring profile

As an admin, navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Setup** &gt; **Scoring Profiles** &gt; **Default Application Profile** and confirm that both indicators are listed in the Profile Indicators related list with the following weights:

|Indicator|Weight|
|---------|------|
|Business Value|50|
|Technical Risk|50|

Equal weights mean each indicator contributes equally to the overall application score. Verify that all five business applications have their **Application scoring profile** field set to **Default Application Profile**. For information on how to attach profile indicators to a scoring profile, see [Attach a profile indicator with an application scoring profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-attach-profile-indicators-with-application-scoring-profiles.md).\[Omitted image "bubblechart-scoring-profile.png"\] Alt text: Default scoring profile

## Step 3: Add indicators to the bubble chart table

Navigate to the Application Bubble Chart \[apm\_bubble\_chart\] table and confirm that both **Business Value** and **Technical Risk** are registered. The available X and Y axis options on the bubble chart are derived from this table. The indicator scores are gathered from the Indicator Scores \[apm\_app\_indicator\_score\] table.

\[Omitted image "bubblechart-add-ind-bctable.png"\] Alt text: Add indicators to the bubble chart table

**Note:** Only indicators registered in the Application Bubble Chart \[apm\_bubble\_chart\] table appear as axis options on the bubble chart. Adding an indicator to a scoring profile alone is not sufficient. For details on how to add X and Y axis indicators, see [Add or edit an application indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-indicator.md).

## Step 4: Stakeholders complete assessments

The EA team sends out assessment surveys. Stakeholders rate each application on Business Value and Technical Risk. After all responses are collected, the platform aggregates them per application into the following raw scores \(application weights\):

\[Omitted image "bubblechart-generate-assessments.png"\] Alt text: Generate assessments for business value

|Application|Business Value \(raw\)|Technical Risk \(raw\)|
|-----------|----------------------|----------------------|
|App A — CRM Platform|85|20|
|App B — Legacy ERP|30|90|
|App C — Analytics Suite|70|40|
|App D — HR Portal|55|60|
|App E — Internal Wiki|20|75|

\[Omitted image "bubblechart-submit-assessment.png"\] Alt text: Submit assessments through Service Portal

**Note:** Raw scores here are assessment aggregate values on a 0–100 scale. These are the *application weights* — the inputs to normalization. They are not directly plotted on the bubble chart.

## Step 5: The scoring job runs and calculates normalized values

The admin runs the **Load Application Indicators and compute Application Scores** scheduled job. The system calculates a Normalized Value for each application per indicator, scaling all values to a 1–10 range relative to each other.

\[Omitted image "bubblechart-job-status.png"\] Alt text: Execute scheduled job to compute application scores

**Verifying that the job ran successfully**

-   **System log**: Navigate to syslog.list, filter Message contains Load Application Indicators, Created = Last 30 minutes. A successful run shows two entries: \#\#\#\# Starting... and \#\#\#\# Completed execution of... &lt;elapsed&gt;ms. A missing completion entry means the job failed mid-run — add Level = Error to the filter to find the cause.
-   **Indicator scores**: Navigate to apm\_app\_indicator\_score.list, filter by Fiscal period = &lt;FY26: Q2&gt; and Configuration Item = any business application \(from this use case\). Both Business Value and Technical Risk rows must appear with a non-zero Normalized value. If rows are missing, check that all assessment instances were Complete or Canceled before regeneration ran.
-   **Progress Worker path**: If you used sn\_apm\_regenerate\_application\_scores.do instead of the scheduled job, search syslog for APM: Regenerate application scores on &lt;date&gt; — this is the log marker for the background worker path.

**Normalization formula:**

This scales raw scores, so all applications are comparable on a 1–10 range regardless of absolute values. The lowest-scoring application always maps to 1.0 and the highest to 10.0, with all others distributed proportionally between.

```
Normalized Value = (((appWeight - minWeight) / (maxWeight - minWeight)) x 9) + 1
```

For indicators with *Minimize* direction, the normalized value is then inverted so that a lower raw value \(better condition\) results in a higher chart position:

```
Adjusted Normalized Value = (10 - Normalized Value) + 1
```

**Business Value — normalized values \(direction: Maximize\)**

Min = 20 \(App E\) · Max = 85 \(App A\) · Range = 65.

|Application|Raw score|Calculation|Normalized Value|
|-----------|---------|-----------|----------------|
|App A — CRM Platform|85|\(\(\(85-20\)/65\)x9\)+1|10.00|
|App B — Legacy ERP|30|\(\(\(30-20\)/65\)x9\)+1|2.38|
|App C — Analytics Suite|70|\(\(\(70-20\)/65\)x9\)+1|7.92|
|App D — HR Portal|55|\(\(\(55-20\)/65\)x9\)+1|5.85|
|App E — Internal Wiki|20|\(\(\(20-20\)/65\)x9\)+1|1.00|

**Technical Risk — normalized values \(direction: Minimize, inverted\)**

Min = 20 \(App A\) · Max = 90 \(App B\) · Range = 70.

|Application|Raw score|Step 1: Normalize|Step 2: Invert|Final Normalized Value|
|-----------|---------|-----------------|--------------|----------------------|
|App A — CRM Platform|20|1.00|\(10-1.00\)+1|10.00|
|App B — Legacy ERP|90|10.00|\(10-10.00\)+1|1.00|
|App C — Analytics Suite|40|3.57|\(10-3.57\)+1|7.43|
|App D — HR Portal|60|6.43|\(10-6.43\)+1|4.57|
|App E — Internal Wiki|75|8.57|\(10-8.57\)+1|2.43|

**Tip:** App B has the highest raw Technical Risk score \(90\), meaning it is the riskiest application. After inversion, it receives a normalized value of 1.00 — the lowest possible — placing it at the bottom of the Y-axis on the bubble chart. This makes the visual intuitive: riskier applications appear lower.

## Step 6: Indicator scores and overall application scores are calculated

The system calculates each application's indicator score — the normalized value weighted by the indicator's share of the scoring profile — and sums them into an overall application score.

**Indicator Score formula:**

```
Indicator Score = Normalized Value x (Indicator Weight / Total Weights)
```

In this example, the weight share for each indicator is 50 / \(50 + 50\) = 0.5.

|Application|BV normalized|BV indicator score|TR normalized|TR indicator score|Overall score|
|-----------|-------------|------------------|-------------|------------------|-------------|
|App A — CRM Platform|10.00|5.00|10.00|5.00|10.00|
|App C — Analytics Suite|7.92|3.96|7.43|3.72|7.68|
|App D — HR Portal|5.85|2.93|4.57|2.29|5.22|
|App E — Internal Wiki|1.00|0.50|2.43|1.22|1.72|
|App B — Legacy ERP|2.38|1.19|1.00|0.50|1.69|

These values are stored across two separate tables:

-   **Indicator Score** \[apm\_app\_indicator\_score\] — holds the per-indicator, per-application, per-fiscal-period score records. The Normalized Value in this table is what the X and Y axes on the bubble chart read directly.
-   **Overall Application Score** \[apm\_app\_score\] — holds the aggregate score per application per fiscal period, calculated by summing all Indicator Scores. This is visible in the **List** view of Application Rationalization and is used as the Bubble Size when the **Overall Score** option is selected in the chart settings.

**Note:** The X and Y axis positions on the bubble chart are read from Indicator Score \[apm\_app\_indicator\_score\] table. The overall score only affects bubble size.

## Verify the business application default filter

Before a scored business application can appear on the bubble chart, verify the business application default filter. This filter is an encoded query stored in the **sn\_apm\_ws.business\_application\_default\_filter** system property.

The default value is:

```
install_status!=2@install_status!=2000@life_cycle_stage!=End of Life@life_cycle_stage!=EMPTY
```

This means the chart excludes any business application that is in *Retired* or *Decommissioned* install status, or whose lifecycle stage is *End of Life* or empty. In this scenario, all five Acme Corp applications have an active install status and a current lifecycle stage, so all five pass the filter and are eligible to appear as bubbles.

**Important:** If your organization has customized this property — for example, by adding a company scope filter such as company.sys\_id=YOURCOMPANYID — any scored application that does not match the custom filter will be silently excluded from the chart, even if it has valid indicator scores for both axes. This is one of the most common causes of missing bubbles. To verify, apply the encoded query on the Business Applications \[cmdb\_ci\_business\_app.list\] table and confirm your scored applications appear in the results.

## The data pipeline

The bubble chart rendering depends on the following data chain. Verify that the following components are aligned for the chart to render data.

|Link|Component|What it does|Where to check|
|----|---------|------------|--------------|
|1|Scoring profile property|Determines which scoring profile the bubble chart queries against.|System Property: **sn\_apm\_ws.app\_indicator\_scoring\_profile**|
|2|Profile indicator configuration|Maps indicators to the scoring profile with weights and configuration.|Table: Profile indicator \[apm\_application\_profile\_indicator\]|
|3|Bubble chart configuration|Maps specific indicators to the X, Y, and Z \(bubble size\) axes of the chart.|Table: Application Bubble Chart \[apm\_bubble\_chart\]|
|4|Indicator score data|Actual score records for business applications, per indicator, per fiscal period.|Table: Indicator Score \[apm\_app\_indicator\_score\]|
|5|Business application default filter|Controls which business applications are visible in application rationalization.|System Property: **sn\_apm\_ws.business\_application\_default\_filter**|

## Step 7: Reading the bubble chart

Before interpreting the chart, check the following details.

|\#|What to check|What good looks like|
|---|-------------|--------------------|
|1|Correct scoring profile configured? \[**sn\_apm\_ws.app\_indicator\_scoring\_profile**\]|Contains the sys\_id of the profile under which indicator scores were created. If blank, the system uses the Default Application Profile. Only one sys\_id is accepted — comma-separated values are not supported.|
|2|Indicators mapped to that profile? \[apm\_application\_profile\_indicator\]|At least two indicators \(for the X and Y axes\) are listed in the Profile Indicators related list with non-zero weights.|
|3|Bubble chart configuration set up? \[apm\_bubble\_chart\]|An active record exists whose X and Y Indicator fields reference indicators that are also listed in the scoring profile from check 2.|
|4|Indicator scores exist for the selected fiscal period? \[apm\_app\_indicator\_score\]|Records exist for business applications, for the fiscal period selected in the chart UI, under the same scoring profile. Both X and Y axis indicators must have scores — a bubble only renders if both axes have data for the same fiscal period.|
|5|Scored apps pass the default filter? \(**sn\_apm\_ws.business\_application\_default\_filter**\)|The business applications with indicator scores are not excluded by the encoded query. Verify by applying the filter on `cmdb_ci_business_app.list` and confirming the scored apps appear.|

Role required: sn\_apm.apm\_analyst.

The EA architect navigates to **Workspaces** &gt; **Enterprise Architecture Workspace**, opens the Application Rationalization page by selecting the application rationalization icon \(\[Omitted image "icon-app-rationalization.png"\] Alt text:\), and then selects **Bubble chart**.

The architect selects the settings icon \(\[Omitted image "icon-bubblechart-settings.png"\] Alt text:\) to configure the chart and selects **Apply**:

-   **X-axis:** Technical Risk
-   **Y-axis:** Business Value
-   **Bubble size:** Overall Application Score
-   **Bubble labels:** Toggle enabled, to display business application names on the chart.

**Note:** The bubble chart plots the **Normalized Value** \(1–10 scale\) on each axis — not the raw assessment score and not the weighted indicator score. The axis scale is fixed at 0–10. For a bubble to appear on the chart, indicator scores for the selected fiscal period must be available for both the X-axis and Y-axis indicators.

After selecting **Apply**, business application bubbles are displayed on the chart. Each application appears at the intersection of its normalized values for the two chosen indicators:

\[Omitted image "bubblechart-final-output.png"\] Alt text: Bubble chart output

|Application|X \(TR norm\)|Y \(BV norm\)|Quadrant|Implication|
|-----------|-------------|-------------|--------|-----------|
|App A — CRM Platform|1.00|10.00|Sustain|High value, low risk — maintain and monitor|
|App C — Analytics Suite|3.57|7.92|Sustain|Strong value, manageable risk — keep steady|
|App D — HR Portal|6.14|5.85|Invest|Moderate value, elevated risk — invest to reduce risk|
|App E — Internal Wiki|8.17|1.00|Migrate|Low value, high risk — migrate or replace|
|App B — Legacy ERP|10.00|2.38|Migrate|Low value, very high risk — urgent action needed|

**Note:** Business application bubbles whose X and Y axis values are within the value range of +/-0.25 of each other are grouped. A grouped bubble displays the total number of business application bubbles it contains. On selecting a grouped bubble, the info pane appears, displaying the list of individual business applications that are part of the grouped bubble.

**Note:** The bubble chart displays up to 500 bubbles by default. If you have more than 500 assessed business applications, configure the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property to increase this limit. For details, see [Change the number of bubbles displayed on the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-sys-prop-change-number-of-bubbles.md).

You can also generate insights into business applications using Now Assist. For information, see [Generate insights into business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/generate-insights-into-ba.md).

## Step 8: Taking action from the bubble chart

The architect identifies App B \(Legacy ERP\) in the Migrate quadrant. Its Business Value normalized score \(2.38\) and Technical Risk normalized score \(1.00\) indicate low value and very high risk, making it a priority for retirement. The architect takes the following actions directly from the bubble chart.

**Set planned disposition**

The architect selects the bubble for App B and performs the following, depending on the bubble type:

<table id="table_xkh_yxr_z3c"><thead><tr><th>

Bubble type

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Single bubble

</td><td>

1.  Select the bubble for App B.
2.  In the pop-up window, select the context menu icon \(\[Omitted image "eaw-icon-menu.png"\] Alt text:\) and select **Set planned disposition**.
3.  In the Set planned disposition window, select **Migrate** from the **Planned disposition** list, enter a **Planned disposition date**, and add the justification in the **Reasoning** field.
4.  Select **Update**.

</td></tr><tr><td>

Grouped bubble

</td><td>

1.  Select the grouped bubble. The info pane appears, displaying the list of individual business applications within the group.
2.  Select the context menu icon \(\[Omitted image "eaw-icon-menu.png"\] Alt text:\) next to App B and select **Set planned disposition**.
3.  In the Set planned disposition window, select **Migrate** from the **Planned disposition** list, enter a **Planned disposition date**, and add the justification in the **Reasoning** field.
4.  Select **Update**.

</td></tr></tbody>
</table>\[Omitted image "bubblechart-set-plan-disposition.png"\] Alt text: Set planned disposition

**Create a demand**

The architect also creates a demand for the retirement initiative directly from the bubble chart:

<table id="table_clh_yxr_z3c"><thead><tr><th>

Bubble type

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Single bubble

</td><td>

1.  Select the bubble for App B.
2.  In the pop-up window, select the context menu icon \(\[Omitted image "eaw-icon-menu.png"\] Alt text:\) and select **Create demand**.
3.  On the Create demand form, fill in the fields and select **Create**. For a description of the field values, see [Create demand form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-demand-form.md).

</td></tr><tr><td>

Grouped bubble

</td><td>

1.  Select the grouped bubble. The info pane appears.
2.  Select the context menu icon \(\[Omitted image "eaw-icon-menu.png"\] Alt text:\) next to App B and select **Create demand**.
3.  On the Create demand form, fill in the fields and select **Create**. For a description of the field values, see [Create demand form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-demand-form.md).

</td></tr></tbody>
</table>\[Omitted image "bubblechart-create-demand.png"\] Alt text: Create demand from the bubble chart page

The architect also notes that App E \(Internal Wiki\) sits in the Migrate quadrant but has a slightly higher Technical Risk normalized value \(2.43\) compared to App B. Before setting a disposition, the architect selects the App E bubble to open the side panel, then selects **Full details** to review the full business application record without leaving the bubble chart. For more details, see [Edit business application details in bubble chart view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-edit-ba-details-in-bubble-chart.md).

## Summary: the full flow at a glance

The following sequence summarizes how a raw assessment score is set to a bubble position on the chart:

1.  **Stakeholder assessments** produce a raw score per application \(the application weight\).
2.  **The scoring job** normalizes raw scores to a 1–10 scale relative to all other applications in the set \(Normalized Value\). For *Minimize*-direction indicators, the value is inverted so that a lower raw score results in a higher chart position.
3.  **Weights are applied** to each normalized value \(Normalized Value x weight share = Indicator Score\).
4.  **Indicator Scores are summed** to produce the Overall Application Score.
5.  **Scores are stored** in two tables: Indicator Scores \[apm\_app\_indicator\_score\] table \(per-indicator scores — drives axis positions\) and Overall Application Score \[apm\_app\_score\] table \(overall aggregate score — drives bubble size when Overall Score is selected\).
6.  **The default application filter** \(**sn\_apm\_ws.business\_application\_default\_filter**\) is applied. Only applications that pass this encoded query filter are eligible to appear as bubbles.
7.  **The bubble chart plots the Normalized Value** on the X and Y axes. The axis scale is fixed at 0–10. Bubble color reflects the planned disposition value set for each application.

## Key behaviors this example illustrates

**Position is relative, not absolute.** An application's bubble position depends on how it compares to all other applications in the evaluated set — not on its raw score alone. If you add or remove applications from the portfolio, the normalized values recalculate and bubbles shift.

**The chart plots normalized values.** Even though the scoring profile uses weighted indicator scores to calculate the overall application score, the X and Y axes show the normalized value \(1–10\). Changing indicator weights does not move bubbles left or right — it only changes the overall score, which controls bubble size when configured that way.

**Minimize-direction indicators are inverted on the chart.** Technical Risk is set to Minimize. Because Technical Risk is on the X-axis, a riskier application appears further right. The Invest quadrant \(top-right\) represents applications with high business value but elevated technical risk — applications worth investing in to reduce that risk.

**Fiscal period alignment is critical.** If the indicators are set to *Quarter* frequency and the fiscal period filter on the chart is set to a month, no data appears. The period filter must match the indicator frequency.

**Bubble size adds a third dimension.** Configuring an indicator or the overall score as the Bubble Size lets you compare a third metric visually without adding another axis — for example, using Portfolio TCO as the bubble size shows cost alongside value and risk.

**Closely scored applications are grouped.** Bubbles whose X and Y axis values are within +/-0.25 of each other are combined into a single grouped bubble showing a count. Select a grouped bubble to open the info pane and see the individual applications inside.

**Parent Topic:**[Use bubble chart view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-using-app-rat-bubble-chart-view.md)

**Related topics**  


[Use bubble chart view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-using-app-rat-bubble-chart-view.md)

[Analyze applications using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-analyze-applications-by-capability.md)

[Create a demand using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-a-demand-using-the-bubble-chart.md)

[Set the planned disposition of a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-set-planned-disposition-of-a-business-application.md)

[Add business application lifecycle data using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-business-application-lifecycle-data.md)

[Edit business application details in bubble chart view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-edit-ba-details-in-bubble-chart.md)

[Change the number of bubbles displayed on the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-sys-prop-change-number-of-bubbles.md)

