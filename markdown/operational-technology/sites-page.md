---
title: Sites page
description: A Site represents a physical location in your organization, such as a DATACENTER, office, or IoT site. Each Site includes location details, time zone settings, and network range configurations that determine which IP addresses the Console for scans during discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/sites-page.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Sites page

A Site represents a physical location in your organization, such as a DATACENTER, office, or IoT site. Each Site includes location details, time zone settings, and network range configurations that determine which IP addresses the Console for scans during discovery.

**Note:** Sites is the starting step to group assets. All devices that are part of a given network range defined in the Site configuration are assigned to that site. If there are multiple Network Zones within the Site, these zones could be assigned to a Site for grouping purposes.

The Sites page contains a list of all the sites available in your Discovery Console for OT system. For each site, you can view the network range, time zone, latitude, and longitude. The following image shows an example of the Sites page.

\[Omitted image "sites-page-ot-console.png"\] Alt text: List of sites on the Sites page for the Discovery Console for OT

**Note:** You can't select the same IP Addresses for both the Include and Ignore selections for the Site without triggering an error.

-   **[Add a Site](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/add-site.md)**  
Add a site to your Discovery Console for OT.
-   **[Edit or delete a Site](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/edit-or-delete-site.md)**  
Edit a site to update its information or delete a site that no longer exists on your Discovery Console for OT.
-   **[Create a Site-specific Variable set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/creating-site-specific-variable-set.md)**  
Create a Site-specific Variable for use in Auto Queries. You can use the **Variable** as a credential for your **Site**.
-   **[Import Sites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/import-site.md)**  
Import existing Sites to the Discovery Console for OT.
-   **[Export sites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/export-site.md)**  
Export Sites on your Discovery Console for OT into a CSV.

**Parent Topic:**[Use the Discovery Console for OT pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/using-discovery-console.md)

