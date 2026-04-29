---
title: Components installed with Threat Intelligence Security Center
description: Several types of components are installed when you download and activate the Threat Intelligence Security Center application, including user roles and properties.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Reference, Threat Intelligence Security Center, Security Operations]
---

# Components installed with Threat Intelligence Security Center

Several types of components are installed when you download and activate the Threat Intelligence Security Center application, including user roles and properties.

## Properties installed

Role required: sn\_sec\_tisc.admin

Users with the Security Administrator \[sn\_sec\_tisc.admin\] role can modify them.

<table id="table_q4b_y2c_ks"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td colspan="2">

**Properties for Threat Intelligence Security Center**

</td></tr><tr><td>

This will disable all the correlation rules. If we just need to disable selected correlation rules, use "active" field on correlation rule instead. sn\_sec\_tisc.disable\_correlation\_rules

</td><td>

-   **Type**: true \| false
-   **Default value**: false

</td></tr><tr><td>

This property is used to enable/disable processing of aggregates in threat score calculator feature.sn\_sec\_tisc.aggregates\_for\_calculator

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td>

The number of rows of raw data that will be saved when a Sighting Search is performed. Range 0 - 100sn\_sec\_tisc.sighting\_search\_raw\_data\_rows

</td><td>

-   **Type**: integer
-   **Default value**: 50

</td></tr><tr><td>

Associate Sighting Search results with CIs in the CMDB.sn\_sec\_tisc.associate\_ci\_with\_sighting\_search

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td>

This will control whether URLs from lists will be defanged or notsn\_sec\_tisc.sn\_sec\_tisc\_case.defang\_record\_list\_urls

</td><td>

-   **Type**: true \| false
-   **Default value**: false

</td></tr><tr><td>

This property will enable the MITRE Technique\(s\), to be rolled up to case\(s\) from the associated objects or security incidents automatically.sn\_sec\_tisc.auto\_rollup\_mitre\_data

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td>

