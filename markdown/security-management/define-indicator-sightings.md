---
title: Define indicator sightings
description: Define sightings that denote that an indicator was seen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sightings, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define indicator sightings

Define sightings that denote that an indicator was seen.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Indicator Sightings**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Indicator**|Identifies the indicator. Search and select the indicator.|
    |**Count**|The number of times the object was seen.|
    |**First Seen**|The time that this object first seen performing malicious activities.|
    |**Last Seen**|The time that this object was last seen performing malicious activities.|
    |**Source**|Specifies the threat source from which this record is created.|
    |**Description**|A description that provides more details and context about the indicator sighting, potentially including its purpose and its key characteristics.|
    |**Source ID**|Unique identifier for this object in the threat source.|
    |**Is Summary**| |
    |**Created Time in Source**|Specifies the time the object is created in the source.|
    |**Modified Time in Source**|Specifies the time the object is modified in the source.|

4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the indicator sighting.

|Related Lists|Description|
|-------------|-----------|
|External References|Lists external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Identities|List of identities associated with this object.|
|Observed Data|Lists observed data associated with this object.|

**Parent Topic:**[Sightings](../concept/indicator-sightings.md)

