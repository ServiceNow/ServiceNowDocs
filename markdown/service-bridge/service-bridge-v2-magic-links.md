---
title: Enable magic links
description: Use magic links to enable consumer users to directly access the linked resource in the provider instance without having to manually log in.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install and configure for provider, Service Exchange for Providers, Service Exchange]
---

# Enable magic links

Use magic links to enable consumer users to directly access the linked resource in the provider instance without having to manually log in.

## Before you begin

Role required: sn\_sb.admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumers**.

2.  Open the appropriate Consumer Connection form.

3.  Under the Related Links, click the **Settings** tab and open the record displayed.

4.  In the **Magic link** tab, perform the following steps:

<table id="table_eff_bfp_rfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable magic links

</td><td>

Option to enable magic links functionality. When enabled, the magic link routes consumer user \(remote user\) to provider instance for completion of tasks.

</td></tr><tr><td>

Single user mode

</td><td>

Option to enable the consumer user to be authenticated as a specific user when accessing the provider instance.

</td></tr><tr><td>

Redirect timeout

</td><td>

Option to specify the number of seconds taken to redirect consumer user to provider instance. The default value is 5, and the maximum limit is 30.**Note:** The redirect timeout can be set only in the consumer instance; it is read-only field on the provider instance. If Redirect timeout value is 0 or empty, consumer user is automatically redirected to the provider instance without any loader UI.

</td></tr></tbody>
</table>5.  Click **Update**.


