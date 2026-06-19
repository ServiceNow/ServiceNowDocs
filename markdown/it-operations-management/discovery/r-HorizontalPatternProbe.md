---
title: Horizontal Pattern probe
description: Discovery uses the Horizontal Pattern probe to launch patterns for horizontal discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/r-HorizontalPatternProbe.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Horizontal Pattern probe

Discovery uses the Horizontal Pattern probe to launch patterns for horizontal discovery.

The Horizontal Pattern probe works with the Horizontal Discovery sensor to enable Discovery to use patterns for discovery. When you see messages in the ECC Queue from this probe, they appear with the ECC queue name **Pattern Launcher**, followed by the name of the pattern. The probe contains a sensor named **Horizontal Discovery Sensor**, which performs the actual updates of the CMDB based on identification rules.

If you create your own device or process classifier and you want to use patterns for discovery, you must [specify this probe in the classifier record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c-UsingPatternsForHorizontalDiscovery.md). You don't need to modify this probe or the Horizontal Discovery sensor.

## Splitting payload

When Discovery uses patterns to discover certain devices such as load balancers or network switches, the MID Server can collect large amounts of data. To better handle this, the Horizontal Pattern probe splits the payload into chunks and create multiple ECC Queue records.

Payload splitting happens in two phases. First, the MID Server checks the total payload against size and count limits. The system checks the size limit first. Second, the MID Server evaluates each configuration item \(CI\) for the number of related items. When a CI has more related items than the chunk size, the system splits those items into separate ECC queue pages. Each page contains a copy of the parent CI with a subset of its related items.

When both phases interact, the number of ECC queue pages can grow significantly. For example, a network switch with 50,000 related items and a chunk size of 100 creates 500 ECC queue pages for that single CI.

The following MID Server properties control payload splitting.

|Property|Default value|Description|
|--------|-------------|-----------|
|mid.discovery.max\_total\_items\_size\_per\_page|3,145,728 bytes \(3 MB\)|Sets the maximum size limit of all items \(CIs, related items, relations, and references\) per ECC queue page. The system checks this threshold first.|
|mid.discovery.max\_ci\_count\_per\_page|500|Sets the maximum number of CIs per ECC queue page.|
|mid.discovery.max\_relation\_count\_per\_page|10,000|Sets the maximum number of relations per ECC queue page.|
|mid.discovery.max\_related\_count\_per\_page|100|Sets the maximum number of related items per chunk. Each chunk becomes a separate ECC queue page containing a copy of the parent CI.|
|mid.discovery.should\_minify\_pattern\_payload|false|Enables JSON minification for pattern payloads. When set to true, trims JSON whitespace from the pattern payload to reduce its size.|

## Tuning payload splitting

You can adjust MID Server properties to reduce the number of ECC queue pages that Discovery creates. The following table identifies common issues and the actions to address them.

|Issue|Action|Related property|
|-----|------|----------------|
|A CI with many related items creates an excessive number of ECC queue pages|Increase the related items chunk size|mid.discovery.max\_related\_count\_per\_page|
|Payload size is the splitting bottleneck|Increase the size limit and the MID Server JVM heap size|mid.discovery.max\_total\_items\_size\_per\_page|
|Payload size exceeds the limit but increasing the JVM heap size is not feasible|Enable payload minification to reduce the JSON payload size|mid.discovery.should\_minify\_pattern\_payload|
|A high CI count per page is causing splitting|Increase the CI count limit|mid.discovery.max\_ci\_count\_per\_page|
|A high relation count per page is causing splitting|Increase the relation count limit|mid.discovery.max\_relation\_count\_per\_page|

**Note:**

-   These properties are per MID Server. Apply changes to all MID Servers involved in the affected Discovery schedules.
-   If necessary, increase **mid.discovery.max\_total\_items\_size\_per\_page** and the MID Server JVM heap size accordingly. Setting these values too high can cause out-of-memory errors on the MID Server and instance nodes. Set values appropriate for your environment.
-   Setting **mid.discovery.should\_minify\_pattern\_payload** to true can reduce payload size without requiring heap size increase.
-   For environments where a CI has many related items, but fewer total CIs, the primary bottleneck is likely **mid.discovery.max\_related\_count\_per\_page**. Start by increasing that property.

**Parent Topic:**[List of Discovery probes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r_ListOfDiscoveryProbes.md)

