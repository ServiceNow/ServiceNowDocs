---
title: Compare versions of a widget related record
description: Compare an Angular Provider or ng-template against its previous version so that you check if your most recent code changes are causing issues on a portal page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/service-portal/compare-related-record-changes.html
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Widget diagnostics, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Compare versions of a widget related record

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

4.  On a widget, click the information icon \(\[Omitted image "info-icon.png"\] Alt text: Information icon\).

    Related records that you modified or developed are outlined in red.

    \[Omitted image "outlined-in-red.png"\] Alt text: Related records outlined in red

5.  Next to a Angular Provider or ng-template record, click **Compare**.

    The system displays the records of the current and previous versions side by side.

    \[Omitted image "compare-related-record.png"\] Alt text: Comparison between current and previous versions of a related record

    Although both sides are labeled **Version**, the left-side record represents the previous version and the right-side record represents the current version.

6.  For each field in which it appears, click the window icon \(\[Omitted image "pop-out-icon.png"\] Alt text: Window icon\) to open the code comparator.

    Your most recent changes to the widget code are highlighted in the code comparator.

    \[Omitted image "code-comparator.png"\] Alt text: Code comparator


