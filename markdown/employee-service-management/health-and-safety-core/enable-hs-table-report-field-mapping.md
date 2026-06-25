---
title: Enable a Health and Safety table for configuring report field mapping
description: Enable a Health and Safety table for report field mapping. You can then configure its mapping with your reporting PDF template, enabling safety agents to generate reports for records in this table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety-core/enable-hs-table-report-field-mapping.html
release: australia
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Enable a Health and Safety table for configuring report field mapping

Enable a Health and Safety table for report field mapping. You can then configure its mapping with your reporting PDF template, enabling safety agents to generate reports for records in this table.

## Before you begin

Verify that the application scope is selected as Health and Safety Core. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: sn\_ohs\_im.admin

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  In the property **Report field mapping tables**, add the table name, for example, `sn_ohs_im_action`, to enable it for report field mapping.

    `sn_ohs_im_incident`, `sn_ohs_im_observation`, and `sn_ohs_im_injury_illness` tables are set as default value in this property.

3.  Select **Save**.


## Result

-   The table is available in the **Mapping table** field when configuring a report field mapping for this table.
-   The **Generate report** button becomes available in all records for this table.
-   Once a report field mapping is set up for this table, the **Generate report** button becomes available for all its records.

## What to do next

To generate a report for this table's records, you must configure its report field mapping. For more information, see [Create a safety report field mapping for generating reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-core/create-safety-report-field-mapping.md).

**Parent Topic:**[Setting up Health and Safety Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-core/setting-up-hs-core.md)

**Related topics**  


[Install Health and Safety Core]()

[Workplace location data]()

[Create a safety report field mapping for generating reports]()

[Configure groups for Health and Safety]()

[Configure scheduled job to generate frequency rates]()

[Assign Health and Safety profile to a user]()

[Add a Health and Safety visitor]()

[Migrate existing safety documents to the Document library]()

