---
title: Define the Jamf configuration
description: Associate that software with a group through a Jamf configuration to create catalog items for Jamf software deployment or to configure your instance to revoke software through .
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Jamf, Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Define the Jamf configuration

Associate that software with a group through a Jamf configuration to create catalog items for Jamf software deployment or to configure your instance to revoke software through .

## Before you begin

Before you create a Jamf configuration record, make sure you have discovered the Jamf applications, groups, and deployments, and set up the necessary software models.

Role required: sn\_jamf\_spoke.jamf\_admin or admin

## About this task

The Jamf configuration process associates software with Jamf groups. To deploy software from a Jamf server, the user or device must be a member of a Jamf group associated with an install deployment. CSD 2.0 enables you to revoke unentitled software using the Jamf server when that software can be removed using the installation group by removing user or device from it. Users requesting revokable software from the Service Catalog also have the ability to define lease start and stop dates and request lease extensions.

Perform these steps for the Jamf applications and policies.

## Procedure

1.  Navigate to **Jamf** &gt; **Configurations**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the Jamf software configuration record.|
    |Group|Name of the group associated with the selected application on the Jamf server. Same group can be used for both installation and uninstallation. Only those groups associated with the application are available for selection.|

4.  Click **Submit**.


**Parent Topic:**[CSD 2.0 for Jamf](../concept/csd2-jamf-tsk.md)

