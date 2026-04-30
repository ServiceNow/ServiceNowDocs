---
title: Configuration settings
description: Use this option to modify the IBM QRadar ingestion integration default system properties.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configuration settings

Use this option to modify the IBM QRadar ingestion integration default system properties.

To modify the system properties, log in as a user with the `sn_si.admin` role and navigate to **IBM QRadar Integration** &gt; **IBM QRadar Integration Settings**.

<table id="table_xpj_dv5_nnb"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enforce a limit on number of security incidents that can be created in 24 hour period.sn\_sec\_qradar.max\_si\_per\_day

</td><td>

Specify the maximum number of security incidents that can be created in 24 hours.

-   Type: integer
-   Default value: 1000

</td></tr><tr><td>

Enforce a limit on number of offenses that can be aggregated to a single incident.sn\_sec\_qradar.max\_aggregation\_per\_si

</td><td>

The offense aggregation limit for a security incident. For example, if there are 102 offenses, the first 100 offense are aggregated to security incident\_1 and the remaining 2 to security incident\_2.

-   Type: integer
-   Default value: 100

</td></tr><tr><td>

This property sets the time period of AQL to fetch recent event/flows for a particular offense.sn\_sec\_qradar.on\_demand\_recent\_days\_limit

</td><td>

Specify the number of days to fetch recent events or flows for a particular offense.

-   Type: integer
-   Default value: 7

</td></tr><tr><td>

This property limits the number of recent events fetched for a particular offense.sn\_sec\_qradar.on\_demand\_event\_limit

</td><td>

Specify the number of events that are retrieved for an offense. The most recent events are retrieved first based on the event timestamp.

-   Type: integer
-   Default value: 100

</td></tr><tr><td>

This property limits the number of recent flows fetched for a particular offense.sn\_sec\_qradar.on\_demand\_flow\_limit

</td><td>

Specify the number of flows that are retrieved for an offense. The most recent flows are retrieved first based on the flow timestamp.

-   Type: integer
-   Default value: 100

</td></tr><tr><td>

This property sets the timeout value\(seconds\) for the AQL which fetches recent flows/events for a particular offense.sn\_sec\_qradar.on\_demand\_timeout

</td><td>

-   Type: integer
-   Default value: 300

</td></tr><tr><td>

Search IDs timeout\(seconds\) for records in queue for polling AQLs of an offense.sn\_sec\_qradar.sid\_ttl

</td><td>

The AQL's time out for an offense in the queue before creating a security incident. For example, if there are 90 offenses, the first 50 offenses are processed for AQL data in the first batch, and the remaining 40 offenses in the subsequent batch in the same polling interval.

-   Type: integer
-   Default value: 300

</td></tr><tr><td>

Threshold to control the number of searches that can be running in IBM QRadar at a time which is triggered by the integration scheduled

 job.sn\_sec\_qradar.records\_threshold\_in\_que\_for\_aql

</td><td>

Specify the number of offenses that you fetch in a single batch in a polling interval.

-   Type: integer
-   Default value: 50

</td></tr><tr><td>

This is the number of days for integration tables clean up.

 sn\_sec\_qradar.queue\_item\_expire

</td><td>

The following are the integration tables:

-   sn\_sec\_qradar\_events - IBM QRadar Events
-   sn\_sec\_qradar\_flows - IBM QRadar Flows
-   sn\_sec\_qradar\_offense\_updates - IBM QRadar Offense Updates
-   sn\_sec\_qradar\_offense\_to\_task - IBM QRadar Offense to Task
-   Type: integer
-   Default value: 30

</td></tr><tr><td>

Offense limit per scheduled job runs per profile either in one-time retrieval or on-going ingestion.

 sn\_sec\_qradar.max\_offense\_limit\_per\_run

</td><td>

Specify the number of offenses that you fetch into the ServiceNow AI Platform in a single retrieval.

-   Type: integer
-   Default value: 1000

</td></tr><tr><td>

Set this property to activate the Offense Updates feature.

 sn\_sec\_qradar.get\_offense\_updates

</td><td>

**Note:** Enabling this setting may cause a delay in creating a security incident.

-   Type: true\| false
-   Default value: false

</td></tr><tr><td>

Enables adding overlapping interval while fetching offenses from QRadar.sn\_sec\_qradar.allow\_overlapping

</td><td>

Option to enable the use of an overlapping time window when fetching offenses from IBM QRadar. When enabled, the system includes a small overlap between consecutive polling intervals to ensure that no offenses are missed due to timing delays or ingestion latency.

-   Type: true\| false
-   Default value: false

</td></tr><tr><td>

Logging Level-debug,info,warn,error.sn\_sec\_qradar.logging.verbosity

</td><td>

Logging verbosity level for the QRadar integration. Supported values include debug, info, warn, and error.

-   Type: Character
-   Default value: debug

</td></tr><tr><td>

Time in minutes to be added as overlap interval.sn\_sec\_qradar.overlapping\_time

</td><td>

Number of minutes to be added as an overlap interval when fetching offenses from IBM QRadar.-   Type: integer
-   Default value: 30

</td></tr><tr><td>

Number of rules that will be included in a single cell.sn\_sec\_qradar.rules\_batch\_size

</td><td>

Specify the maximum number of correlation rules that will be grouped and sent together in a single request to IBM QRadar during offense polling.This setting will help control batching behavior and performance. Lower value result in more API calls with smaller payloads, while higher value reduces the number of API calls and increases the size of each request.

Adjust this value based on QRadar performance and API limits.

-   Type: integer
-   Default value: 50

</td></tr><tr><td>

Fetch ADE Rulessn\_sec\_qradar.fetch\_ade\_rules

</td><td>

Option to ingest ADE Rules in IBM QRadar Rules list.Fetch ADE Rules will fetch Anomaly Rules created in IBM QRadar.

-   Type: true\| false
-   Default value: false

</td></tr></tbody>
</table>Any modified integration settings will be applied during the next polling interval as defined in the profile.

