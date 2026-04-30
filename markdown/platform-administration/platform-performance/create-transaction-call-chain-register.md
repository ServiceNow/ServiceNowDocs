---
title: Create a transaction call chain register
description: Create a call chain register to record call chain information for a problematic \(or slow\) transaction during the next occurrence of that URL. You specify that the next occurrence of the transaction URL should be persisted with all of its call chain information.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Transaction call chains, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Create a transaction call chain register

Create a call chain register to record call chain information for a problematic \(or slow\) transaction during the next occurrence of that URL. You specify that the next occurrence of the transaction URL should be persisted with all of its call chain information.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the Transaction Log or Slow Transactions list, select the problematic transaction, and enable recording of the call chain.

<table id="choicetable_nc2_kmn_f4b"><thead><tr><th align="left" id="d121326e54">

Type of Log

</th><th align="left" id="d121326e57">

Steps

</th></tr></thead><tbody><tr><td id="d121326e63">

**Transaction Log**

</td><td>

1.  Navigate to **System Logs** &gt; **Transactions**
2.  To aid in debugging, filter and group the Transaction Log by application scope, limiting transactions that appear to only those transactions originating in specific scopes.
3.  Select the problematic transaction.
4.  In the Transaction Log Entry form, select **Open Record**, then select **Record call chain of next occurrence**.


</td></tr><tr><td id="d121326e101">

**Slow Transactions**

</td><td>

1.  Navigate to **System Diagnostics** &gt; **Stats** &gt; **Slow Transactions**
2.  To aid in debugging, filter and group the Slow Transactions list by application scope, limiting transactions that appear to only those transactions originating in specific scopes.
3.  Select the problematic transaction.
4.  In the Slow Transactions form, click **Open Record**, then select **Record call chain of next occurrence**.


</td></tr></tbody>
</table>2.  On the Transaction Call Chain Register form, fill in the fields.

    For a description of the field values, see [Transaction call chain register form](../reference/transaction-call-chain-reg-form.md).

3.  Select **Submit**.


## Result

A call chain register is created to designate that the next occurrence of the transaction URL should be persisted with all of its call chain information.

**Note:** Once the call chain is recorded \(**true** appears in the **Recorded** field\), you can view it in the Transaction Call Chain Register form itself.

## What to do next

[Review a transaction call chain](review-transaction-call-chain.md)

**Parent Topic:**[Transaction call chains](../concept/transaction-call-chains.md)

