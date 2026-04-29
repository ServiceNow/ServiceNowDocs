---
title: Integer values for default choice lists
description: Choice provide four default values.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Choice list field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Integer values for default choice lists

Choice provide four default values.

Some common choice lists use integer values that do not match the string labels. For example, the Problem table uses these default values for the **State** field.

|Value|Label|
|-----|-----|
|1|Open|
|2|Known Error|
|3|Pending Change|
|4|Closed/Resolved|

These integer values are also used in several default business rules. For example, a business rule on the Incident table sets the active flag to false when the **State** field changes to **7**, which is the default value for the **Closed**. If you change the values of your Incident state options, this business rule may no longer behave as desired or expected.

On the Incident table, the **Active**, **State**, and **Incident state** fields are affected by the following default business rules.

|Business rule|Description|
|-------------|-----------|
|mark\_closed \(incident\)|If the incident\_state changes to **7** \(**Closed**\), the **Active** field is set to false|
|incident reopen \(incident\)|If the incident\_state is less than **7** \(**Closed**\) and the **Active** field is false, the **Active** field is set to true|
|mark closed \(task\)|If the state changes to either **3** \(**Closed Complete**\) or **4** \(**Closed Incomplete**\), the **Active** field is set to false|
|task closer \(task\)|If the **Active** flag changes from true to false and the state is neither **3** \(**Closed Complete**\) nor **4** \(**Closed Incomplete**\), the state is set to **3** \(**Closed Complete**\)|
|task reopener \(task\)|If the **Active** field changes from false to true and the state is either **3** \(**Closed Complete**\) or **4** \(**Closed Incomplete**\), the state is set to **1** \(**Open**\)|

**Note:** Notice that these business rules do not change incident\_state based on a change to either the **Active** field or the **State** field. Changes to incident\_state drive the other two fields, not the other way around.