If true, shows all tactics \(including the tactics which doesn't have any techniques associated to the case\) for the MITRE lists rendered in the report.sn\_sec\_tisc.show\_all\_tactics\_reporting

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td>

Sys ID of the email client template for the Case \(sn\_sec\_tisc\_case\) table which will be used in share report.sn\_sec\_tisc.reporting\_email\_template\_sn\_sec\_tisc\_case

</td><td>

-   **Type**: string
-   **Default value**: b55e22c54324021060eee0ea78b8f2df

</td></tr><tr><td>

Default TLP level is applied when creating a new record. If not set manually on the form, this value will be used.sn\_sec\_tisc.tlp\_default\_value

</td><td>

-   **Type**: choice list
-   **Default value**: 955c9e5543d35110baf06e434ab8f2fb

</td></tr><tr><td>

Logging level-debug,info,warn,errorsn\_sec\_tisc.logging.verbosity

</td><td>

-   **Type**: choice list
-   **Default value**: info

</td></tr><tr><td colspan="2">

**Properties for Threat Intelligence Feeds**

</td></tr><tr><td>

Maximum time in seconds an outbound HTTP connection waits to fetch TAXII collection datasn\_sec\_tisc.taxii.http.max\_timeout

</td><td>

-   **Type**: integer
-   **Default value**: 300

</td></tr><tr><td>

Maximum number of objects retrieved in one REST call from a TAXII server \(Applicable only for TAXII versions 2.0 and 2.1\)sn\_sec\_tisc.taxii.max\_page\_size

</td><td>

-   **Type**: integer
-   **Default value**: 5000

</td></tr><tr><td>

Maximum number of retries for a failed TAXII2. X REST callsn\_sec\_tisc.taxii2.retry\_count

</td><td>

-   **Type**: integer
-   **Default value**: 3

</td></tr><tr><td>

Maximum number of objects retrieved in one REST call from Cyware TAXII serversn\_sec\_tisc.cyware\_taxii.max\_page\_size

</td><td>

-   **Type**: integer
-   **Default value**: 1000

 **Note:** Specifies the page size used when fetching data from TAXII collections related to the Cyware TAXII Feed.

For all other TAXII collections, the page size retrieved from the TAXII collection defaults to the value defined in the corresponding property: `sn_sec_tisc.taxii.max_page_size`.

</td></tr><tr><td>

Number of records to fetch at a time from CrowdStrike. Higher the number, more the memory would consumed for processing the payload.sn\_sec\_tisc.crowdstrike\_api\_limit

</td><td>

-   **Type**: integer
-   **Default value**: 1000

</td></tr><tr><td>

Denotes the number of indicators to be pulled in a single API call.**Note:** This is applicable only when the integration doesn't find the necessary present in the system.

sn\_sec\_tisc.crowdstrike\_indicator\_batch\_size

</td><td>

-   **Type**: integer
-   **Default value**: 1000

</td></tr><tr><td>

Denotes the number of actors to be pulled in a single API call.**Note:** This is applicable only when the integration doesn't find the necessary present in the system.

sn\_sec\_tisc.crowdstrike\_actor\_batch\_size

</td><td>

-   **Type**: integer
-   **Default value**: 1000

</td></tr><tr><td>

Denotes the number of reports to be pulled in a single API call.**Note:** This is applicable only when the integration doesn't find the necessary present in the system.

sn\_sec\_tisc.crowdstrike\_report\_batch\_size

</td><td>

-   **Type**: integer
-   **Default value**: 50

</td></tr><tr><td>

The allowed total of offset and limit from CrowdStrike API.sn\_sec\_tisc.crowdstrike\_offset\_limit\_total

</td><td>

-   **Type**: integer
-   **Default value**: 50000

</td></tr><tr><td>

**Properties for Tagging Rules**

</td><td>

 

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td colspan="2">

**Properties for REST APIs**

</td></tr><tr><td>

Defines the maximum page size \(max number of observables returned as part of the response\) for Observables Fetch API. Not recommended to increase to high value as it may affect API response time.sn\_sec\_tisc.api\_maximum\_page\_size\_limit

</td><td>

-   **Type**: integer
-   **Default value**: 1000

</td></tr><tr><td>

Defines the maximum number of observables that can be sent in the request body for Observables Add API. Not recommended to increase to high value as it may affect API response time.sn\_sec\_tisc.add\_obs\_api\_max\_records

</td><td>

-   **Type**: integer
-   **Default value**: 100

</td></tr><tr><td colspan="2">

**Properties for Webhooks**

</td></tr><tr><td>

Maximum number of events to send as part of one webhook request. The batch size will be limited to 2000 even if a higher value is set in this property.sn\_sec\_tisc.webhook\_max\_event\_batch\_size

</td><td>

-   **Type**: integer
-   **Default value**: 100

</td></tr><tr><td>

Number of times a failed request should be retried before marking it as error and moving on to next batch of events. The retry count will be limited to 10 even if a higher number is set in this property.sn\_sec\_tisc.webhook\_retry\_count

</td><td>

-   **Type**: integer
-   **Default value**: 100

</td></tr><tr><td>

Number of seconds to wait before re-attempting a failed batch. This will exponentially increase based on the retry count. For eg, if retry\_count is 3 and retry\_interval is 30, retries are fired after 30, 60 and 120s. The initial retry interval will be limited to 300 seconds even if a higher value is set in this property.sn\_sec\_tisc.webhook\_retry\_interval

</td><td>

-   **Type**: integer
-   **Default value**: 30

</td></tr><tr><td>

Ignore webhook events triggered by threat score re-applysn\_sec\_tisc.webhook\_ignore\_threat\_score\_reapply

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td colspan="2">

**Properties for Investigation Canvas**

</td></tr><tr><td>

Setting the value to true adds new nodes to the top left corner; false adds them to the center of the canvas.sn\_sec\_tisc.canvas\_suspend\_reLayout

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td colspan="2">

**Properties for export in CTI formats**

</td></tr><tr><td>

Maximum number of rows that can be exported to a STIX 2.1 filesn\_sec\_tisc.stix\_export\_limit

</td><td>

-   **Type**: integer
-   **Default value**: 10000

</td></tr><tr><td>

Include Journal type fields in export file.sn\_sec\_tisc.export\_journal\_fields

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td colspan="2">

**Properties for Threat Intelligence Sharing**

</td></tr><tr><td>

Enables or disables case sensitive for applying redaction for shared intel. \(By default, the value will be false implying that the redaction will be case insensitive. Note: Changing the value of this property from false to true or true to false will DELETE all the data from redaction category as well as values table.\)sn\_sec\_tisc.case\_sensitive\_for\_redaction

</td><td>

-   **Type**: true \| false
-   **Default value**: false

</td></tr><tr><td>

Maximum number of rows allowed in the redaction upload file.sn\_sec\_tisc.max\_redaction\_rows\_import

</td><td>

-   **Type**: integer
-   **Default value**: 10000

</td></tr><tr><td>

Title of outbound TAXII serversn\_sec\_tisc.taxii\_server\_discovery\_api\_title

</td><td>

-   **Type**: string
-   **Default value**: ServiceNow TAXII Server

</td></tr><tr><td>

Description of outbound TAXII serversn\_sec\_tisc.taxii\_server\_discovery\_api\_description

</td><td>

-   **Type**: string
-   **Default value**: Discovery endpoint for sharing cyber threat intelligence via TAXII

</td></tr><tr><td>

Title of outbound TAXII server default API rootsn\_sec\_tisc.taxii\_server\_api\_root\_title

</td><td>

-   **Type**: string
-   **Default value**: ServiceNow TAXII Server

</td></tr><tr><td>

Description of outbound TAXII server default API rootsn\_sec\_tisc.taxii\_server\_api\_root\_description

</td><td>

-   **Type**: string
-   **Default value**: SAPI root endpoint for sharing cyber threat intelligence via TAXII

</td></tr><tr><td>

Default page size of TAXII Server API responsesn\_sec\_tisc.taxii\_server\_api\_response\_page\_limit

</td><td>

-   **Type**: integer
-   **Default value**: 100

</td></tr><tr><td>

Maximum number of records that can be added to a outbound TAXII server collectionsn\_sec\_tisc.taxii\_server\_collection\_record\_limit

</td><td>

-   **Type**: integer
-   **Default value**: 10000

</td></tr><tr><td>

The maximum number of entities that can be added to a TAXII collection in a single "Add to TAXII Collection" request. The system enforces a hard limit of 10,000 entities per request, regardless of any higher configured value.sn\_sec\_tisc.add\_to\_taxii\_collection\_entity\_threshold

</td><td>

-   **Type**: integer
-   **Default value**: 1000

</td></tr><tr><td colspan="2">

**Properties for Tagging Rules**

</td></tr><tr><td>

Enables or disables case sensitive matching of keywords or regex n tagging rules \(By default this is unselected \(No\) meaning matches are case-sensitive\).sn\_sec\_tisc.case\_sensitive\_for\_tagging\_rules

</td><td>

-   **Type**: true \| false
-   **Default value**: false

</td></tr></tbody>
</table>## Scheduled Jobs

The following table describes the scheduled jobs:

|Job|Description|
|---|-----------|
|Aggregate Indicator Source Records|Aggregates Indicator source records.|
|Aggregate Object Source Records|Aggregates Object source records.|
|Aggregate Observable Source Records|Aggregates Observable source records.|
|Cleanup of Stale Imports|Cleans up stale import job records.|
|Cleanup of unused new nodes of canvas|Cleans up unused new nodes of canvas.|
|Cleanup Secure File Download Records|Cleans up secure file download records.|
|De-duplicate Indicator Source Records|Deduplicates Indicator source records.|
|De-duplicate Object Source Records|Deduplicates Object source records.|
|De-duplicate Observable Source Records|Deduplicates Observable source records.|
|Inactivate Expired Indicators|Inactivates expired indicator records.|
|Inactivate Expired Objects|Inactivates expired object records.|
|Inactivate Expired Observables|Inactivates expired observable records|
|Migrate Data from TI to TISC|Processes pending migration job run records|
|Populate aggregated records for indicator source records|Identifies parent aggregated record for newly created indicator source records|
|Populate aggregated records for object source records|Identifies parent aggregated record for newly created object source records.|
|Populate aggregated records for observable source records|Identifies parent aggregated record for newly created observable source records.|
|Populate TISC Reference in TI|Populates reference of TISC aggregated observable in TI observable record.|
|Process Approved Imports|Processes approved import jobs.|
|Process Imported MISP Dsm Queue Records|Processed staged MISP feed ingestion queue records.|
|Process Imported MISP Indicator Import Queue Records|Processes staged MISP data ingested from import intelligence|
|Process Imported STIX Import Queue Records|Processes staged STIX data ingested from import intelligence|
|Process Imported STIX Import Queue Records - Ingestion|Processes staged STIX data ingested from threat feeds.|
|Process Pending Case Artifacts Migration|Migrates case artifacts from Threat intelligence application to Threat Intelligence security center.|
|Process pending threat source ingestion Queue Records|Processes pending source ingestion queue records.|
|Process Queued Entities For Threat Score Calculator|processes pending threat calculator queue entries|
|Process Queued MISP Dsm Queue Records|Processes queued MISP data ingested from threat feed|
|Process Queued MISP Indicator Import Queue Records|Processes queued MISP data ingested from import intelligence|
|Process Queued STIX Import Queue Records - Ingestion|Processes queued STIX data ingested from threat feeds.|
|Process Queued STIX Indicator Import Queue Records|Processes queued STIX data ingested from import intelligence|
|Process Webhook Queue|Processes pending webhook queue records.|
|Re-Aggregate Source Records|Re-aggregates source records for which aggregated records are deleted.|
|Remove filtered source record|Cleans up filtered source records|
|Resume CrowdStrike Integration Process Checker / Reprocess CrowdStrike Source Records|Resumes CrowdStrike feed integration runs waiting for rate limit / Reporcess source records for aggregating relationships|
|Sync False Positive Observables Count|Synchronizes observable false positive counts with flase positive counts per source|
|TISC Create Webhook Batches|Created batches for queued webhook queueu entries for processing|
|TISC Fire Webhooks|Executes pending webhook batches|
|Updating Relationship Archived Column|Updates relationship source and target records archival status|

