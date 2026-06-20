---
title: Share Sightings Search results
description: You can share local sightings details or results that are associated with a particular search with your Trusted Security Circle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/share-sightings-search-results.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 1
breadcrumb: [View Sightings Search Results, Create sightings search configuration records, Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Share Sightings Search results

You can share local sightings details or results that are associated with a particular search with your Trusted Security Circle.

## Before you begin

Role required: sn\_si.analyst

## About this task

Sharing can be automated using the following Security Incident Response **Properties**.

-   Automatically share the results of a sightings search to the default ServiceNow trusted circle
-   Include observables with no local sightings when automatically sharing sightings search results
-   Respond with local sightings whenever a threat share is received from a trusted circle

## Procedure

1.  Navigate to a security incident.

2.  Select the **Show IoC** related list and select the **Sightings Search Results** tab to view the list of sightings searches.

3.  Select a sightings search result.

4.  On the **Sightings Search Result**form, Select the **Share sighting search result** related link.

    The Sighting Search Result Share dialog box appears.

5.  Enter a **Name** for this observable share record.

6.  Enter a **Description**of the observables to share.

7.  Choose **Circles** to share the observables with.

8.  Select **Submit**.

    The observable\(s\) are shared with the specified Trusted Circle.


**Parent Topic:**[View Sightings Search Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/view-sightings-search-results.md)

