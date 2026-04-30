---
title: Compare changes to related records
description: Compare an Angular Provider or ng-template against its previous version so that you check if your most recent code changes are causing issues on a portal page.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Widget diagnostics, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Compare changes to related records

Compare an Angular Provider or ng-template against its previous version so that you check if your most recent code changes are causing issues on a portal page.

## Before you begin

Role required: admin or sp\_admin

## About this task

Your widget may be using potentially problematic code from any of the following records:

-   Widget Dependencies
-   Angular Providers
-   Angular ng-templates

You can compare versions for these related records directly from your portal page to check code changes for each related record.

**Note:** There's no option to compare versions for Widget Dependency records. Also, there's no option to compare versions for related records that you created. You can only compare versions of a base system record that you modified.

## Procedure

1.  Navigate to a portal page.

2.  On the page, open the widget context menu by CTRL+right-clicking any widget.

3.  On the widget context menu, click **Show Widget Customizations**.

    Widgets are color-coded as follows:

    |Color|Customization level|
    |-----|-------------------|
    |Green|Base system widget|
    |Yellow|Cloned widget|
    |Blue|New widget|
    |Red|Customized widget|

4.  On a widget, click the information icon \(![Information icon](../image/info-icon.png)\).

    Related records that you modified or developed are outlined in red.

    ![Related records outlined in red](../image/outlined-in-red.png)

5.  Next to a Angular Provider or ng-template record, click **Compare**.

    The system displays the records of the current and previous versions side by side.

    ![Comparison between current and previous versions of a related record](../image/compare-related-record.png)

    Although both sides are labeled **Version**, the left-side record represents the previous version and the right-side record represents the current version.

6.  For each field in which it appears, click the window icon \(![Window icon](../image/pop-out-icon.png)\) to open the code comparator.

    Your most recent changes to the widget code are highlighted in the code comparator.

    ![Code comparator](../image/code-comparator.png)


**Parent Topic:**[Widget diagnostics](../concept/sp-diagnostic-tool.md)

