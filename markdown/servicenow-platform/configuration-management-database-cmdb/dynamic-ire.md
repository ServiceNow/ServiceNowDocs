---
title: Dynamic IRE
description: Dynamic Identification and Reconciliation Engine \(IRE\) processes CI identification for maximum accuracy and efficiency and eliminates the need to manually create or maintain rules. Actually, you can't alter any of the algorithms or operations of Dynamic IRE.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Dynamic IRE

Dynamic Identification and Reconciliation Engine \(IRE\) processes CI identification for maximum accuracy and efficiency and eliminates the need to manually create or maintain rules. Actually, you can't alter any of the algorithms or operations of Dynamic IRE.

When necessary to differentiate, the legacy, manually-driven IRE, is referred to as Static IRE.

Dynamic IRE is a new engine that you can choose to use instead of Static IRE. Dynamic IRE identifies CIs using an improved identification dynamic process and automatically updates its IRE identification rules during ingestion of data payloads.

Dynamic IRE evaluates various conditions within the payload simultaneously by running algorithms in parallel to score potential matches and to accurately determine CI identity across multiple data sources. Compared to Static IRE, on average, Dynamic IRE matches CIs using a larger combination of the CI attributes to improve the chances of finding an optimal match, and by so, reducing the chances for duplicate CIs.

Dynamic IRE is applicable only to the Hardware \[cmdb\_ci\_hardware\] class and its descending classes. However, you can configure the system to exclude from Dynamic IRE specific classes descending from the Hardware class.

Key benefits of Dynamic IRE are:

-   Usually identifies CIs more accurately resulting in a reduction of duplicate CIs.
-   Eliminates manual configuration and continuous maintenance of IRE process rules.

## Modes of operation

Dynamic IRE provides two modes of operation:

-   **Simulation mode**

    In simulation mode, Dynamic IRE and Static IRE run in parallel so you can experience and compare Dynamic IRE to Static IRE.

    In simulation mode, both Static IRE and Dynamic IRE process the payloads, and any differences in processing and outcome are stored in the CMDB IRE Output Comparison Items \[cmdb\_ire\_output\_comparison\_item\] table. Also, after some time of simulations, you can compare the performance of Dynamic IRE to Static IRE.

-   **Committed mode**

    In committed mode, only Dynamic IRE performs IRE processes and Static IRE is turned off. Once in a committed mode, you can switch back to Static IRE without implications.


Typically, you should start with the simulation mode on a non-production instance to test effectiveness and performance, examine the outcome, and then commit to full usage of Dynamic IRE on your production instance.

## Exclude classes from Dynamic IRE

There might be reasons for configuring child classes descending from the Hardware class, to be excluded from Dynamic IRE. For example, you might want to exclude a custom class with custom attributes, for which there are IRE rules that are based on those custom attributes. In this situation, it might not be beneficial to apply Dynamic IRE for that class and its descendants. So if Dynamic IRE is enabled, Static IRE is still being used for those excluded classes.

For more information, see [Exclude classes from Dynamic IRE](../task/dynamic-ire-exclude-class.md).

## Simulate and commit to Dynamic IRE

To start using Dynamic IRE exclusively, a general guideline is to test it first by simulation on a non-production instance:

1.  Ensure that you meet the user role requirement: sn\_cmdb\_user.
2.  On a non-production instance, navigate to the CI Class Manager.
3.  In CI Class Manager, select **Hierarchy** and then select the Hardware class.
4.  In the Hardware navigation panel, select **Identification Rule**.
5.  In the Dynamic IRE section, select **Simulate Dynamic IRE**.
6.  Carefully review the Simulate Dynamic IRE tile:
    -   If you're ready to start a simulation to test Dynamic IRE on a non-production instance, select **Simulate Dynamic IRE**. The simulation runs IRE processes on the Hardware and any descending classes, and then shows a comparison in terms of effectiveness and performance, between Dynamic and Static IRE. Carefully examine this comparison, which can help you determine whether to commit to using Dynamic IRE.
    -   If you have already completed a simulation, reviewed the results, and are ready to fully use Dynamic IRE with the Hardware class, on a production instance select the agreement and then select **Commit to Dynamic IRE**.

Alternatively, you can use the **glide.identification\_engine.dynamic\_ire\_enabled** system property to enable or disable Dynamic IRE, and by so, switching between Dynamic and Static IRE. For more information about this property, see [Properties for Identification and Reconciliation](../reference/properties-id-reconciliation.md).

## Comparison of the results of Dynamic IRE and Static IRE

In simulation mode, you can see a comparison of the activities and outcome between Dynamic IRE and Static IRE, at a high level and at a record level. Examine the details in this comparison carefully, to help you evaluate the effectiveness of Dynamic IRE in your environment before committing to using it.

This comparison calculates a parity score, which is the percentage of identical results between Dynamic IRE and Static IRE.

**Note:** For a mature Static IRE implementation \(with manually-created rules\), the parity score is expected to be high. This indicates that Dynamic IRE is capable of producing similar results to Static IRE without requiring any manually-created rules or validations for accuracy.

![Charts of comparison between Dynamic and Static IRE.](../../now-assist-cmdb/image/na-cmdb-ire-compare-skill.png)

Bar charts show the difference in CI operations of inserting CIs, updating CIs, and CIs found to be incomplete, between the two methods. Select a bar to show the list of comparison records from the CMDB IRE Output Comparison Items \[cmdb\_ire\_output\_comparison\_item\] table, for the selected bar chart. Those records contain the details about CIs that were processed differently between Dynamic IRE and Static IRE. Select a record to open it and to review the comparison details \(in JSON format\).

On a record form, you can select **Summarize** to show an organized and more user friendly presentation of the comparison results, generated by the Now Assist for CMDB IRE comparison record summarization skill.

**Parent Topic:**[Exploring CMDB Identification and Reconciliation \(IRE\)](exploring-ire.md)

