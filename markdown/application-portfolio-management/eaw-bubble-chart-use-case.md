---
title: Use case: How indicator scores appear on the bubble chart
description: Understand how application indicator scores are calculated and displayed as bubbles on the Application Rationalization bubble chart.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-21"
reading_time_minutes: 16
keywords: [bubble chart, indicator scores, normalized value, application rationalization, scoring profile]
breadcrumb: [Use bubble chart view, Working with application rationalization, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Use case: How indicator scores appear on the bubble chart

Understand how application indicator scores are calculated and displayed as bubbles on the Application Rationalization bubble chart.

## Scenario

Acme Corp's enterprise architecture team wants to rationalize its application portfolio. They want to evaluate five business applications on two dimensions:

-   **Business Value** — how much value the application delivers to the business, gathered from stakeholder surveys.
-   **Technical Risk** — how much technical risk the application carries, gathered from stakeholder surveys.

Use the Application Rationalization bubble chart in the EA Workspace to visually identify which applications to invest in, sustain, migrate, or retire. The color of each bubble reflects the planned disposition set for that application. Refer to the legend on the bubble chart to see the significance of each color.

**Note:** The bubble color settings cannot be modified.

## The data pipeline

The bubble chart rendering depends on the following data chain. Verify the following that must be aligned for the chart to render data.

|Link|Component|What it does|Where to check|
|----|---------|------------|--------------|
|1|Scoring profile property|Determines which scoring profile the bubble chart queries against.|System Property: **sn\_apm\_ws.app\_indicator\_scoring\_profile**|
|2|Profile indicator configuration|Maps indicators to the scoring profile with weights and configuration.|Table: `apm_application_profile_indicator`|
|3|Bubble chart configuration|Maps specific indicators to the X, Y, and Z \(bubble size\) axes of the chart.|Table: `apm_bubble_chart`|
|4|Indicator score data|Actual score records for business applications, per indicator, per fiscal period.|Table: `apm_app_indicator_score`|
|5|Business application default filter|Controls which business applications are visible in application rationalization.|System Property: **sn\_apm\_ws.business\_application\_default\_filter**|

## Step 1: Set up indicators

As an EA admin user, navigates to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Setup** &gt; **Indicators** and confirms that two default indicators are active:

|Indicator|Data source|Direction|Frequency|
|---------|-----------|---------|---------|
|Business Value|Assessment|Maximize|Quarter|
|Technical Risk|Assessment|Minimize|Quarter|

**Business Value** uses *Maximize* because a higher score is better. **Technical Risk** uses *Minimize* because a higher risk score is worse — the system inverts the normalized value so that riskier applications appear lower on the Y-axis.

**Note:** No new indicators need to be created for this use case. Both are available by default in the Default Application Profile. For information on how to create custom indicators, see [Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md).

## Step 2: Set up the scoring profile

As an admin, navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Setup** &gt; **Scoring Profiles** &gt; **Default Application Profile** and confirms that both indicators are listed in the Profile Indicators related list with the following weights:

|Indicator|Weight|
|---------|------|
|Business Value|50|
|Technical Risk|50|

Equal weights mean each indicator contributes equally to the overall application score. Verify that all five business applications have their **Application scoring profile** field set to **Default Application Profile**. For information on how to attach profile indicators to a scoring profile, see [Attach a profile indicator with an application scoring profile](../../task/eaw-task/eaw-attach-profile-indicators-with-application-scoring-profiles.md).

**Important:** The **sn\_apm\_ws.app\_indicator\_scoring\_profile** system property accepts only a single sys\_id. Comma-separated values are not supported. If you enter multiple values, the bubble chart falls back to the Default Application Profile and ignores your custom profile.

## Step 3: Add indicators to the bubble chart table

Navigate to the Application Bubble Chart \(`apm_bubble_chart`\) table and confirm that both **Business Value** and **Technical Risk** are registered. The available X and Y axis options on the bubble chart are derived from this table. The indicator scores are gathered from the Indicator Scores \(`apm_app_indicator_score`\) table.

**Note:** Only indicators registered in the `apm_bubble_chart` table appear as axis options on the bubble chart. Adding an indicator to a scoring profile alone is not sufficient. For details on how to add X and Y axis indicators, see [Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md).

## Step 4: Stakeholders complete assessments

The EA team sends out assessment surveys. Stakeholders rate each application on Business Value and Technical Risk. After all responses are collected, the platform aggregates them per application into the following raw scores \(application weights\):

|Application|Business Value \(raw\)|Technical Risk \(raw\)|
|-----------|----------------------|----------------------|
|App A — CRM Platform|85|20|
|App B — Legacy ERP|30|90|
|App C — Analytics Suite|70|40|
|App D — HR Portal|55|60|
|App E — Internal Wiki|20|75|

**Note:** Raw scores here are assessment aggregate values on a 0–100 scale. These are the *application weights* — the inputs to normalization. They are not directly plotted on the bubble chart.

## Step 5: The scoring job runs and calculates normalized values

The admin runs the **Load Application Indicators and compute Application Scores** scheduled job. The system calculates a Normalized Value for each application per indicator, scaling all values to a 1–10 range relative to each other.

**Normalization formula:**

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

-   **Indicator Score** \(`apm_app_indicator_score`\) — holds the per-indicator, per-application, per-fiscal-period score records. The Normalized Value in this table is what the X and Y axes on the bubble chart read directly.
-   **Overall Application Score** \(`apm_app_score`\) — holds the aggregate score per application per fiscal period, calculated by summing all Indicator Scores. This is visible in the **List** view of Application Rationalization and is used as the Bubble Size when the **Overall Score** option is selected in the chart settings.

**Note:** The X and Y axis positions on the bubble chart are read from `apm_app_indicator_score`. The overall score only affects bubble size.

## Verify the business application default filter

Before a scored business application can appear on the bubble chart, verify the business application default filter. This filter is an encoded query stored in the **sn\_apm\_ws.business\_application\_default\_filter** system property.

The default value is:

```
install_status!=2@install_status!=2000@life_cycle_stage!=End of Life@life_cycle_stage!=EMPTY
```

This means the chart excludes any business application that is in *Retired* or *Decommissioned* install status, or whose lifecycle stage is *End of Life* or empty. In this scenario, all five Acme Corp applications have an active install status and a current lifecycle stage, so all five pass the filter and are eligible to appear as bubbles.

**Important:** If your organization has customized this property — for example, by adding a company scope filter such as `company.sys_id=YOURCOMPANYID` — any scored application that does not match the custom filter will be silently excluded from the chart, even if it has valid indicator scores for both axes. This is one of the most common causes of missing bubbles. To verify, apply the encoded query on the `cmdb_ci_business_app.list` table and confirm your scored applications appear in the results.

## Step 7: Reading the bubble chart

Before interpreting the chart, check the following details.

|\#|What to check|What good looks like|
|---|-------------|--------------------|
|1|Correct scoring profile configured? \(**sn\_apm\_ws.app\_indicator\_scoring\_profile**\)|Contains the sys\_id of the profile under which indicator scores were created. If blank, the system uses the Default Application Profile. Only one sys\_id is accepted — comma-separated values are not supported.|
|2|Indicators mapped to that profile? \(`apm_application_profile_indicator`\)|At least two indicators \(for the X and Y axes\) are listed in the Profile Indicators related list with non-zero weights.|
|3|Bubble chart configuration set up? \(`apm_bubble_chart`\)|An active record exists whose X and Y Indicator fields reference indicators that are also listed in the scoring profile from check 2.|
|4|Indicator scores exist for the selected fiscal period? \(`apm_app_indicator_score`\)|Records exist for business applications, for the fiscal period selected in the chart UI, under the same scoring profile. Both X and Y axis indicators must have scores — a bubble only renders if both axes have data for the same fiscal period.|
|5|Scored apps pass the default filter? \(**sn\_apm\_ws.business\_application\_default\_filter**\)|The business applications with indicator scores are not excluded by the encoded query. Verify by applying the filter on `cmdb_ci_business_app.list` and confirming the scored apps appear.|

Role required: `sn_apm.apm_analyst`.

The EA architect navigates to **Workspaces** &gt; **Enterprise Architecture Workspace**, opens the Application Rationalization page by selecting the application rationalization icon \(![Application rationalization icon.](../../image/eaw-image/icon-app-rationalization.png)\), and then selects **Bubble chart**.

The architect selects the settings icon \(![Settings icon.](../../image/eaw-image/icon-bubblechart-settings.png)\) to configure the chart and selects **Apply**:

-   **X-axis:** Business Value
-   **Y-axis:** Technical Risk
-   **Bubble size:** Overall Application Score
-   **Bubble labels:** Toggle enabled, to display business application names on the chart.

**Note:** The bubble chart plots the **Normalized Value** \(1–10 scale\) on each axis — not the raw assessment score and not the weighted indicator score. The axis scale is fixed at 0–10. For a bubble to appear on the chart, indicator scores for the selected fiscal period must be available for both the X-axis and Y-axis indicators.

After selecting **Apply**, business application bubbles are displayed on the chart. Each application appears at the intersection of its normalized values for the two chosen indicators:

|Application|X \(BV norm\)|Y \(TR norm\)|Quadrant|Implication|
|-----------|-------------|-------------|--------|-----------|
|App A — CRM Platform|10.00|10.00|Invest|High value, low risk — continue investing|
|App C — Analytics Suite|7.92|7.43|Invest|Strong on both — growing asset|
|App D — HR Portal|5.85|4.57|Sustain|Moderate on both — maintain as-is|
|App E — Internal Wiki|1.00|2.43|Retire|Low value, high risk — rationalize|
|App B — Legacy ERP|2.38|1.00|Retire|Low value, very high risk — urgent action needed|

**Note:** Business application bubbles whose X and Y axis values are within the value range of +/-0.25 of each other are grouped. A grouped bubble displays the total number of business application bubbles it contains. On selecting a grouped bubble, the info pane appears, displaying the list of individual business applications that are part of the grouped bubble.

**Note:** The bubble chart displays up to 500 bubbles by default. If you have more than 500 assessed business applications, configure the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property to increase this limit. For details, see [Change the number of bubbles displayed on the bubble chart](../../task/eaw-task/eaw-update-sys-prop-change-number-of-bubbles.md).

You can also generate insights into business applications using Now Assist. For information, see [Generate insights into business applications](../../../now-assist-ea/task/generate-insights-into-ba.md).

## Step 8: Taking action from the bubble chart

The architect identifies App B \(Legacy ERP\) in the Retire quadrant. Its Business Value normalized score \(2.38\) and Technical Risk normalized score \(1.00\) indicate low value and very high risk, making it a priority for retirement. The architect takes the following actions directly from the bubble chart.

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
2.  In the pop-up window, select the context menu icon \(![Context menu icon.](../../image/eaw-image/eaw-icon-menu.png)\) and select **Set planned disposition**.
3.  In the Set planned disposition window, select **Retire** from the **Planned disposition** list, enter a **Planned disposition date**, and add the justification in the **Reasoning** field.
4.  Select **Update**.

</td></tr><tr><td>

Grouped bubble

</td><td>

1.  Select the grouped bubble. The info pane appears, displaying the list of individual business applications within the group.
2.  Select the context menu icon \(![Context menu icon.](../../image/eaw-image/eaw-icon-menu.png)\) next to App B and select **Set planned disposition**.
3.  In the Set planned disposition window, select **Retire** from the **Planned disposition** list, enter a **Planned disposition date**, and add the justification in the **Reasoning** field.
4.  Select **Update**.

</td></tr></tbody>
</table>**Create a demand**

The architect also creates a demand for the retirement initiative directly from the bubble chart:

<table id="table_clh_yxr_z3c"><thead><tr><th>

Bubble type

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Single bubble

</td><td>

1.  Select the bubble for App B.
2.  In the pop-up window, select the context menu icon \(![Context menu icon.](../../image/eaw-image/eaw-icon-menu.png)\) and select **Create demand**.
3.  On the Create demand form, fill in the fields and select **Create**. For a description of the field values, see [Create demand form](../../reference/eaw-reference/eaw-demand-form.md).

</td></tr><tr><td>

Grouped bubble

</td><td>

1.  Select the grouped bubble. The info pane appears.
2.  Select the context menu icon \(![Context menu icon.](../../image/eaw-image/eaw-icon-menu.png)\) next to App B and select **Create demand**.
3.  On the Create demand form, fill in the fields and select **Create**. For a description of the field values, see [Create demand form](../../reference/eaw-reference/eaw-demand-form.md).

</td></tr></tbody>
</table>The architect also notes that App E \(Internal Wiki\) sits in the Retire quadrant but has a slightly higher Technical Risk normalized value \(2.43\) compared to App B. Before setting a disposition, the architect selects the App E bubble to open the side panel, then selects **Full details** to review the full business application record without leaving the bubble chart. For more details, see [Edit business application details in bubble chart view](../../task/eaw-task/eaw-edit-ba-details-in-bubble-chart.md).

## Summary: the full flow at a glance

The following sequence summarizes how a raw assessment score is set to a bubble position on the chart:

1.  **Stakeholder assessments** produce a raw score per application \(the application weight\).
2.  **The scoring job** normalizes raw scores to a 1–10 scale relative to all other applications in the set \(Normalized Value\). For *Minimize*-direction indicators, the value is inverted so that a lower raw score results in a higher chart position.
3.  **Weights are applied** to each normalized value \(Normalized Value x weight share = Indicator Score\).
4.  **Indicator Scores are summed** to produce the Overall Application Score.
5.  **Scores are stored** in two tables: `apm_app_indicator_score` \(per-indicator scores — drives axis positions\) and `apm_app_score` \(overall aggregate score — drives bubble size when Overall Score is selected\).
6.  **The default application filter** \(**sn\_apm\_ws.business\_application\_default\_filter**\) is applied. Only applications that pass this encoded query filter are eligible to appear as bubbles.
7.  **The bubble chart plots the Normalized Value** on the X and Y axes. The axis scale is fixed at 0–10. Bubble color reflects the planned disposition value set for each application.

## Key behaviors this example illustrates

**Position is relative, not absolute.** An application's bubble position depends on how it compares to all other applications in the evaluated set — not on its raw score alone. If you add or remove applications from the portfolio, the normalized values recalculate and bubbles shift.

**The chart plots normalized values.** Even though the scoring profile uses weighted indicator scores to calculate the overall application score, the X and Y axes show the normalized value \(1–10\). Changing indicator weights does not move bubbles left or right — it only changes the overall score, which controls bubble size when configured that way.

**Minimize-direction indicators are inverted on the chart.** Technical Risk is set to Minimize, so a riskier application appears lower on the Y-axis. This makes the Invest quadrant \(top-right\) intuitively represent applications that are both valuable and low-risk.

**Fiscal period alignment is critical.** If the indicators are set to *Quarter* frequency and the fiscal period filter on the chart is set to a month, no data appears. The period filter must match the indicator frequency.

**Bubble size adds a third dimension.** Configuring an indicator or the overall score as the Bubble Size lets you compare a third metric visually without adding another axis — for example, using Portfolio TCO as the bubble size shows cost alongside value and risk.

**Closely scored applications are grouped.** Bubbles whose X and Y axis values are within +/-0.25 of each other are combined into a single grouped bubble showing a count. Select a grouped bubble to open the info pane and see the individual applications inside.

**Parent Topic:**[Use bubble chart view](eaw-using-app-rat-bubble-chart-view.md)

**Related topics**  


[Use bubble chart view](eaw-using-app-rat-bubble-chart-view.md)

[Analyze applications using the bubble chart](../../task/eaw-task/eaw-analyze-applications-by-capability.md)

[Create a demand using the bubble chart](../../task/eaw-task/eaw-create-a-demand-using-the-bubble-chart.md)

[Set the planned disposition of a business application](../../task/eaw-task/eaw-set-planned-disposition-of-a-business-application.md)

[Add business application lifecycle data using the bubble chart](../../task/eaw-task/eaw-add-business-application-lifecycle-data.md)

[Edit business application details in bubble chart view](../../task/eaw-task/eaw-edit-ba-details-in-bubble-chart.md)

[Change the number of bubbles displayed on the bubble chart](../../task/eaw-task/eaw-update-sys-prop-change-number-of-bubbles.md)

