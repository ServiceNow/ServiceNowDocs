---
title: Compare financial baselines of a demand
description: You can compare baselines to review the variances in the financial data of a demand and see what changed.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a baseline of a demand, Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Compare financial baselines of a demand

You can compare baselines to review the variances in the financial data of a demand and see what changed.

## Before you begin

Role required: it\_demand\_manager

## About this task

You can [create](create-demand-baseline.md) multiple baselines at various stages of a demand's life cycle. For example, at the end of each phase or after every calendar month or quarter. Each baseline captures the financial data of the demand at a particular moment, providing a basis from which you can identify and review the changes made to the demand. Having multiple baselines and comparing them helps you track the performance of your demand.

If you’re creating demand with the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin activated and Demand Currency view enabled, you can view and compare the financial details of the demand in baselines in the demand currency. For more information about the fields that are available only in the Demand Currency view, see [Multicurrency in Demand Management](../concept/multicurrency-demand.md).

## Procedure

1.  To compare financial baselines of a demand, perform one of the following options.

<table id="choicetable_ydr_q2x_xfb"><thead><tr><th align="left" id="d279520e97">

Option

</th><th align="left" id="d279520e100">

Steps

</th></tr></thead><tbody><tr><td id="d279520e106">

**From the Demand form**

</td><td>

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **Workbench**.
2.  Open a demand.
3.  On the Demand form, select the **Cost Plans** or **Benefit Plans** related list.
4.  Select **Manage**.
5.  On the Demand Workbench, select the baseline information icon \( ![](../image/new-baseline-info-icon.png) \) and then select **Compare Baselines**.


</td></tr><tr><td id="d279520e165">

**From the Baseline form**

</td><td>

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.
2.  Open a demand.
3.  On the Demand form, select the **Demand Baselines** related list.
4.  Open a baseline.
5.  On the Baseline form, select the **View Financial Baseline** related link.


</td></tr></tbody>
</table>2.  On the Financial Baseline form, select the baselines you want to compare from the two lists.

    By default, the current and the most recent baselines are selected.

3.  Select **Compare**.

    The comparative data of the baselines are displayed in the following two sections:

    -   The **Financial Baseline Summary** section displays three widgets: the first two widgets contain the financial data of the two baselines, and the third widget contains their variance.
    -   The **Financial Baseline Details** section displays the cost plans and benefit plans of the two baselines in two different grids. Each plan type has two rows corresponding to each baseline data.

        **Note:** To see the color code of rows representing each baseline, select the baseline legend icon \(![](../image/new-info-icon-coral.png)\).

4.  Add additional fields or reorganize the comparative data on the **Financial Baseline Summary** section of the form.

    -   To toggle viewing the **Financial Baseline Summary** section, select the **Collapse** icon ![](../image/new-collapse-icon.png) or **Expand** icon ![](../image/new-expand-icon.png).
    -   To show or hide additional fields on the widgets in the **Financial Baseline Summary** section, select the configuration icon ![](../image/new-widget-configuration-icon.png) and select the field names.

        **Note:** If the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated, you can add additional fields to the baseline such as Total planned cost in demand currency, Operating budget in demand currency, and Financial return in demand currency.

        The selected field preferences are saved and are available when you reopen the Financial Baseline form.

    -   To reset to the default widget layout, select **Reset to defaults**.
    -   To view the financial information of the baselines in demand currency, toggle the **Show Widgets in Demand Currency** button.

        **Note:** This button is available only when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated.

5.  View details of financial data of the cost and benefit plans on the **Financial Baseline Details** section of the form.

    -   To view a cost plan or benefit plan comparative data in yearly, quarterly, or monthly format, select the **Year** or **Quarter** or **Month** views respectively.
    -   To view details of a fiscal year, select the **Expand** icon ![](../image/new-expand-icon.png) or **Collapse** icon ![](../image/new-collapse-icon.png).

**Parent Topic:**[Create a baseline of a demand](create-demand-baseline.md)

