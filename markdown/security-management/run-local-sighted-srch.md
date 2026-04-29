---
title: Run a sightings search on observables in a case
description: You can search for observables using the Sighting Search feature to determine how often they occur. Each occurrence is considered a sighting. You can limit the search to the number of sightings within a selected number of days or within a date range.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IoCs and observables in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Run a sightings search on observables in a case

You can search for observables using the Sighting Search feature to determine how often they occur. Each occurrence is considered a sighting. You can limit the search to the number of sightings within a selected number of days or within a date range.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Case Management** &gt; **All Cases**.

2.  Open the case that contains observables for which you want to run a sightings search.

3.  Click the **Case Artifacts** related link.

4.  Click the **Observables** tab.

5.  Select one or more observables for which you want to search for sightings.

    ![Run a sightings search](../image/run-sightings-search-obs.png)

6.  From the **Actions on selected items** drop-down list, select **Run sightings search**.

    The **Run Sighting Search** dialog box appears.

    ![Sightings search](../image/SightingsSearch.png)

7.  Either enter the number of days or hours you want to search for sightings of the selected observables, or select a date range.

8.  Click **Search**.


**Parent Topic:**[IoCs and observables in cases](../concept/cases-in-threat.md)

**Related topics**  


[Create a case from IoCs or observables](create-cases-threat.md)

[Add IoCs and observables to an existing case](add-records-to-cases-threat.md)

[Create an observable from a case](create-an-observable-from-a-case.md)

