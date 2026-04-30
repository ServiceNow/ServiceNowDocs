---
title: Create and configure a profile for sightings search with the Microsoft Defender for Endpoint integration
description: Create and configure the sightings search profile automatically using the Microsoft Defender for Endpoint.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create and configure a profile for sightings search with the Microsoft Defender for Endpoint integration

Create and configure the sightings search profile automatically using the Microsoft Defender for Endpoint.

## Before you begin

Role required: sn\_si.admin, sn\_si.admin

## About this task

You can use the Sightings Search workflow to perform the sighting searches. This workflow accepts a list of observables, finds any implementing capabilities, creates the queries that are based on the sighting search configurations, and executes the searches that are based on the configured workflow.

The Microsoft Defender for Endpoint provides a base system sighting search profile that enables you to configure the automatic sighting searches. With this profile, you can access the related observable sighting information of an organization and also see the sightings from other organizations.

## Procedure

1.  Navigate to **Integrations** &gt; **Sighting Search Configuration**.

2.  Click **New**.

3.  On the form, fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the sighting search profile.|
    |Is saved search|Option to save the search configuration. The saved search configuration queries are example queries. You can substitute them with the parameters for your environment and create additional-saved search configurations as required.|
    |Sightings search source|The source configured for the sightings search in Microsoft Defender for Endpoint integration.|
    |Search|Native search string that forms a query.|
    |Active|Option to enable the saved search configuration. Only active search configurations can perform a sightings search.|
    |Observable type|Type of observable category. For example, IP address, hash value, URL, and domain name.|
    |Maximum observable per search|Maximum number of observables that you can view from a search query. Set this value to 1 for this integration.|
    |Sightings search parameters|Parameters to define more complex queries that include logic and other operators supported by the specified log store.|

4.  Click **Submit**.


