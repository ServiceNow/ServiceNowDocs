---
title: Enable magic links
description: Configure magic links to enable consumer users to access provider instance resources directly without manual authentication. Magic links streamline cross-instance navigation by automatically handling login credentials.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use for providers, Service Exchange for Providers, Service Exchange]
---

# Enable magic links

Configure magic links to enable consumer users to access provider instance resources directly without manual authentication. Magic links streamline cross-instance navigation by automatically handling login credentials.

## Before you begin

Role required: sn\_sb.admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumers**.

2.  Open the appropriate Consumer Connection form.

3.  Under the Related Links, select the **Settings** tab and open the record displayed.

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
</table>5.  Select **Update**.


**Parent Topic:**[Using Service Exchange for providers](../concept/service-bridge-v2-administer.md)

