---
title: Split a SAFe feature
description: Split a SAFe feature into two separate features so that you can track complete and incomplete stories. You can move the feature with the incomplete stories to your backlog or to a future program increment \(PI\) so that you can maintain accurate metrics of the previous sprints and PIs.
locale: en-US
release: xanadu
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Define a feature in SAFe, SAFe entities, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Split a SAFe feature

Split a SAFe feature into two separate features so that you can track complete and incomplete stories. You can move the feature with the incomplete stories to your backlog or to a future program increment \(PI\) so that you can maintain accurate metrics of the previous sprints and PIs.

## Before you begin

Role required: safe\_art\_user or safe\_admin

## About this task

If your SAFe feature has incomplete stories at the end of a PI, you can split this feature into two features.

The new feature has a reference to the original feature and the field values are copied from the original feature.

The completed stories of the original feature move to a new feature whose state is set to **Released**.

**Note:** To split a SAFe feature, you must have at least one complete and incomplete story each.

## Procedure

1.  Navigate to **All** &gt; **Scaled Agile Framework \(SAFe\)** &gt; **SAFe Board**.

2.  From the list at the top-left corner, select the level as **ART** and select your agile release train.

3.  Click the **Backlog** tab.

4.  Select the **List** view.

    ![SAFe program increment list view](../../benchmarks-for-spm/images/list-view.png)

5.  From your current PI section, locate the SAFe feature that has incomplete stories and click its number to open its form.

    You can click **Complete** to get the list of incomplete features.

6.  On the feature form, click the **Move completed stories to new feature** related link.

    -   The updated feature form shows only those stories that are incomplete.
    -   The new feature contains the completed stories from the original feature.
    -   The **Original feature** field on the new feature references to the original feature that you've split.

        **Note:** Configure your feature form layout to view this field.

    -   "- Completed" is appended to the short description of the new feature to indicate that it is complete.

## What to do next

Schedule the feature that has incomplete stories to your backlog or a new PI of your choice.

**Parent Topic:**[Define a feature in SAFe](create-SAFefeature.md)

