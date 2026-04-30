---
title: List of Notify calls
description: If you are a Notify administrator, you can view a list of calls and the status of a call made to or from Notify. The call records help in reporting and analytics.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Notify for making conference calls, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# List of Notify calls

If you are a Notify administrator, you can view a list of calls and the status of a call made to or from Notify. The call records help in reporting and analytics.

To view a list of calls, navigate to **Notify** &gt; **Calls**.

Call records are generated automatically when a user calls a Notify number or when a user makes an outbound call through Notify. You cannot create call records manually.

**Note:** Although you can delete a call record, doing so may result in cascade deletion of related records.

For Notify calls where the source is specified, such as a task number, the source is added to the Notify Calls \[notify\_call\] table in the **Source** column. For Notify conference calls where the source is specified, the source is added to the records for each of the calls in the conference.

|Call status|Description|
|-----------|-----------|
|initiated|The number has just been dialed|
|ringing|The call is currently ringing.|
|in\_progress|The call was answered and is currently in progress.|
|no\_answer|The call was not answered.|
|completed|The call was answered and has ended normally.|
|busy|The caller received a busy signal.|
|failed|The call could not be completed as dialed, most likely because the phone number was non-existent.|
|invalid|The call could not be connected since input is invalid.|
|unknown|The driver does not support the status|

**Parent Topic:**[Using Notify for making conference calls](../concept/c_NotifyConferenceCalls.md)

