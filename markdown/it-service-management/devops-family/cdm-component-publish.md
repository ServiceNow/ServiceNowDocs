---
title: Publish or unpublish a shared component version
description: Publish a version of a shared component in a library so that it can be used in an application.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Sharing components among applications — Component libraries, Use, DevOps Config, IT Service Management]
---

# Publish or unpublish a shared component version

Publish a version of a shared component in a library so that it can be used in an application.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

<table id="choicetable_ow3_zws_2xb"><thead><tr><th align="left" id="d343900e138">

Option

</th><th align="left" id="d343900e141">

Description

</th></tr></thead><tbody><tr><td id="d343900e147">

**Publish a version of a shared component**

</td><td>

Select an unpublished version from the list and select **Publish**.If there’s any existing published version of the component, then it’s unpublished before publishing the selected version. The **Published** value updates to **true**.

</td></tr><tr><td id="d343900e167">

**Unpublish a version of a shared component**

</td><td>

Select a published version from the list, select the ![Down arrow button.](../image/icon-down-arrow-button.png), and then select **Unpublish**.The selected version of the component is unpublished and the **Published** value updates to **false**.

</td></tr></tbody>
</table>
