---
title: Configure Splunk Enterprise Security settings
description: Use the Splunk Enterprise Security \(ES\) settings to modify the preset configurations and their values as per your requirements.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Install and configure, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Splunk Enterprise Security settings

Use the Splunk Enterprise Security \(ES\) settings to modify the preset configurations and their values as per your requirements.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  Navigate to **All** &gt; **Splunk ES Integration** &gt; **Splunk ES Settings**.

2.  On the form, fill the fields.

<table id="table_qnf_rch_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enforce a limit on the number of notable events that can be aggregated to a single incident.

</td><td>

Option to enforce a limit on the number of your notable events that you want to aggregate to a single incident.By default, the value is set as 100.

</td></tr><tr><td>

Enforce a limit on the number of security incidents that can be created in a 24-hour period.

</td><td>

Option to enforce a limit on the number of security incidents that can be created in a period of 24 hours.By default, the value is set as 1000.

</td></tr><tr><td>

Enforce a limit on the number of values to parse in each field received from Splunk.

</td><td>

Option to enforce a limit on the number of values that you want to parse for each field received from Splunk.By default, the value is set as 1000.

</td></tr><tr><td>

Number of correlation rules to pull from Splunk.

</td><td>

Option to define the number of correlation rules to retrieve from Splunk.By default, the value is set as 500.

</td></tr><tr><td>

The Time-to-Live parameter for Splunk search job in seconds.

</td><td>

Option to define the Time-to-Live parameter for the Splunk search in the form of seconds.By default, the value is set as 600.

</td></tr><tr><td>

Number of notable types to batch in one search.

</td><td>

Option to define the total number of notable types that you want batch in a single search.By default, the value is set as 20.

</td></tr><tr><td>

Number of days to retain the Splunk search job metadata in ServiceNow

</td><td>

Option to define the number of days that you want to retain the Splunk search job metadata in ServiceNow.By default, the value is set as 30.

</td></tr><tr><td>

The delimiter character to split the values in field mappings.

</td><td>

Option to define the delimiter character to split the values in field mappings.By default, the value is set as \(,\).

</td></tr><tr><td>

Number of overlap minutes to add while fetching the events from Splunk \(to overcome the indexing delay from Splunk\)

</td><td>

Option to define the number of overlap minutes to add while retrieving the events from Splunk to overcome the indexing delay from Splunk.By default, the value is set as 30.

</td></tr><tr><td>

Pull updated notable events

</td><td>

Option to retrieve updated notable events.By default, the value is set as No.

</td></tr><tr><td>

Activate this setting to update existing Splunk source configurations for token based authentication support. You must update the integration configuration with token details after this setting is enabled.

</td><td>

Option to update existing Splunk source configuration to token based authentication support from an existing version.**Note:** After you upgrade to the new version, the token field would become unavailable. You must enable this setting to get the token-based authentication, after which you must update the integration configuration with token details.

 By default, the value is set as No.

</td></tr><tr><td>

Enable the check box to pull Closed Notables during ingestion.

</td><td>

Option to pull the closed events into the ServiceNow Splunk ES instance. If unchecked, only active events are pulled into the instance.By default, the value is set as No.

</td></tr></tbody>
</table>3.  Click **Save**.


