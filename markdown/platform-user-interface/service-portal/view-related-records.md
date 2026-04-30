---
title: View related records
description: View and identify potentially problematic code in the widget dependencies, Angular Providers, and ng-templates that are being used by the widget.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Widget diagnostics, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# View related records

View and identify potentially problematic code in the widget dependencies, Angular Providers, and ng-templates that are being used by the widget.

## Before you begin

Role required: admin or sp\_admin

## About this task

Your widget may be using potentially problematic code from any of the following records:

-   Widget Dependencies
-   Angular Providers
-   Angular ng-templates

You can view these related records directly from your portal page to check the code in each record.

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

4.  On any widget, click the information icon \(![Information icon](../image/info-icon.png)\).

5.  On the window, open links to the following related records:

<table id="table_q5f_hbh_djb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dependencies

</td><td>

JavaScript and CSS files that the widget uses from the Widget Dependencies \[sp\_dependency\] table.**Note:** The widget dependencies listed on this window only reflect the first-level dependencies. Any dependency that is nested deeper than the first level is not included. To further troubleshoot the widget, check the nested dependencies in the widget record.

</td></tr><tr><td>

Angular Providers

</td><td>

Angular Providers that the widget uses from the Widget Angular Providers \[sp\_angular\_provider\] table.

</td></tr><tr><td>

Angular templates

</td><td>

Angular ng-templates that the widget uses from the Angular ng-templates \[sp\_ng\_template\] table.

</td></tr></tbody>
</table>    Related records that you modified or developed are outlined in red.

    ![Related records outlined in red](../image/outlined-in-red.png)

    You can open each related record by clicking the record name.


## What to do next

If you're still unable to diagnose the widget, consider checking nested dependencies or URL dependencies.

**Parent Topic:**[Widget diagnostics](../concept/sp-diagnostic-tool.md)

