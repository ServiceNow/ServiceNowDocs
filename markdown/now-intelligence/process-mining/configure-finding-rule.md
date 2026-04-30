---
title: Configure finding rules
description: Configure finding rules for your finding definition. Finding rules define what record criteria triggers your finding definitions.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set rule-based finding definitions using Classic view, Setting improvement opportunities from Classic view, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure finding rules

Configure finding rules for your finding definition. Finding rules define what record criteria triggers your finding definitions.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## Procedure

1.  Open the finding definition record where you want to add a finding rule.

2.  In the **Finding Rules** tab, select **New**.

3.  On the form, fill in the fields.

    For a description of the field values, see [Finding rule form](../reference/finding-rule-form.md).

4.  Right-click the form header, and select **Save** to save the finding rule record.

5.  To create additional finding rule within the same chain, select **Create next rule \(same chain\)**.

    This option opens a new finding rule within the same chain. The **sequence** value is one higher than the current rule.

6.  To create additional finding rule within a new chain, select **Create next rule \(new chain\)**.

    This option opens a new finding rule within a new chain.


## Example

In this example, a finding rule is created to find when someone requests an approval on an incident record, and that approval is approved by the same user. Because the **Duration min** field is set to one day, the rule only triggers when the approval is approved more than 24 hours after it was requested.

![Example finding rule record](../image/finding-rule-example-new.png "Example of finding rule record")

## What to do next

-   Configure automated root cause analysis to find the root cause of undesired process behavior. For details on this feature. See [Automated root cause analysis](../concept/auto-rca.md).
-   Configure Automation Discovery to help you identify automation opportunities for your workflows. For details on this configuration, see [Automation Discovery](../../automation-discovery/concept/automation-discovery.md).

-   Configure cluster analysis to group similar records into a cluster \(one group\) so you can identify patterns. For more detail on this configuration, see [Cluster analysis](../concept/cluster-analysis.md).


**Parent Topic:**[Set rule-based finding definitions using Classic view](configure-finding-definition.md)

