---
title: Double-check form submission
description: When the system determines that a particular field \(such as task.number\) should not be written to by the current user, the system renders that field in a read-only mode, which is why the number field is not writable on most incidents.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contextual Security Manager, Access Control List Rules, Access Management]
---

# Double-check form submission

When the system determines that a particular field \(such as task.number\) should not be written to by the current user, the system renders that field in a read-only mode, which is why the number field is not writable on most incidents.

If you set the system to double-check the values of any incoming fields for writability, then the system applies the same set of security rules to the inbound leg of a transaction. When you submit an incident, for example, the system double-checks to determine if the number field can be written to before posting any changes.

If you tell the system not to double-check inbound transactions, then the system allows you to write to a nominally read-only field if that is the transaction the client sends back. In many deployments this is actually a desirable behavior if, for example, you are using client scripts to set nominally read-only fields in response to user selections in other, writable fields.

|Property|Location|Default|
|--------|--------|-------|
|Double check security on inbound transactions during form submission \(rights are always checked on form generation\)|**System Properties** &gt; **Security**|Disabled \(no double-checking\)|

