---
title: Create an indicator definition
description: You can create a new KPI Composer indicator definition directly from the relevant artifact in the Data Definition tab. Fill the indicator definition with the necessary information for creating a Performance Analytics indicator.After you create an indicator definition in KPI Composer, you can add contributing indicators to that definition. Formula indicator definitions, where the formula includes one or more other indicators, require contributing indicators to be complete.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Design your indicator solution, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create an indicator definition

You can create a new KPI Composer indicator definition directly from the relevant artifact in the Data Definition tab. Fill the indicator definition with the necessary information for creating a Performance Analytics indicator.

## Before you begin

You have an existing [KPI Composer project](../concept/kpi-composer-projects.md) with a complete draft of the [KPI tree](../concept/design-kpi-tree.md#) in the Analytics tab. You also need technical knowledge of Performance Analytics indicators.

Role required: sn\_kpi\_composer.admin or admin to link to a Performance Analytics indicator, sn\_kpi\_composer.user for other functionality. No roles are required for responsible users or users with edit access, except to link to a Performance Analytics indicator.

## About this task

You can create an indicator definition for every artifact in your project, whether or not it is associated with a Performance Analytics widget. You cannot add more than one indicator definition for an artifact. However, if you link an artifact to a formula indicator, you automatically link it to all the [contributing indicators](../concept/performance-analytics-glossary.md#) in the formula.

## Procedure

1.  Navigate to **All** &gt; **KPI Composer** and open the relevant project.

2.  Navigate to the Data Definition tab.

3.  Locate an artifact, probably a Measurement, that you want to define an indicator for.

    **Tip:** Before you continue to create an indicator definition, check whether any suitable indicator definitions already exist. Click the artifact to open its properties. Then browse the list of available indicator definitions.

    ![Properties of a measurement artifact in the data definition tab](../image/kpi-composer-data-def-measurement-props.png)

4.  Select the plus sign, +.

5.  In the **PA Indicator** field, you can search the existing Performance Analytics indicators on this instance to see if any match this indicator definition.

    If you select a Performance Analytics indicator, its properties appear read-only in the "Linked PA indicator details" column. This information is there to help you base the indicator definition on the linked indicator.

    **Note:** Requires the sn\_kpi\_composer.admin or admin role.

    You can only search the indicators by name.

    A link icon appears in artifacts next to the name of an indicator definition that is linked to a Performance Analytics indicator.

    ![Critical success factor artifact in Data Definition tab, showing indicator definitions linked to PA indicators](../image/kpi-comp-element-linked-indicators.png)

6.  Fill in the **Development instructions** field with any information for your developers that is not in the rest of the form.

    The information in **Development instructions** is for your internal developers use only. You can also provide details about the indicator in the **Description** field. The information in the **Description** field should be replicated in the **Description** field of the resulting Performance Analytics indicator.

7.  Decide on the **Direction** of the indicator.

    |Value|Use case|
    |-----|--------|
    |**Maximize**|Select if an increase in this indicator score is desired. For example, consider selecting **Maximize** for an indicator that shows revenue. Analytic tools and graphic elements reflect that an increase in this indicator score is good and a decrease is bad.|
    |**Minimize**|Select if a decrease in this indicator score is desired. For example, consider selecting **Minimize** for an indicator that shows costs. Analytic tools and graphic elements reflect that a decrease in this indicator score is good and an increase is bad.|
    |**None**|Select if the direction of change in this score doesn’t matter to your business.|

8.  Decide whether an Automated, Formula, or Manual indicator best represents the information in the artifact.

<table id="choicetable_tkh_r5y_4jb"><thead><tr><th align="left" id="d169508e276">

Indicator Type

</th><th align="left" id="d169508e279">

Description

</th></tr></thead><tbody><tr><td id="d169508e285">

**Automated**

</td><td>

An automated indicator uses an indicator source as its data set. The indicator source specifies a table or database view, conditions for filtering records from that source, and the frequency at which you expect to display the data. The indicator applies an aggregator and optional conditions to this data.

</td></tr><tr><td id="d169508e297">

**Formula**

</td><td>

Calculate scores from the scores of one or more other indicators. Apply mathematical operations or a preset method, such as the method to calculate the gap between an indicator score and the indicator target.

</td></tr><tr><td id="d169508e309">

**Manual**

</td><td>

Manual indicators are not associated with an indicator source. Scores for manual indicators are not generated automatically by a data collection job. Instead, populate these indicators by adding scores to the scoresheet manually.

 Manual indicators are typically used for data that cannot be retrieved from the ServiceNow instance because it comes from an outside system, such as customer data from a third-party sales system.

</td></tr></tbody>
</table>9.  Fill in any remaining fields.

    -   If you are defining a Manual indicator, you do not have to add any more information.
    -   If you are defining a Formula indicator, clearly describe to a Performance Analytics administrator how to build the formula. You do not have to use actual formula indicator JavaScript syntax.
    -   If you are defining an Automated indicator, include the following information:

        |Field|Description|
        |-----|-----------|
        |Aggregation|The aggregate function to apply to the data from the indicator source.|
        |Frequency|Expected periodicity for collecting data. Usually the indicator Frequency matches the indicator source Valid for frequency value.|
        |Facts table|The table that the indicator source references.|
        |Condition|Textual description of the conditions for filtering records from the facts table. You do not have to use condition builder syntax.|

10. Either click **Submit**, or, if you want to define supporting indicators, open the context menu and click **Save**.


## Creating an indicator definition

In the following short animation, the user defines a formula indicator for the measurement "% of major incident first call resolution." The indicator is based on an existing PA indicator that calculates a similar percentage but does not filter on Priority.

![Creating an indicator definition for a measurement](../image/kpi-comp-create-indicator-def.gif)

**Parent Topic:**[Design your Performance Analytics solution with KPI Composer](../concept/designing-pa-solution.md)

**Related topics**  


[Automated indicators](../concept/automated-indicators.md)

[Indicator sources](../concept/c_IndicatorSources.md#)

[Formula indicators](../concept/formula-indicators.md)

[Manual indicators](t_CreateAManualIndicator.md)

## Add contributing indicators

After you create an indicator definition in KPI Composer, you can add contributing indicators to that definition. Formula indicator definitions, where the formula includes one or more other indicators, require contributing indicators to be complete.

### Before you begin

You have an existing KPI Composer project with a complete draft of the KPI tree in the Analytics tab. This project has at least one indicator definition that requires references to other indicators.

You need technical knowledge of Performance Analytics indicators.

Role required: Same as creating an indicator definition

### Procedure

1.  In the relevant artifact on the Data Definition tab, click the indicator definition name to open the indicator definition.

    ![Measurement artifact with the indicator definition highlighted](../image/kpi-comp-open-indic-def.png)

2.  In the Supporting Indicator Definitions related list, click one of the following buttons:

    -   Click **New** to create a new indicator definition. Follow the same procedure as in [Create an indicator definition](create-indicator-definition.md#).
    -   Click **Edit** to open a list of existing indicator definitions in this project. You can select as many indicators as you need.
    Search the existing indicator definitions before you create new ones, so as not to duplicate indicators.


### Result

After saving the changes, the artifact in the Data Definition tab shows the [contributing indicator](../concept/performance-analytics-glossary.md#) definitions under the main indicator definition, with a darker background.

### Adding a contributing indicator

In this example, the contributing indicator Number of resolved incidents is added to the % of major incident first call resolution artifact. This indicator matches an existing indicator definition.

![Animated gif showing a contributing indicator being added to an artifact](../image/kpi-comp-contrib-indicators.gif)

