---
title: Compare pattern versions
description: If you have multiple versions of the same pattern, you can compare them to decide which pattern version to use for discovery.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Choose the pattern version, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Compare pattern versions

If you have multiple versions of the same pattern, you can compare them to decide which pattern version to use for discovery.

## Before you begin

Role required: pd\_admin

## About this task

Service Mapping and Discovery use patterns in their discovery process. Every time you modify and save a pattern, you create a version of this pattern.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  Click the required pattern.

    The form for this pattern opens.

3.  Click the **Pattern** tab.

4.  Scroll down to the **Versions** section.

    The state of the active pattern version that Service Mapping and Discovery use is **Current**.

5.  Click the previous pattern version, which you want to compare to the current version.

6.  Click **Compare to Current** under **Related Links**.

7.  In the Compare to Current window, click the **Pattern text** pane either under **Selected Version** or **Current Version**.

    ![Click the Pattern text pane to open the text comparison window.](../image/CompareToCurrent.png)

    The text comparison view opens showing the text of the selected pattern version and the current pattern version side by side. The step containing a difference appears highlighted.

    Highlight colors indicate the type of change:

    -   Updated step — purple
    -   New line or characters — green
    -   Deleted line or characters — red
8.  Review the differences in the pattern versions.

9.  If necessary, click **Revert chunk** to replace the step in the current version with the step from the previous version.

    ![Click Revert chunk to replace the step in the current step with the step from the previous version.](../image/CompareToCurrentRevertChunk.png)

10. Click **OK** when done.

11. If you copied any steps from the previous version and want to save the change, click **Save Merge**.


**Parent Topic:**[Choose the pattern version](t_ChoosePatternVersionPatDef.md)

