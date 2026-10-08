---
title: Equinix connector metrics
description: Reference for the power metrics collected at the cabinet level and the environmental metrics collected at the zone level by the Equinix pull connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/equinix-connector-metrics.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Equinix, metrics, reference]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Equinix connector metrics

Reference for the power metrics collected at the cabinet level and the environmental metrics collected at the zone level by the Equinix pull connector.

## Cabinet metrics

The connector collects the following power metrics for each cabinet in the account's facility hierarchy. The cabinet is identified in MetricBase by its Equinix level value, for example `SG3:03:070210:0308`.

|Metric|Description|
|------|-----------|
|`kw`|Real power draw, in kilowatts.|
|`kva`|Apparent power draw, in kilovolt-amperes.|
|`amps`|Current, in amperes.|
|`powerFactor`|The cabinet's power factor.|
|`percentageKva`|Current utilization as a percentage of the cabinet's contracted capacity. Values can exceed 100% for an oversubscribed cabinet.|
|`peakKvaLastSevenDays`|The highest apparent power reading recorded over the previous seven days.|
|`peakKvaLastSevenDaysPercentage`|The seven-day peak apparent power as a percentage of the cabinet's contracted capacity.|
|`primaryKva`|Apparent power drawn from the primary feed.|
|`redundantKva`|Apparent power drawn from the redundant feed.|
|`cabinetRating`|The cabinet's contracted power capacity, in kilovolt-amperes.|

## Zone metrics

The connector collects the following environmental metrics for each zone in the account's facility hierarchy. The zone is identified in MetricBase by its Equinix zone label, for example `SG3:3:03:HALL7:Z1`.

|Metric|Description|
|------|-----------|
|`Temperature`|Ambient temperature for the zone, in degrees Celsius.|
|`Humidity`|Relative humidity for the zone.|

## System alerts

The connector also retrieves system alerts for each account and forwards them as events. Alert retrieval is paginated, so accounts with many active alerts are collected across multiple requests rather than truncated at the first page.

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[Configure the Equinix pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-equinix.md)

