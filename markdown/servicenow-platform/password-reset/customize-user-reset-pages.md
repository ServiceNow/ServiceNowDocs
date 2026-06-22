---
title: Add a custom header or footer to the user pages for Password Reset
description: You can specify UI macros that add a header or footer to the pages that end users work in while resetting a password \(the Identify, Verify, and Reset pages\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/password-reset/customize-user-reset-pages.html
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing Password Reset processes, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a custom header or footer to the user pages for Password Reset

You can specify UI macros that add a header or footer to the pages that end users work in while resetting a password \(the Identify, Verify, and Reset pages\).

## Before you begin

Role required: password\_reset\_admin

## About this task

\[Omitted image "header-footer-enduser-pages.png"\] Alt text: Example custom header and footer on the password reset pages

## Procedure

1.  Configure a UI macro for the header or footer: Navigate to **All** &gt; **System UI** &gt; **UI Macros**, click **New**, and then enter a meaningful **Name** and **Description**.

2.  In the **XML** text box, enter the macro text.

    The example macro adds the text "Trust Acme to Deliver!" to the footer of the page that users work in while resetting a password.

    \[Omitted image "header-footer-macro-DOC45847.png"\] Alt text: XML macro code for a custom footer

3.  Select the **Active** check box and then click **Submit**.

4.  Navigate to **Password Reset** &gt; **Processes** and select the process to update.

5.  On the **Advanced** tab, click \(\[Omitted image "look-up-in-list-button.png"\] Alt text: magnifying glass icon\) for the **Header UI macro** or **Footer UI macro** and select the macro that you created.

6.  Click **Save**.

7.  Verify the appearance of the end-user pages.

<table id="choicetable_pzg_5m2_wbb"><tbody><tr><td id="d276614e178">

**If the reset pages are Public Access**

</td><td>

On the **Password Reset Details** tab, click the **Public URL**.

</td></tr><tr><td id="d276614e193">

**If the reset pages are not Public Access**

</td><td>

Log in as an end user and request password reset.

</td></tr></tbody>
</table>
**Parent Topic:**[Customizing Password Reset processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/password-reset/customizing-password-reset.md)

