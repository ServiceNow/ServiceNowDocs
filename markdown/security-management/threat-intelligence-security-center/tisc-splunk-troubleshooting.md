---
title: Troubleshoot the TISC add-on in Splunk
description: Enable debug logging on the add-on, view the resulting log entries in Splunk, and check input execution status from the Input Metadata Lookup KV store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-splunk-troubleshooting.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
keywords: [tisc, splunk, troubleshoot, debug, logging, input metadata lookup]
breadcrumb: [TISC add-on for Splunk overview, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Troubleshoot the TISC add-on in Splunk

Enable debug logging on the add-on, view the resulting log entries in Splunk, and check input execution status from the Input Metadata Lookup KV store.

## Before you begin

Role required: Splunk admin

The TISC add-on is installed and configured. See [Configure TISC add-on in Splunk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-configure-splunk.md).

## About this task

Use this procedure when an input is not pulling observables from TISC as expected, when records appear stale or missing in the KV store, or to inspect the execution history of a configured input.

## Procedure

1.  From the add-on, open the **Configuration** page and select the **Logging** tab.

2.  Set **Log level** to **DEBUG** and select **Save**.

    Subsequent input runs provide verbose debug statements that can be searched in Splunk.

3.  To view the debug entries, run a search in Splunk that scopes to the add-on's internal logs and filters on the `DEBUG` level.

    For example:

    ```
    index=_internal sourcetype=splunkd "TA-threat-intelligence-security-center" log_level=DEBUG
    ```

    Refine the search further by input name or time range to narrow the results to a specific run.

4.  To verify the execution status of each input, look up the `inputs_metadata_lookup` KV store.

    ```
    | inputlookup inputs_metadata_lookup
    ```

    The lookup contains one record per configured input. Each record captures the following fields:

    |Field|Description|
    |-----|-----------|
    |configuration\_name|Name of the account configuration associated with the input.|
    |historical\_fetch\_date|Start date used the last time **Enable Historical Fetch** was set on the input. Empty if a historical fetch has not been run.|
    |historical\_fetch\_pending|Status indicating whether a historical fetch is pending.|
    |input\_name|Name of the input.|
    |last\_successful\_execution\_time|Timestamp of the most recent successful execution of the input.|
    |status|Outcome of the most recent execution: `success` or `failure`.|
    |status\_message|Detail message for the most recent execution, including error context if the run failed.|
    | |.|

5.  After you have diagnosed the issue, return to the **Logging** tab and reset **Log level** to **INFO** to stop emitting verbose entries.


## Result

You have collected the diagnostic information needed to identify why an input failed or returned unexpected results. Provide the relevant log entries and the input's metadata record when raising a support case or working with the add-on team.

**Parent Topic:**[TISC add-on for Splunk overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-addon-splunk.md)

**Related topics**  


[Configure TISC add-on in Splunk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-configure-splunk.md)

[Data storage in Splunk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-storage-splunk.md)

[TISC add-on for Splunk overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-addon-splunk.md)

