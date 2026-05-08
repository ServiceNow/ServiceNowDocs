---
title: Publish or unpublish a shared component version
description: Publish a version of a shared component in a library so that it can be used in an application.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sharing components among applications — Component libraries, Using DevOps Config, DevOps Config, IT Service Management]
---

# Publish or unpublish a shared component version

Publish a version of a shared component in a library so that it can be used in an application.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_admin

## About this task

When a version is unpublished, it means that the component and its version can no longer be used in an application. However, it has no impact on applications that are already using the version.

**Note:** A shared component can only have one published version at a time.

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Click the component libraries icon \(![Component libraries icon.](../image/icon-component-libraries.png)\) in the left navigation pane to open the **Component libraries** list tab.

3.  Select a component library from the **Component libraries** list tab.

4.  Select the **Components** tab and then select a component name to open.

5.  Select the **Versions** tab.

6.  Publish or unpublish a version of the component.

<table id="choicetable_ow3_zws_2xb"><thead><tr><th align="left" id="d409291e127">

Option

</th><th align="left" id="d409291e130">

Description

</th></tr></thead><tbody><tr><td id="d409291e136">

**Publish a version of a shared component**

</td><td>

Select an unpublished version from the list and select **Publish**.If there’s any existing published version of the component, then it’s unpublished before publishing the selected version. The **Published** value updates to **true**.

</td></tr><tr><td id="d409291e156">

**Unpublish a version of a shared component**

</td><td>

Select a published version from the list, select the ![Down arrow button.](../image/icon-down-arrow-button.png), and then select **Unpublish**.The selected version of the component is unpublished and the **Published** value updates to **false**.

</td></tr></tbody>
</table>
