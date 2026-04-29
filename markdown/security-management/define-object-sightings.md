---
title: Define object sightings
description: Define object sighting that describes that an object \(malware, tool, threat actor, and so on\) was seen.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sightings, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define object sightings

Define object sighting that describes that an object \(malware, tool, threat actor, and so on\) was seen.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Object Sightings**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Object**|Identifies the object. Search and select the object.|
    |**Count**|The number of times the object was seen.|
    |**First Seen**|The time that this object first seen performing malicious activities.|
    |**Last Seen**|The time that this object was last seen performing malicious activities.|
    |**Source**|Specifies the threat source from which this record is created.|
    |**Description**|A description that provides more details and context about the object sighting, potentially including its purpose and its key characteristics.|
    |**Source ID**|Unique identifier for this object in the threat source.|
    |**Is Summary**| |
    |**Created Time in Source**|Specifies the time the object is created in the source.|
    |**Modified Time in Source**|Specifies the time the object is modified in the source.|

4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the object sighting.

|Related Lists|Description|
|-------------|-----------|
|External References|Lists external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Identities|List of identities associated with this object.|
|Observed Data|Lists observed data associated with this object.|

**Parent Topic:**[Sightings](../concept/indicator-sightings.md)

