---
title: Configure document expiration monitoring attributes
description: Configure document attributes such as grace period, lead time, and reminder frequency to manage document that are near or past their original expiry date.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supplier Document Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure document expiration monitoring attributes

Configure document attributes such as grace period, lead time, and reminder frequency to manage document that are near or past their original expiry date.

## Before you begin

Role required: sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Administration** &gt; **Supplier document expiration monitoring attributes**.

    The Decision Builder opens and displays the Decision table to configure the grace period, lead time, and reminder frequency.

<table id="table_a3r_mzq_k3c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grace period

</td><td>

Additional time allotted to complete the document upload task after the initial due date is past. The default duration for this attribute is 30 days.**Note:** A supplier case is created once the grace period elapses. For more information, see [Case playbook for specific supplier case types](../concept/gen-playbook-cases.md).

</td></tr><tr><td>

Reminder frequency

</td><td>

The frequency at which email reminders are sent within the grace period for completing the document task. The default reminder frequency is set to 7 days.

</td></tr><tr><td>

Lead time

</td><td>

The number of days before the document expiry date when a document upload task is created. The default time is 30 days.**Note:** A supplier task is created once the configured lead time elapses.

</td></tr></tbody>
</table>2.  In the decision table, go to the document attribute that you want to configure and set the time period in terms of days.

3.  Select **Save**.


**Parent Topic:**[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

**Related topics**  


[Create a supplier document configuration](create-doc-config.md)

[Manually run a supplier document configuration](run-doc-config.md)

[Uploading supplier documents](../concept/upload-doc-about.md)

