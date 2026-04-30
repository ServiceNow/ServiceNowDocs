---
title: View Sightings Search Data
description: Review the aggregate data of all sighting searches.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create sightings search configuration records, Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# View Sightings Search Data

Review the aggregate data of all sighting searches.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to a security incident.

2.  Select the **Sightings Search Data** tab from **Show All Related Lists** Related List group to view the list of sightings searches.

    **Note:** This data can be shared with Trusted Security Circle.

<table id="table_lg3_dm5_vy"><thead><tr><th>

Result

</th><th>

Description

</th></tr></thead><tbody><tr><td>

End date range

</td><td>

Time to stop looking for sightings.

</td></tr><tr><td>

External Sightings

</td><td>

Aggregated count of external sightings. \(Received from threat sharing.\)

</td></tr><tr><td>

Internal Sightings

</td><td>

Aggregated count of internal sightings.

</td></tr><tr><td>

Is Local

</td><td>

Indicates whether the sightings came from the current or a shared environment.

</td></tr><tr><td>

Observable

</td><td>

List of all observables searched for by query.

</td></tr><tr><td>

Sighting count

</td><td>

Number of sightings searched for.

</td></tr><tr><td>

Sighting search

</td><td>

Sightings Search identifier.

</td></tr><tr><td>

Sighting search detail

</td><td>

Aggregate detail of the sighting search.

</td></tr><tr><td>

Sighting search link

</td><td>

Link pointing to the Sighting search portal. The search query is automatically applied upon clicking the Sighting search link.

</td></tr><tr><td>

Sighting search query

</td><td>

Query to identify the instance. 172.10.0.171 is substitutable and gets substituted in the observable selected.

\(search 172.10.0.171 \| head 10\)

**Note:** Selection of days will not be applicable to Saved search.

</td></tr></tbody>
</table>
**Parent Topic:**[Create sightings search configuration records](../../security-incident-response/task/sightings-search-configurations.md)

