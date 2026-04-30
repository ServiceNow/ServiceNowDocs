---
title: Inspect different page types
description: Inspect and troubleshoot the functionality of different page types like UI Pages, Service Portal, Standard UI, and Custom URL using the Page Inspector.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Page Inspector, Custom UI test steps, UI test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Inspect different page types

Inspect and troubleshoot the functionality of different page types like **UI Pages**, **Service Portal**, **Standard UI**, and **Custom URL** using the Page Inspector.

## Before you begin

Role required: admin, atf\_test\_designer, atf\_test\_admin

## Procedure

1.  Navigate to **All** &gt; **Page Inspector** &gt; **Manual Page Inspector**.

2.  Select the **Page Type** you want to inspect.

<table id="table_f43_tsd_blb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

UI Pages

</td><td>

Existing UI pages. Select a starting page from the available list.

</td></tr><tr><td>

Standard UI

</td><td>

Standard platform forms, lists, and some UI pages. Select a form or a list or a UI page in the **Starting Page** field.**Note:** The optional **Record** field shows up only if you select a form in the **Starting Page** field.

</td></tr><tr><td>

Service Portal

</td><td>

Any available portal in the instance. Select an available portal and a starting page to be inspected.**Note:** Portal field shows up only if you select Service Portal as the **Page Type**.

</td></tr><tr><td>

Custom

</td><td>

Custom Platform URL to be inspected.**Note:** Don’t copy-paste the complete URL onto the **Starting Page URL** field. For example, include only `/home.do` as the input if you want to inspect `https://instance.service-now.com/home.do`

</td></tr></tbody>
</table>3.  Click **Inspect**.


**Parent Topic:**[Page Inspector](../concept/atf-page-inspector.md)

