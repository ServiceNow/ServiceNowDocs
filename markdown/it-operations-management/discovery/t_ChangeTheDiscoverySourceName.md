---
title: Change the source name of Discovery results
description: You have the option of changing the source name of discovery results. This might be desirable if Discovery is running on your network together with another discovery product, and you want to use customized identifiers.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Change the source name of Discovery results

You have the option of changing the source name of discovery results. This might be desirable if Discovery is running on your network together with another discovery product, and you want to use customized identifiers.

## Before you begin

Role required: discovery\_admin or admin

## About this task

The Source \[sys\_object\_source\] table stores information identifying the source of a discovery, the ID of that source, and the date/time of the last scan.

To view this information, configure a CI form and add the **Sources** related list. This table is populated automatically when the Discovery plugin is enabled.

![Sources List](../image/DiscoveryCISources.png "Sources List")

To migrate your Discovery Source to ServiceNow:

## Procedure

1.  Update the **glide.discovery.source\_name** system property to have a value of ServiceNow.

2.  Edit the dictionary entry for the Configuration Item \[cmdb\_ci\] table.

3.  Update the choice list for the discovery\_source column to only have the value ServiceNow for a discovery product.

4.  Open a list for the Configuration Item \[cmdb\_ci\] table and filter on a discovery source field value you want to change.

5.  Use the Update All option to change the value to ServiceNow.

6.  Open a list for the Source \[sys\_object\_source\] table and filter on a name field value you want to change.

7.  Use the Update All option to change the value to ServiceNow.


**Parent Topic:**[Advanced Discovery configuration](../concept/c_DiscoveryExtendedCapabilities.md)

