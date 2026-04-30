---
title: Canceled-transaction logging to a table
description: The system logs canceled transactions to a table in addition to the transaction log.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Transaction cancellation, Resolving platform performance issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Canceled-transaction logging to a table

The system logs canceled transactions to a table in addition to the transaction log.

Transactions canceled manually or by a quota rule are logged to the Transaction Cancellation Log \[syslog\_cancellation\] table. The Transaction Cancellation Log is an extra debugging feature, and doesn't contain information on all cancellations.

**Note:** There are safeguards in place to help prevent infinite loops and issues related to synchronicity. Because of this, it's not always possible to log a cancellation to a database table.

You can find the Transaction Cancellation Log by selecting **System Logs** &gt; **System Log** &gt; **Transaction Cancellations**.

You can turn off canceled-transaction logging to a table by changing a property.

<table id="table_awx_phf_z5"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.quota.manager.log.cancellation

</td><td>

Indicates whether canceled transactions are to be logged to the Transaction Cancellation Log table.Type: Boolean

 Default value: true

 Location: [Add to the System Properties](../../reference-pages/reference/r_AvailableSystemProperties.md#) \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Transaction cancellation](transaction-cancellation.md)

