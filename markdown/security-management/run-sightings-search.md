---
title: Run a Sightings Search
description: Determine the prevalence of a threat over time or test remediation or eradication efforts. You can select individual or multiple observables and the date range for your search from a security incident. Results are included in the Security Incident Observables related list.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create sightings search configuration records, Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Run a Sightings Search

Determine the prevalence of a threat over time or test remediation or eradication efforts. You can select individual or multiple observables and the date range for your search from a security incident. Results are included in the **Security Incident Observables** related list.

## Before you begin

Role required: sn\_si.analyst

## About this task

The Sightings Search capability has a flow, [Security Operations Integration - Sightings Search Flow](../../security-operations-integrations/task/secops-integration-sightings-search-workflow.md), that executes the sightings search. This flow accepts a list of observables, finds any implementing capabilities, creates the queries based on Sightings Search Configurations, and executes the searches based on the configured flow.

**Note:** An active implementation must be configured. Sightings Search supports Elasticsearch, Splunk, McAfee ESM, HPE ArcSight Logger, and QRadar incident enrichment. If no implementations are available, capability actions, such as **Run Sightings Search**, are not displayed in product menus.

## Procedure

1.  Navigate to a security incident.

2.  Click the **Show IoC** related link.

3.  Select **Observables** from the Related List tab.

4.  Select the observables you want to perform a sightings search on.

5.  Click **Run Sightings Search** in the **Actions on selected rows...** drop-down menu.

    ![Observables](../image/RunSightingsSearch.png)

    The Run Sightings Search dialog box opens.

    ![Run Sighting Search dialog box](../image/SightingsSearchDialogBox.png)

    **Note:** Values entered in the dialog box overwrite capability configuration values for this run.

6.  Choose the number of days or a date range to search for data.

<table id="choicetable_cgw_qxn_qz"><tbody><tr><td id="d410335e155">

**Last**

</td><td>

The number of hours or days prior to the creation of the incident to search. The default is 7 days. The limit is 99 hours or days.

</td></tr><tr><td id="d410335e167">

**between**

</td><td>

Range of dates to search. Default dates are:-   The date and time the incident was opened.
-   The date and time seven days prior to the opening of the incident.


</td></tr></tbody>
</table>    **Note:** **Last** is the number of hours or days prior to the creation of the incident to search. The default is 7 days. The limit is 99 hours or days.

7.  Click **Search**.

    A Sightings Search record is created. Aggregate and associated sightings data are displayed in the security incident under the **Sightings Search Results** and **Sightings Search Details** tabs.

    **Note:** Sightings search results data can be shared with Trusted Security Circle, with the exception of raw data in the case of implementations configured to include raw data.

    |Result|Description|
    |------|-----------|
    |Number|The identifier for the sightings search.|
    |Observable count|Number of observables searched for by query.|
    |Internal sightings|Count of internal sightings.|
    |External sightings|Count of external sightings. \(Received from threat sharing.\)|
    |Matched configuration items|Count of configuration items that matched an existing record in your cmdb for each observable found in your environment.|
    |Start date range|Time to start looking for sightings.|
    |End date range|Time to stop looking for sightings.|
    |Updated|Date and time of the last modification.|

    Note: If the implementation used for the sightings search is configured to include raw data, and at least one sighting is found, an attachment containing raw data samples appears at the top of the security incident.

    |Detail|Description|
    |------|-----------|
    |Sighting search|The identifier for the sightings search.|
    |Observable|Observable searched for by query.|
    |Observable type|Type of observable searched for by query.|
    |Internal sightings|Aggregated count of internal sightings.|
    |External sightings|Aggregated count of external sightings. \(Received from threat sharing.\)|
    |Updated|Date and time of the last modification.|


**Parent Topic:**[Create sightings search configuration records](../../security-incident-response/task/sightings-search-configurations.md)

