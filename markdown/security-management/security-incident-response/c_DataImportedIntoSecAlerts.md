---
title: Data imported into security alerts
description: When an event is created with more JSON-encoded data, that data is imported into any field with a name that matches the fieldName of that value in the JSON data.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security incidents created from events and alerts, Security incident automatic creation, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Data imported into security alerts

When an event is created with more JSON-encoded data, that data is imported into any field with a name that matches the fieldName of that value in the JSON data.

If you have data in your third-party monitoring software \(for example, Splunk\) that is not common to the base system, you can add new fields to the Alert table to accommodate the data import. The JSON format for importing data into alerts is the same format used for creating security incidents from events and alerts:

```
{ "fieldName" : "fieldValue", "fieldName" : "fieldValue" }
```

The only difference is that the data in the field is always overwritten with the fieldValue.

When the security event data is imported, it populates the fields in the Alert table with matching field names. If the alert is later turned into a security incident, the same additional information data populates matching fields in the security incident.

