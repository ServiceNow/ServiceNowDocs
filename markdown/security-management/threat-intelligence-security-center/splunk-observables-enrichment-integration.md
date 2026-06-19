---
title: TISC integration with Splunk
description: The integration between the Threat Intelligence Security Center \(TISC\) and Splunk enables users to filter and pull in relevant threat intelligence observables data into Splunk. Within the Splunk, the users can use this data to generate security alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/splunk-observables-enrichment-integration.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [servicenow, splunk, tisc, observables, enrichment integration]
breadcrumb: [TISC add-on for Splunk overview, TISC Security Tools Integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# TISC integration with Splunk

The integration between the Threat Intelligence Security Center \(TISC\) and Splunk enables users to filter and pull in relevant threat intelligence observables data into Splunk. Within the Splunk, the users can use this data to generate security alerts.

Role required: Splunk admin

Using the TISC add-on application, you can configure the interval at which you can pull observables from ServiceNow TISC instance.

This interval determines how frequently the application can make requests to ServiceNow and retrieve the observables data. Also, you can define and apply filters to specify the observables that you want to pull from the ServiceNow TISC instance.

Once the observables are pulled from ServiceNow, the observables data is stored in Splunk KV Store \(Key-Value Store\) and you can further write the correlation rules over the set of observables which were pulled in.

**Parent Topic:**[TISC add-on for Splunk overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-addon-splunk.md)

