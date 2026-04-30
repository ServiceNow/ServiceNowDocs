---
title: Load more IoC data
description: Depending on settings in two properties and a script include definition, you can load geolocation information for IP addresses and websites in the Observables form. With further customization, you can also add other information, such as country codes, city names.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Observables, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Load more IoC data

Depending on settings in two properties and a script include definition, you can load geolocation information for IP addresses and websites in the Observables form. With further customization, you can also add other information, such as country codes, city names.

## Before you begin

The following two properties must be set:

-   **The domain name to retrieve additional information for IP addresses/URLs** \[sn\_ti.ip\_lookup.web\_site\]
-   **The API key to be used for the above domain, if any** \[sn\_ti.ip\_lookup.api\_key\]

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Observables**.

2.  Click the IP address or URL of the observable to which you want to view more IoC data.

    The **Location** field shows the geolocation of the IoC.

3.  Click the **Enrich data** button to load the additional IoC data.

4.  You can also configure the Observable form to add other location-related fields, such as the country code and city code.

    **Note:** To load more location-related information, edit the **ThreatAdditionalInfo** script include and provide the appropriate API key from the website that provides the additional information.


**Parent Topic:**[Observables](../concept/c_Observables.md)

**Related topics**  


[Define an observable](t_AddObservable.md)

[Add a related IoC to an observable](t_AddIoCToObserv.md)

[Add associated tasks to an observable](t_AddAssociatedTasksToObservable.md)

[Add a related observable](t_AddRelatedObservable.md)

[Identify observable sources](t_IdentifyObservbleSources.md)

[Perform lookups on observables](perform-lookups-on-observables.md)

[Perform threat enrichment on observables](perform-enrich-on-observs.md)

