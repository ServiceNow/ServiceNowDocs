---
title: Multi-record, custom field Splunk alert examples
description: When you are creating multiple record Splunk alerts with custom fields, you need to define search criteria for generating alert data. Examples of search criteria for security incidents and security events are shown.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Multiple-record, custom field Splunk alerts, ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Multi-record, custom field Splunk alert examples

When you are creating multiple record Splunk alerts with custom fields, you need to define search criteria for generating alert data. Examples of search criteria for security incidents and security events are shown.

## Security incident search

For a security incident, this criteria builds a search to fill in columns in the security incident table.

```
host=Development source="/CodeArchive/password/password_decrypt.cpp" |
eval contact_type="Monitoring" |
eval cmdb_ci=host |
eval subcategory="Sensitive Data Monitoring" |
eval description=_raw |
eval source_ip=found_ip
```

## Security event search

For a security event, this is the same search, but it populates Event fields instead. If this event is turned into a security incident, and any fields that do not exist in the event are populated, they are transferred to the security incident. Otherwise, they remain in the additional information field of the event and alert.

```
host=Development source="/CodeArchive/password/password_decrypt.cpp" |
eval type="Monitoring" | 
eval node=host | 
eval source=source
eval subcategory="Sensitive Data Monitoring" | 
eval description=_raw | 
eval source_ip=found_ip 
```

**Note:** The search criteria you use will add as many records as are found in the search. It may add 5 or 10,000,000,000 records. So this is NOT a recommended method for the bulk tranfer of data. The intent of this method is to add one record per REST call into the ServiceNow instance.

