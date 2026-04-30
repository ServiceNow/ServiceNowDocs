---
title: Understanding PDIs
description: PDIs require you to select a specific release and maintain consistent usage to avoid hibernation.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Personal developer instance guide, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Understanding PDIs

PDIs require you to select a specific release and maintain consistent usage to avoid hibernation.

Sign in to the Developer Site to keep your PDI active. After a period of inactivity, your instance is reclaimed. Back up your work regularly to prevent data loss.

**Note:** To save your work, commit your work to source control or create update sets. Work that is not saved may be lost due to instance reclamation.

When a PDI is reclaimed, the instance is unassigned from you, reset to its original state, and reassigned to another Developer Program member. Reclaiming instances allows the Developer Program to support active program members with free instances. The **Account** menu on the Developer Site header includes a reminder in the Activity section that you have ten days of inactivity.

![PDI that could be reclaimed](../image/pdi-guide-tokyo_pdiguide_images_servicenow_pdi_activity.png)

Keep your PDI active by signing in or performing developer-type activities on your instance such as:

-   Creating an application
-   Creating a table
-   Adding a field to a table
-   Creating a Script Include

## Hibernation

To keep the developer program free and provide PDIs to everyone who wants one, instances hibernate when they are idle. When a PDI hibernates, the database and application server shut down to conserve computing resources. All your data is preserved when the PDI hibernates. You can wake up a hibernating instance by signing in to the Developer Site. Waking an instance from hibernation resets the ten-day inactivity countdown.

In addition, you should also be aware of the following:

-   PDIs are returned to the pool of available instances if they go unused for ten days. Duration may change due to availability.
-   Availability is not guaranteed.
-   PDIs cannot be clone targets or clone sources for customer or partner instances.
-   PDIs cannot be linked via team development to customer or partner instances since they belong to ServiceNow®.
-   PDIs cannot publish to the ServiceNow Application Repository or the ServiceNow® Store.
-   PDIs cannot work with Machine Learning, Instance Data Replication, or MetricBase.
-   Many ServiceNow® Store applications cannot be installed on PDIs.

## Mainentance

ServiceNow® occasionally needs to perform maintenance on the underlying infrastructure associated with PDIs. Maintenance includes updating and patching software, firmware, and replacing hardware. During maintenance, your PDI may not be accessible. The length of time required for maintenance depends on the type of maintenance. If available, the My Instance page indicates the expected completion time for planned maintenance. Your work and data on your PDI is unaffected by planned maintenance.

## PDIs and the release selector

When content is available for different releases, use the release selector to select a release. The server icon next to the release name identifies the release of your PDI. The bar under the release name identifies the selected release. When working on your PDI, be sure the content matches your PDI.

![Select a release](../image/pdi-release-selector.png)

If the content does not match your PDI release, click the release with the server icon to view the content that matches the release of your PDI.

![Selected release](../image/pdi-release-selector-2.png)

The selector only shows releases for which the current page of content is available except when the content is not available for your PDI release. When the content is not available for your PDI release, the PDI release is grayed out and cannot be selected.

![Release content not available](../image/pdi-release-selector-3.png)

If your PDI is not on the latest release, follow the steps for [upgrading your PDI](../task/upgrading_your_pdi.md) to get the latest release.

**Parent Topic:**[Personal developer instance guide](personal_developer_instance_guide.md)

