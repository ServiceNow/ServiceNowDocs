---
title: TISC integration with Splunk
description: The integration between the Threat Intelligence Security Center \(TISC\) and Splunk lets you filter and pull relevant threat intelligence observables data into Splunk.In Splunk, you can use this data to generate security alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/splunk-observables-enrichment-integration.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [servicenow, splunk, tisc, observables, enrichment integration]
breadcrumb: [TISC add-on for Splunk overview, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# TISC integration with Splunk

The integration between the Threat Intelligence Security Center \(TISC\) and Splunk lets you filter and pull relevant threat intelligence observables data into Splunk.In Splunk, you can use this data to generate security alerts.

Role required: Splunk admin

Using the TISC add-on application, you can configure the interval at which you can pull observables from ServiceNow TISC instance.

This interval determines how frequently the application can make requests to ServiceNow and retrieve the observables data. Define and apply filters to specify the observables to pull from the ServiceNow TISC instance.

After the observables are pulled from ServiceNow, the observables data is stored in Splunk Key-Value Store \(KV Store\) and you can further write the correlation rules over the set of observables retrieved.

**Parent Topic:**[TISC add-on for Splunk overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-addon-splunk.md)

