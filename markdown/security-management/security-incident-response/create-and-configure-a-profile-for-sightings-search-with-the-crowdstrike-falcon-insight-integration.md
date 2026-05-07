---
title: Create and configure a profile for the sighting search
description: Use sightings searches for CrowdStrike Falcon Insight to locate infected machines across your organization's network and to address security incident response cases.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create and configure a profile for the sighting search

Use sightings searches for CrowdStrike Falcon Insight to locate infected machines across your organization's network and to address security incident response cases.

## Before you begin

Role required: sn\_si.analyst

## About this task

Select individual or multiple observables and perform a manual sighting search in CrowdStrike Falcon Insight to determine the prevalence of a threat over time.

## Procedure

1.  Navigate to **All** &gt; **CrowdStrike Falcon Insight Integration** &gt; **Sightings Search Profiles**.

2.  Select **New**.

3.  Configure this profile to determine what servers to search for a specific CrowdStrike Falcon Insight search capability.

4.  On the form, fill the fields:

<table id="table_uwr_ky4_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Sighting Search profile.

</td></tr><tr><td>

Is saved search

</td><td>

Saved search configuration is created if you select this option.

</td></tr><tr><td>

Sightings search source

</td><td>

The source for the sightings search. Select the **CrowdStrike Falcon Insight Sighting Search** as the source.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the additional is active or not.

</td></tr><tr><td>

Observable type

</td><td>

CrowdStrike Falcon Insight integration supports the following Observable types:-   Hash
-   IP
-   URL
Sighting search is supported for the following Observables types:

-   Domain name
-   IP address \(V4\)
-   IP address \(V6\)
-   MD5 hash
-   SHA1 hash
-   SHA256 hash


</td></tr><tr><td>

Maximum observables per search

</td><td>

Maximum number of observables that you can view from a search query.

</td></tr><tr><td>

Search

</td><td>

The default search string is`$(observable)`, but you can define your own search query by specifying parameters that are supported by the CrowdStrike Falcon Insight integration.

</td></tr><tr><td>

Sightings Search Parameters

</td><td>

Parameters to define more complex queries that include logic and other operators supported by the specified log storeYou can use the Related Links at the bottom of the page to generate a test query after defining Sighting Search Parameters.

</td></tr></tbody>
</table>    ![Configuring sightings search.](../image/falcon-insight-sightings-search.png)

5.  Select **Submit**.

    The configuration is complete and you can invoke the sightings search from the ServiceNow AI Platform security incident.

6.  To verify the configuration and run a sighting search, perform the followings steps:

    1.  Open a security incident, scroll to the bottom of the security incident, and click **Show all Related Lists**.

    2.  If you select one or more Configuration Items \(CI\) from the **Running Processes** related lists.

        **Note:** If you run a sighting search for a CI from the Running Processes related list, then it will only be a Process Hash sighting search.

    3.  Select the **Actions on selected rows...** drop-down list, and select **Run CrowdStrike Sightings Search**.

    4.  Look up the required Sighting Search Profile using the search option.

    5.  Select the required Sighting Search Profile, and select **Submit**.

    6.  If you select one or more Observables from the **Associated Observables** related lists.

    7.  Select the **Actions on selected rows...** drop-down list, and select **Run Sightings Search**.

    8.  In the time frame pop-up, select any random value and select **Search**.

    9.  On completion of the search, validate the results and details in the work notes and related lists.

    10. Select the **Sightings** tab to view the sighting details.

    11. Select the **Preview** icon next to the CI to view more information about CrowdStrike sighting details.

    12. Select the **Sightings Search Details** to view the sighting search details, and select the **Sightings Search Results** tab for search results.


