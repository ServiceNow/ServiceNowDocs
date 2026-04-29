---
title: SLAs for application services and CIs
description: Event Management supports the creation of SLAs for application services and for CIs.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# SLAs for application services and CIs

Event Management supports the creation of SLAs for application services and for CIs.

You can monitor and manage the quality of the application services offered by your organization. For example, you might want to set up an SLA that is triggered when the max alert severity of an application service or CI is **Critical**, and measure the time it takes to bring the application service or CI back to the **OK** state, when the conditions that caused the alert have been resolved.

## SLAs and the Task table

You can create SLA definitions only for tables that extend the Task table. The Event Management application provides a table named Event Management SLA \[em\_ci\_severity\_task\], which extends the Task table. Use this table in your SLA definitions to specify the severity level that should trigger and stop the SLA. During alert impact calculation, changes in the severity level of application services and CIs are automatically updated in the Event Management SLA table. [Scheduled jobs](../reference/r_InstalledWithEventManagement.md#) keep the information in this table up to date.

## How the Event Management SLA table is populated

The Event Management SLA table is populated differently for application services and CIs:

-   For application services, the system automatically populates the Event Management SLA table when an application service is created or when its max severity is changed.
-   For CIs, you must first identify which CIs can be made available for SLAs by creating an SLA configuration record. The system then automatically populates the Event Management SLA table with the CI max severity is changed.

**Note:** Duplicate CIs are not added to the Event Management SLA table even if the same CI matches more than one SLA configuration filter.

-   **[Create an SLA configuration for CIs](../task/t_EMCreateAnSLAConfiguration.md)**  
Create an SLA configuration from the Event Management application to determine which CIs are available for SLAs.
-   **[Create an SLA definition for a CI or application service](../task/t_EMCreateSLADefForCI_BS.md)**  
You can create SLA definitions for CIs and application services just as you can for other task records in the instance.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

