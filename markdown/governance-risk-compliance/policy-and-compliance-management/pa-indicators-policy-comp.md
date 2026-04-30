---
title: Monitor controls using GRC Performance Analytics Indicators
description: You can link Policy and Compliance Management content and items to Performance Analytics indicators, breakdowns, and thresholds. You can associate Performance Analytics indicators with control objectives and controls to view scorecards and trends and analyze current conditions and trends.The GRC: Performance Analytics Integration plugin provides an integration between Performance Analytics and the Risk Management and Policy and Compliance Management applications. This plugin provides more insight into organizational risk and compliance performance.You can associate Performance Analytics indicators with risk statements and policy statements to analyze trends related to the risk or policy.You can associate Performance Analytics indicators with risks and controls to analyze trends related to the entity that risk or control belongs to.You can update all the items belonging to a GRC content record so each item is individually related to the PA indicator.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Monitor controls using GRC Performance Analytics Indicators

You can link Policy and Compliance Management content and items to Performance Analytics indicators, breakdowns, and thresholds. You can associate Performance Analytics indicators with control objectives and controls to view scorecards and trends and analyze current conditions and trends.

The risks and controls associated with a PA indicator or PA indicator/breakdown/element automatically monitor any PA threshold with the same PA indicator or PA indicator, breakdown, or element relationship. Any PA threshold breach is reported at the risk or control and Performance Analytics indicators relationship level within a breach counter.

![Performance analytics integration overview.](../../grc-common/image/pa-integration.png)

## PA threshold breach impact

When a risk or control and Performance Analytics indicators relationship breach counter is different than zero \(for example, a PA threshold with the same PA indicator or PA indicator, breakdown, or element relationship has breached\), and if no opened issue exists, then an issue is created which is associated to the risk or control. Also for risks, the **Indicator failure factor** represents the number of risk and Performance Analytics indicators relationships with a breach counter different than zero.

## Reset all PA Indicator breach counters

Reset breach counters associated to a risk or control by clicking **Reset all PA Indicator breach counters** or opening the specific relationship and clicking **Reset Breach Counter**.

## GRC PA indicator breach reports

There are two reports for the reporting of breaches:

-   Risk PA Indicator Breaches
-   Control PA Indicator Breaches

**Parent Topic:**[Using the Classic user interface for Policy and Compliance tasks](using-policy-compliance-legacy-ui.md)

## Activate GRC: Performance Analytics Integration

The GRC: Performance Analytics Integration plugin provides an integration between Performance Analytics and the Risk Management and Policy and Compliance Management applications. This plugin provides more insight into organizational risk and compliance performance.

### Before you begin

Role required: admin

### About this task

This plugin includes demo data and activates related plugins if they are not already active.

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


### What to do next

After activating the GRC: Performance Analytics Integration plugin on an instance with customized related lists on content \(risk or control objective\) or items \(risk or control\), you may have to manually add the PA Indicator to content relationships and/or the PA indicator to item relationships.

**Related topics**  


[List of plugins](../../grc-common/task/activate-grc-pa-prem-integ.md)

## Associate a PA indicator with a risk statement or control objective

You can associate Performance Analytics indicators with risk statements and policy statements to analyze trends related to the risk or policy.

### Before you begin

Role required: sn\_risk.manager or sn\_compliance.manager

### Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Control objectives**.
    -   **All** &gt; **Risk** &gt; **Risk Library** &gt; **Risk Statements**.
2.  Open a risk statement or control objective.

3.  In the **PA Indicators** related list, click **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |PA Indicator|The performance analytics indicator to associate the Risk Statement or control objective with.|

5.  Click **Submit**.

    On the risk statement or control objective form, in the **PA Indicators** related list, you see the associated indicator. You can optionally click **View Indicator** on the desired indicator to see the Performance Analytics scorecard of the indicator. The PA Indicator associations are carried over to all risks or controls associated to the original risk statement or control objective. Also, if the indicator has a breakdown that matches the risk or entity of the control \(for example a Business Service breakdown\), the **Breakdown** and **Element** fields for the relationship are automatically filled in.


## Associate a PA indicator with risks and controls

You can associate Performance Analytics indicators with risks and controls to analyze trends related to the entity that risk or control belongs to.

### Before you begin

Role required: sn\_risk.manager or sn\_compliance.manager

### Procedure

1.  Navigate to one of the following locations:

    -   **Policy and Compliance** &gt; **Controls** &gt; **All Controls**.
    -   **Risk** &gt; **Risk Register** &gt; **All Risks**.
2.  Open a risk or control.

3.  In the **PA Indicators** related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_chs_jgz_pw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PA Indicator

</td><td>

Performance analytics indicator to associate the Risk or Control with.

</td></tr><tr><td>

Breakdown

</td><td>

Break down to view a specific trend based on the breakdown element.

</td></tr><tr><td>

Element

</td><td>

Break down element to view a particular trend and scorecard. **Note:** This field depends on the **Breakdown** field being populated. When visible, it is mandatory.

</td></tr></tbody>
</table>5.  Click **Submit**.

    On the Risk or Control form, in the **PA Indicators** related list, you see the associated indicator. You can optionally click **View Indicator** on the desired indicator to see the Performance Analytics scorecard of the indicator.


## Update associated GRC indicators for a set of items

You can update all the items belonging to a GRC content record so each item is individually related to the PA indicator.

### Before you begin

Role required: sn\_risk.manager or sn\_compliance.manager

### Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Control Objectives**.
    -   **All** &gt; **Risk** &gt; **Risk Library** &gt; **Risk Statements**.
2.  Open a Risk Statement or Control Objective that has an associated Performance Analytics Indicator.

3.  Click the **Update PA Relationships** related link.

    All the risks or controls related to the risk statement or policy statement are automatically associated with all the risk statement or policy indicators of the statement. Also, if the indicator has a breakdown that matches the risk or entity of the control \(for example a Business Service breakdown\), the **Breakdown** and **Element** fields for the relationship are automatically filled in.


