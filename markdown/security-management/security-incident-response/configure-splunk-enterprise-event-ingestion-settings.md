---
title: Configure Splunk Enterprise Event Ingestion settings
description: Use the Splunk Enterprise Event Ingestion settings to modify the preset configurations and their values as per your requirements.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Splunk Enterprise Event Ingestion settings

Use the Splunk Enterprise Event Ingestion settings to modify the preset configurations and their values as per your requirements.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  Navigate to **All** &gt; **Splunk Integration** &gt; **Splunk Integration Settings**.

2.  On the form, fill the fields.

<table id="table_qnf_rch_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum number of alerts to be displayed in the profile creation.sn\_sec\_splunk\_v2.max\_alerts\_to\_display

</td><td>

Option to define the maximum number of alerts that you want to display while creating an event profile.By default, the value is set as 500.

</td></tr><tr><td>

Maximum number of security incidents to be created in one day.sn\_sec\_splunk\_v2.max\_si\_per\_day

</td><td>

Option to define the maximum number of security incidents that can be created in one day.By default, the value is set as 1000.

</td></tr><tr><td>

Maximum number of events to fetch from Splunk per call.sn\_sec\_splunk\_v2.max\_events\_per\_call

</td><td>

Option to define the maximum number of events to retrieve from Splunk for each call.By default, the value is set as 100.

</td></tr><tr><td>

The number of days an item remains in the queue table after completing/erroring for information or debugging purposes.sn\_sec\_splunk\_v2.queue\_item\_expire

</td><td>

Option to define the number of days for an item to remain in the queue table after completion or error occurrence due to information or debugging purposes.By default, the value is set as 14.

</td></tr><tr><td>

Number of days to retain the event import, event to task and fired alerts data.sn\_sec\_splunk\_v2.retention\_period

</td><td>

Option to determine the number of days that you want to retain the event import, event to task, and fired alerts data.By default, the value is set as 30.

</td></tr><tr><td>

Activate this setting to update existing Splunk source configurations for token based authentication support. You will need to update the integration configuration with token details once this setting is enabled.sn\_sec\_splunk\_v2.upgrade\_existing\_tile

</td><td>

Option to update existing Splunk source configuration to token based authentication support from an existing version.**Note:** After you upgrade to the new version, the token field would become unavailable. You need to enable this setting to get the token based authentication, after which you need to update the integration configuration with token details.

 By default, the value is set as No.

</td></tr><tr><td>

Logging level - debug, info, warn, error.sn\_sec\_splunk\_v2.logging.verbosity

</td><td>

Option to set the logging level \(debug, info, warn, or error\)

</td></tr><tr><td>

Splunk search time to live in seconds.sn\_sec\_splunk\_v2.sid\_ttl

</td><td>

Option to set the time in seconds that Splunk search results are retained. By default, the value is set as 14.

</td></tr><tr><td>

Number of overlap minutes to add while fetching the events from Splunk\(to overcome indexing delay from Splunk\).sn\_sec\_splunk\_v2.overlap\_time

</td><td>

Option to specify additional minutes to overlap when fetching events from Splunk, helping to account for indexing delays. By default, the value is set as 0.

</td></tr><tr><td>

Alert rule batch size to be used for firing Splunk search queries during ingestion.sn\_sec\_splunk\_v2.rules\_batch\_size

</td><td>

Option to set the batch size for firing Splunk search queries during ingestion.By default, the value is set as 50.

</td></tr><tr><td>

Events Limit per triggered alert to handle spike.sn\_sec\_splunk\_v2.spike\_events\_limit

</td><td>

Option to limit the number of events processed per triggered alert, helping to manage spikes in event volume.By default, the value is set as 1000.

</td></tr><tr><td>

The delimiter character to split the values in field mappings.sn\_sec\_splunk\_v2.delimiter

</td><td>

Option to specify the delimiter character used to split values in field mapping.

</td></tr></tbody>
</table>3.  Select **Save**.


**Parent Topic:**[Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-install-and-configure.md)

