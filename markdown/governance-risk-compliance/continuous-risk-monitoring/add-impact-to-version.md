---
title: Add impact to version
description: Add impact levels to a version to categorize authorization packages by risk level. Impacts filter control objectives based on the impact requirements and work with versions.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-12-03"
reading_time_minutes: 1
breadcrumb: [Add version to workflow, Workflow configuration, CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Add impact to version

Add impact levels to a version to categorize authorization packages by risk level. Impacts filter control objectives based on the impact requirements and work with versions.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **Workflow Configurations**.

2.  Select a Workflow Configuration.

3.  To view the impact list, select the expand icon \(![impact expand icon](../image/WF-version-and-impact-icon.png)\) in the **Versions** tab.

4.  Select **New** to add a new impact.

    ![Adding impact to version.](../image/WF-version-and-impact4.png)

    **Impact New record** page displays.

5.  On the **Impact New record** form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |Name|Enter the impact level name \(for example, Low, Moderate, High, or Critical\).|
    |Workflow version|The workflow version is automatically populated based on the version that you have selected.|
    |Active|Select the **Active** option to make the impact available for selection.|
    |Order|The order in which you want to list the impacts.|
    |Filter condition|Enter the condition to filter control objectives by this impact level.|

6.  Select **Submit** to add the new impact to the selected version.


## Result

The workflow impact is available for authorization packages. Baseline controls are filtered based on both version and impact conditions.

## What to do next

[Add view rules to workflow](add-view-rules-to-workflow.md)

