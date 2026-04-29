---
title: Add related fields to a Microsoft 365 configuration record
description: Add related fields to filter values based on the chosen primary field. These filter values will automatically adjust according to the selected filter criteria.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Add additional reporting configuration filters for a Microsoft 365 configuration record, Integrating Microsoft 365 with ServiceNow reporting, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Add related fields to a Microsoft 365 configuration record

Add related fields to filter values based on the chosen primary field. These filter values will automatically adjust according to the selected filter criteria.

## Before you begin

Create additional reporting configuration filters for a Microsoft 365 configuration record. For more information, see [Set up Microsoft 365 reporting configuration](configure-o365-reporting-configs.md) and [Add additional reporting configuration filters for a Microsoft 365 configuration record](add-additional-reporting-filters.md).

Role required: \(per product\)

-   In Operational Sustainability Management: sn\_esg\_msoff\_intg.admin
-   In Audit Management: sn\_audit.admin

## About this task

Filter the fields dynamically and set up dependencies by using related fields. In the Microsoft 365, you can configure fields so that cascading filters are supported dynamically. You can select a value in a field and have the related fields automatically update to show the relevant options. This process helps you to streamline data entry and improve efficiency.

## Procedure

1.  Navigate to once of the following locations:

    -   **All** &gt; **Operational Sustainability Management** &gt; **Microsoft 365 Reporting Integration** &gt; **Reporting Configurations**
    -   **All** &gt; **Audit** &gt; **Audit report** &gt; **Reporting Configurations**
2.  Open the record for which you want to add the additional reporting configuration filters.

3.  On the Microsoft 365 reporting configuration filters related list, select the field name of the filter you want to add related fields to.

4.  Select the lock icon ![Lock icon.](../../../reuse/icons/product-icons/lock-outline-24.svg) to unlock the related fields and then choose the fields that the **Field name** should be related to.

5.  Add related fields by selecting the magnifying glass icon ![Magnifying glass icon.](../../../reuse/icons/product-icons/magnifying-glass-outline-24.svg) and choosing the fields that you want.

    Only fields with a greater order values can be selected as related fields.

6.  Select update.

    The available **Field name** values are now dependent on what value is selected for the fields added as related fields. For example, if you selected the city field name you can select the country field name as a related field so that only cities from that country show when you make selections.

7.  Repeat steps 3 through 6 until all the related fields that you want are set up.


## Result

The related fields are ready to be used as part of your configuration data.

## Data aggregation for entities in Japan

If an ESG reporting disclosure manager wants to understand the total emissions for an entire year for a particular location in Japan and if the location has sub-locations, you can make this process easier by using related fields. To add related fields, select the field that you want to set a dependency with. For instance, select the City field and add the Country field as a related field. Now, when you select Japan as the location's country, the options for the city field will be limited to only cities located in Japan. This setup helps ensure that the data aggregation for Scope 1 emissions is focused on Japan and its specified sub-locations, such as Tokyo and Kyoto.

**Parent Topic:**[Add additional reporting configuration filters for a Microsoft 365 configuration record](add-additional-reporting-filters.md)

