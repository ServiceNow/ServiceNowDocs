---
title: Easy import properties
description: Several properties control the behavior of easy import.
locale: en-US
release: australia
product: Easy Import
classification: easy-import
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Easy import, Imports, Workflow Data Fabric]
---

# Easy import properties

Several properties control the behavior of easy import.

-   **glide.import\_template.row\_limit**

    Controls the maximum number of rows included in an easy import template. By default, if a table contains more than 10,000 records, only the first 10,000 are exported.

    -   Type: Integer
    -   Default value: 10,000
    -   Location: [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md)
-   **glide.easy\_import.run\_business\_rules**

    When true, business rules, workflows, approval engines, auditing, and field normalization apply when easy import inserts or updates data. This functionality is equivalent to setting GlideRecord.setWorkflow\(\) to true or false.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md)
-   **glide.import\_template.field\_types\_to\_ignore**

    A list of fields that will be ignored when a record is imported with easy import feature.

    -   Type: String
    -   Default value: table\_name, order\_index, collection, user\_image, video, timer, translated\_field, conditions, field\_name, sys\_class\_name, journal, journal\_input, due\_date, user\_input, image, workflow, template\_value, domain\_id, documentation\_field, user\_roles, glide\_list
    -   Location: [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md)

**Parent Topic:**[Easy import](../concept/c_EasyImport.md)

