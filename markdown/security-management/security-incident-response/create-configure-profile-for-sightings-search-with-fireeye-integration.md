---
title: Configure a profile for sightings search with the FireEye Integration
description: Configure the sightings search profile using the following procedure.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure a profile for sightings search with the FireEye Integration

Configure the sightings search profile using the following procedure.

## Before you begin

Role required: NowPlatform Security incident administrator \(sn\_si.admin\)

Whenever a source is created, individual sightings search configurations for five types \(File, IPs\(v4\), MD5, SHA1 and SHA256\) will be created and inactive by default. You should make it active before using Sighting Search. Each Observable type is having different search query to retrieve sightings. We would be initiating a different search for each observable type. Multiple observables search for a sighting search is not possible in FireEye as it would perform an AND operation on the observables and the result might be inaccurate.

**Note:** For Sightings search only five active searches can be present at once. Remaining will be queued and will start after the completion of any one of the ongoing sightings.

If you want to create a new sightings search profile, follow the steps below to create one:

## Procedure

1.  Navigate to **Integrations** &gt; **Sightings Search Configuration**.

2.  Click **New**.

3.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the capability profile.|
    |Is saved search|This will run a saved search i.e. the Name field should match the name of the saved search.|
    |Sightings search source|Defines the source configured for the integration.|
    |Search|Add a native search string to form a query.|
    |Active|Query will run only if it is active.|
    |Observable type|Defines the type of observable category.|
    |Maximum observables per search|The number of observables before the search query is split into multiple queries. Set this value to 1 for this integration.|
    |Sightings search parameters|Use Sightings Search Parameters to define more complex queries that include logic and other operators supported by specified log store.|

4.  Click **Submit** to complete the configuration.


