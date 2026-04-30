---
title: View RSS Feeds
description: A threat intelligence feed is a real-time, continuous data stream that gathers information related to cyber risks or threats. RSS Feeds provide an easy way to stay up to date with your favorite websites, such as blogs or latest cyber security news.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 7
breadcrumb: [TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# View RSS Feeds

A threat intelligence feed is a real-time, continuous data stream that gathers information related to cyber risks or threats. RSS Feeds provide an easy way to stay up to date with your favorite websites, such as blogs or latest cyber security news.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **RSS Feeds** &gt; **All RSS Feeds** object.

    **Note:** The ingested feeds can be browsed using this section but you cannot create new records.

4.  On the form, following fields are auto-populated.

    |Field|Description|
    |-----|-----------|
    |Title|Title of the RSS Feed.|
    |Description|Description that provides more details and context about the RSS feeds, including its purpose and key characteristics.|
    |Link|Indicates the link added to the RSS feeds.|
    |Source|RSS feed source from which this object record is created.|
    |Published Date|Date when the RSS feed is published.|
    |Author|Author for the RSS feed.|

5.  Click **Save**.

    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for this feed.|

<table id="table_ytw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Media URL

</td><td>

Indicates the media URL.

</td></tr><tr><td>

Feedback Comments URL

</td><td>

Link to the feedback comments.

</td></tr><tr><td>

Status

</td><td>

State of an RSS feed record in relation to its configured expiration period. This field supports tracking of ingested records.-   When a record is created through RSS feed ingestion, the application assigns an initial status based on its validity period.
-   The status changes automatically as the record approaches or reaches its expiration time.
**Note:** This field identifies whether records are still valid for analysis or have aged out based on data retention settings.

The **Status** field works with the **Expiration time** field and reflects the retention behavior defined by the feed's **Expiry days** configuration.

</td></tr><tr><td>

Expiration time

</td><td>

The **Expiration time** value is automatically calculated based on the configured **Expiry days** period for the feed. When records are ingested, the application sets the expiration time by adding the configured number of days to the record creation date.If the expiry period is not specified for an integration, the **Expiry period** field remains empty for the RSS feed record. As a result, the RSS feed record continues to remain active and does not expire.

**Note:**

For all feed integrations, the field configuration includes an Expiry days setting that defines the retention period for ingested data. Previously, records created through RSS feeds did not include expiration tracking.

For example, if the expiry period is set to 30 days, each ingested record receives an expiration time equal to the ingestion date plus 30 days.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |**TISC Tags**|
    |Select Tags|Select the tags that are associated with the vulnerability.|
    |Add Tags|Add new tags.|
    |**Taxonomies**|
    |Select Taxonomy|Select a Taxonomy that is associated with this vulnerability.|
    |Add Taxonomy Values|Add Taxonomy values that are associated with this vulnerability.|

    **RSS Feed Actions from the list view: Add TISC Tags**

    -   Select any RSS feed from the list view.
    -   Select **Add TISC Tags** to associate tags with the RSS feed record.
    -   Search and select the desired TISC tag.
    -   Select **Submit** to add the tag.

        A confirmation displays indicating that the tags are applied successfully.

    **RSS Feed Actions from the list view: Add Taxonomy**

    -   Select any RSS feed from the list view.
    -   Select **Add Taxonomy** to associate taxonomies with the RSS feed record.
    -   Search and select the desired TISC taxonomy value.
    -   Select **Submit** to add the taxonomies.

        A confirmation displays indicating that the tags &amp; taxonomy values are applied successfully.

    **RSS Feed Actions from the list view: Add to Case**

    -   Select any RSS feed from the list view.
    -   Select **Add to Case** to associate the RSS feed record with a case.
    -   Select the case\(s\).
    -   Select **Add** to add the case to the RSS feed record.

        A confirmation displays indicating that the selected records are added to case\(s\) successfully.

6.  Modify the feed details, if required.

7.  Navigate to the **TISC Tags &amp; Taxonomies** section.

    1.  In the **TISC Tags** related list, **Select TISC Tags** to add tags.

    2.  In the **Taxonomy** related list, **Select Taxonomy** to add taxonomies directly from the RSS feed form view.

8.  Select **Save** to apply the changes.

9.  Select **Add to Case** to associate the RSS feed record to a case directly from the form view.

10. Select **Delete** to delete the RSS feed, if required.


## What to do next

Use the **Related Records** section to view the detailed information about objects associated with the RSS feeds. Click any of related list to explore the linked records.

|Related Record|Description|
|--------------|-----------|
|MITRE Techniques|Lists the MITRE techniques related to RSS feeds.|
|Attack Patterns|List of attack patterns that are related to RSS feeds.|
|Campaigns|List the campaigns that are related to RSS feeds.|
|Courses of Action|Lists the courses of action related to RSS feeds.|
|Data Sources|Lists the data sources related to RSS feeds.|
|Data Components|Lists the data components related to RSS feeds.|
|Identities|Lists the identities that are related to RSS feeds.|
|Indicators|Lists the indicators that are related to RSS feeds.|
|Infrastructure|List the Infrastructure such as systems, software services, and any associated physical or virtual resources that are related to RSS feeds.|
|Intrusion Set|List the intrusion sets such as a set of adversarial behaviors and resources with common properties that are related to RSS feeds.|
|Locations|Lists the geographical locations associated to RSS feeds.|
|Malware|List the malware source records that are related to RSS feeds.|
|Malware Analysis|Lists the metadata and results of a particular static or dynamic analysis performed on a malware instance associated to RSS feeds.|
|Observables|List of observables related to RSS feeds.|
|Object Sightings|List of object sightings related to RSS feeds.|
|Observed Data|Lists the observed data that are cyber security related entities such as files, systems, and networks and associated with RSS feeds.|
|Threat Actors|List the threat actors that are related to RSS feeds.|
|Threat Events|List the threat events that are related to RSS feeds.|
|Threat Groupings|Lists the threat groupings as objects that have a shared context with RSS feeds.|
|Threat Notes|Lists the threat notes that convey information to provide further context or analysis that are associated with RSS feeds.|
|Threat Opinions|Lists the threat opinions as an assessment of the accuracy of the information that are associated with RSS feeds.|
|Threat Reports|Lists the threat reports associated with RSS feeds.|
|Tools|Lists the tools associated with RSS feeds.|
|Vulnerabilities|Lists the vulnerability records that centralize identification details, relationships, and remediation tracking associated with RSS feeds.|
|Related Cases|Lists the related case tasks that are associated with RSS feeds.|
|Related Case Tasks|Lists the related canvases that are associated with RSS feeds.|

**Related Records Actions:**

Use **Link** and **Unlink** to associate or remove associations between existing records without creating new records. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).

**Parent Topic:**[TISC Library Repository](../concept/tisc-ioc.md)

**Related topics**  


[Observables](../concept/observables.md)

[Indicators](../concept/indicator.md)

[Threat Entities](../concept/tisc-threat-entities.md)

[Other Objects](../concept/tisc-other-objects.md)

[Vulnerability Artifacts](../concept/vulnerability.md)

[Working with Reports in TISC](../concept/tisc-reports-lib-view.md)

[MITRE-ATT&amp;CK Repository](../concept/tisc-mitre-att-ck-framework-overview.md)

[Relationships Objects](../concept/relationship-objects.md)

[Potential Relationships](../concept/potential-relationships.md)

[Vulnerability relationship mapping](../concept/tisc-vul-relationship-map.md)

