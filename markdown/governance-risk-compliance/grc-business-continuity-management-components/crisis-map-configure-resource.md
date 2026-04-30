---
title: Configure a resource for crisis map
description: Configure resources to plot the organization's assets on the crisis map. The assets can be locations, employees, data centers, suppliers, and others. Configuring resources is also required as an input to set up alert rules.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure search for places in crisis map, Setting up the crisis map, Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure a resource for crisis map

Configure resources to plot the organization's assets on the crisis map. The assets can be locations, employees, data centers, suppliers, and others. Configuring resources is also required as an input to set up alert rules.

## Before you begin

Role required: System administrator

Set up the Google maps for enabling the crisis map functionality. For more information, see [Set up Google Maps API](https://www.servicenow.com/docs/access?context=set-up-google-maps-api&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **Threat and Alert Data Feeds** &gt; **Administration** &gt; **Resource Configurations**.

2.  To add a new scheduled data import, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the resource configuration used in the map visualization.|
    |Icon|Image representing a resource item on the map.|
    |Table|Table for resources to plot on the map.|
    |Location field|Location column of the table used as location on the map.|
    |Use Coordinates|Option for enabling coordinates to plot the resources on the geo-map.|
    |Application|Read-only field. The field helps distinguish items relevant to the crisis map.|
    |Active|Option to indicate that the resource configuration is active.|
    |Category|Value is BCM application. Helps to identify the BCM-related resources when multiple applications use the component.|
    |Searchable|Option to indicate if the resource is searchable in the map visualization.|
    |Contact User Field|Contact for communication for the resource in focus.|
    |Contact Alias|Contacts for identification.|
    |Display Fields|Fields selected for display as the contacts.|
    |Conditions|Conditions for filtering records from the table.|

4.  Click **Submit**.


**Parent Topic:**[Configure search for places in crisis map](crisis-map-place-api-configuration.md)

