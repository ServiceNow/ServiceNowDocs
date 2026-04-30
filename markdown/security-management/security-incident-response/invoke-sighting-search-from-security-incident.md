---
title: Invoke Sighting Search from a Security Incident
description: Invoke the sightings search from a SIR security incident by following the below procedure.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Invoke Sighting Search from a Security Incident

Invoke the sightings search from a SIR security incident by following the below procedure.

## Before you begin

Role required: ServiceNow AI Platform administrator \(sn\_si.admin\)

## Procedure

1.  Navigate to the Security Incidents.

2.  Open any existing SIR or create a new SIR.

3.  Click Show IoC in Related Links.

4.  Click **Associated Observables** related lists.

    ![Associated Observables related list selected](../image/invoke-sighting-search-from-security-incident.png)

5.  Add any existing observables or create new observable.

    ![Add a new or existing Associated Observable to the related list](../image/invoke-sighting-search-create-observable.png)

6.  Select the observables and from Actions on selected rows, click **Run Sightings Search**.

    ![Observables in the list selected and Run Sightings Search selected](../image/invoke-sighting-search-run-sighting-search.png)

7.  Ignore the inputs in the next dialog box that asks for time data.

    There are default values populated. However, the search is performed real time and the time values are ignored for this integration.

    ![Run Sightings search](../image/run-sightings-search.png)

8.  Check the worknotes for status.

    ![Security Incident work notes](../image/invoke-status-worknotes.png)

9.  On completion of the search, check the results and details in the related lists.

10. Click on **Sightings Search Details** tab for details and **Sightings Search Results** tab for search results.

    ![Sighting Search Details](../image/invoke-sightings-search-details-tab.png)

    ![Sightings Search Results](../image/invoke-sightings-search-results.png)


