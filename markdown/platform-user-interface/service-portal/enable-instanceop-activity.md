---
title: Enable instance options for the Activity tab
description: Format the work notes and add @mentions in the Activity tab on a standard ticket page.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure the standard ticket page, Standard ticket page, Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable instance options for the Activity tab

Format the work notes and add @mentions in the Activity tab on a standard ticket page.

## Before you begin

Role required: sp\_admin or admin

You should add the **Activity** tab in the standard ticket configuration of a request type. For information on configuring tabs, see [Configure the standard ticket page](configure-st-page.md).

## Procedure

1.  Navigate to the request in Service Portal.

2.  Press Control and right-click anywhere in the **Activity** tab.

3.  Click **Instance Options**.

4.  Configure settings for the **Activity** tab.

<table id="table_chk_fqc_fmb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Rich Text Editor

</td><td>

Option to enable formatting the work notes.**Note:**

For the Ticket Form for Case \(csm\_ticket\) page, the **Activity** tab options must be configured from the Activity tab configuration record of the sn\_customerservice\_case page.

1.  Navigate to **All** &gt; **Standard Ticket Configuration**.
2.  Select the **sn\_customerservice\_case** record.
3.  In Tab Configurations, select the **Activity** tab configuration record.
4.  Edit the **rich\_text\_editor** widget parameter field.


</td></tr><tr><td>

Enable @ Mentions \(works only when Rich Text Editor is enabled\)

</td><td>

Option to enable mentioning the relevant people in work notes.**Note:** This option is applicable only when the **Enable Rich Text Editor** instance option is selected.

</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Configure the standard ticket page](configure-st-page.md)

