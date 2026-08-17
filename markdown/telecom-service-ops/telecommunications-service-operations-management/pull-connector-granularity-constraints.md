---
title: Pull connector granularity constraints
description: Each connector type enforces minimum and maximum values for the granularity and metrics collection schedule fields on the connector instance form. The connector instance form rejects values outside the supported range.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/pull-connector-granularity-constraints.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Pull connector granularity constraints

Each connector type enforces minimum and maximum values for the granularity and metrics collection schedule fields on the connector instance form. The connector instance form rejects values outside the supported range.

|Connector|API / metric type|Field|Constraint|
|---------|-----------------|-----|----------|
|Meraki|All metrics|Granularity|Granularity must be a positive multiple of 60 seconds and must divide evenly into the metrics collection schedule.|
|Uplink loss and latency|Granularity|Maximum 5 minutes|
|Device performance|Metrics collection schedule|30 minutes \(1800 seconds\) is the default collection window. If a lower value is set, an error is shown and the value is reset to the default of 1800 seconds.|
|Fortinet|Interface logs|Metrics collection schedule|10 minutes \(600 seconds\) is the default collection window. If a higher value is set, an error is shown and the value is reset to the default of 600 seconds.|

## Field descriptions

|Field|Description|
|-----|-----------|
|Granularity|Time resolution of each sample returned per API call. Controls how finely the source system data is sliced within a polling cycle.|
|Metrics collection schedule|Frequency at which the connector polls the source system API. Also referred to as the poller iteration window.|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

