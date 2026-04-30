---
title: Configure Next Experience debugging preferences
description: Debug your Next Experience instance to detect and remove existing and potential errors in your Next Experience components and scripts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Preferences, Working in Next Experience, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure Next Experience debugging preferences

Debug your Next Experience instance to detect and remove existing and potential errors in your Next Experience components and scripts.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **User Menu** &gt; **Preferences** &gt; **Debugging**.

2.  Select one of the debugging options.

<table id="table_k23_qnk_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script Debugger

</td><td>

Opens a JavaScript debugger with a script tracer and a session log. For more information, see [Debugging scripts](https://www.servicenow.com/docs/access?context=script-debug-overview&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr><tr><td>

UX Source Maps

</td><td>

Enables you to perform debugging using UX source maps in your browser. For example, when used with Firefox v102+, the user can set a break point in component code and, when the browser stops at that break point, variable names should appear in the scope section. **Note:** When you are not debugging using UX source maps, it is best to toggle this user preference off as it can cause performance degradation of the instance.

</td></tr><tr><td>

Automated Test Framework Page Inspector

</td><td>

Enables you to identify and inspect pages created in classic custom UI pages using the page inspector. For more information, see [Page Inspector](https://www.servicenow.com/docs/access?context=atf-page-inspector&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Seismic Developer Tool

</td><td>

Opens a link to the Chrome web store Seismic Developer Tools download page. The Seismic Dev Tools \(SDT\) Chrome Extension is a tool that helps Seismic developers effectively identify, diagnose, and resolve defects and performance issues.**Note:** This option can be removed from the Debugging user preferences by setting the **glide.ui.next\_experience.seismic\_developer\_tool\_user\_pref\_enabled** system property to **false**.

</td></tr></tbody>
</table>
