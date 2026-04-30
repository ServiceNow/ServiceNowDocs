---
title: Perform a manual sighting search in Microsoft Defender for Endpoint
description: Select individual or multiple observables and perform a manual sighting search in Microsoft Defender for Endpoint to determine the prevalence of a threat over time.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and configure profile, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Perform a manual sighting search in Microsoft Defender for Endpoint

Select individual or multiple observables and perform a manual sighting search in Microsoft Defender for Endpoint to determine the prevalence of a threat over time.

## Before you begin

Role required: sn\_si.admin, sn\_si.analyst

## About this task

The supported Observable types are the following:

-   Domain name
-   IP address \(V4\)
-   IP address \(V6\)
-   MD5 hash
-   SHA1 hash
-   SHA256 hash

## Procedure

1.  Navigate to the **Security Incidents**.

2.  Open an existing SIR or create a new SIR.

3.  In the related links, click **Show IoC**.

4.  Click the Associated Observables related lists.

5.  Select the observables.

6.  From the Actions list, click **Run Observable Enrichment**.

7.  Select the observables under **Action** on selected rows, and click **Run Sightings Search**.

    **Note:** Sighting search is supported for Domain name, IP address \(V4\), IP address \(V6\), MD5 hash, SHA1 hash, and SHA256 hash observables types respectively.

8.  Specify the time frame for the search, and click **Search**.

    **Note:** The Microsoft Defender for Endpoint supports sighting search only for the last 30 days. If your range query is earlier than the last 30 days, then sighting search does not retrieve any data. If your range query overlaps with the last 30 days, then the sightings from only the last 30 days get retrieved, and if your range query is within the last 30 days, then the sightings from the defined start time to the current time is retrieved.

9.  On completion of the search, validate the results and details in the related lists.

10. Click **Sightings Search Details** to view the sighting search details.

11. Click the **Sighting** tab for details and **Sightings Search Results** tab for search results.

    You can view additional information related to the particular sighting in the **Summary** field.


