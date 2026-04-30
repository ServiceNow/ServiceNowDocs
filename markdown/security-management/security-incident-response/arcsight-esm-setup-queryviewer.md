---
title: Set up the ArcSight ESM Query Viewer
description: Create a query viewer and define filters that will include recently created correlation events that will be ingested ServiceNow.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up your ServiceNow AI Platform instance for the ArcSight ESM event ingestion integration, ArcSight ESM Event Ingestion for Security Operations integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the ArcSight ESM Query Viewer

Create a query viewer and define filters that will include recently created correlation events that will be ingested ServiceNow.

## Before you begin

Role required: ArcSight Administrator

## Procedure

1.  Log into the ArcSight ESM console to create a query viewer.

2.  To create a new query, navigate to **File** &gt; **New** &gt; **Query**.

    ![ArcSight ESM: Query Viewer Setup: Create](../image/sir-arcsight-query-viewer-setup2.png)

3.  Define conditions for the Query Viewer in the **Inspect/Edit** panel.

    ![ArcSight ESM: Query Viewer Setup: Create: General](../image/sir-arcsight-query-viewer-setup3.png)

<table id="choicetable_xs5_bvc_c5b"><thead><tr><th align="left" id="d196635e104">

Field Name

</th><th align="left" id="d196635e107">

Description

</th></tr></thead><tbody><tr><td id="d196635e113">

**Name**

</td><td>

Enter a name for the query.

</td></tr><tr><td id="d196635e122">

**Query On**

</td><td>

Select **Event** from the drop down list.

</td></tr><tr><td id="d196635e134">

**Start Time**

</td><td>

To ingest the most recent data, select the date from the events are to be ingested. Specify a date that is a day or a few days earlier than the current date. **Note:** You cannot specify a date that is more than 7 days older than the current date. If you are ingesting a large number of events, you must specify a date that is 1 or 2 days older than the current date.

</td></tr><tr><td id="d196635e146">

**End Time**

</td><td>

This is the current date.

</td></tr><tr><td id="d196635e156">

**Row Limit**

</td><td>

The maximum number of events that can be ingested at a time. Specify a value that is less than 5000 here.

</td></tr></tbody>
</table>4.  Click on the **Fields** tab.

    ![ArcSight ESM: Query Viewer Setup: Create: Fields](../image/sir-arcsight-query-viewer-setup4.png)

5.  Select the fields that must be included during ingestion.

    You must select the `Event ID`, `Name`, and `End Time` fields for ingestion to be successful.

6.  Click the **Add 'ORDER BY' columns** link and select **Event ID** field and specify the sort order as **Descending** to ensure that the latest events are ingested.

7.  Click the **Conditions** tab.

8.  Right click **Event** under **Event Conditions** under the **Summary** section.

9.  Click **New Condition** &gt; **Root** &gt; **Type** and select the Event Type as **Correlation**.

    **Important:** Only correlation events will be retrieved; base events for correlations will not be retrieved.

    ![ArcSight ESM: Query Viewer Setup: Select Type](../image/sir-arcsight-query-viewer-setup5.png)

10. Click **OK** to save the query.

    The next step is to create a Query Viewer for this query.

11. Navigate to **File** &gt; **New** &gt; **Query Viewer**.

    ![ArcSight ESM: Query Viewer Setup: Create Query Viewer](../image/sir-arcsight-query-viewer-setup6.png)

    |Field Name|Description|
    |----------|-----------|
    |**Name**|Enter a name for the Query Viewer.|
    |**Query**|Select the query you have just created.|
    |**Refresh Data After**|Specify the frequency at which the data is to be refreshed.|

12. Click the **Fields** tab and ensure that the mandatory fields \(`Event ID, Name, End Time`\) you have specified in your query are selected.

13. Click **Apply** to save the Query Viewer.

    The new Query Viewer that you have created is listed in the Query Viewers section.

14. Click on the Query Viewer to see the data being ingested.

    ![ArcSight ESM: Setup Query Viewer: Completed](../image/sir-arcsight-query-viewer-setup7.png)


