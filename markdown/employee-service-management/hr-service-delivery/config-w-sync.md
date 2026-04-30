---
title: Configure worker profile settings
description: Configure parameters to ensure that worker profiles are synchronized between Workday and ServiceNow.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Synchronize worker profiles, Configuring HR Service Delivery Integration with Workday, HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure worker profile settings

Configure parameters to ensure that worker profiles are synchronized between Workday and ServiceNow.

## Before you begin

Role required: sn\_hr\_workday.admin

## Procedure

1.  Navigate to **Workday Worker Profile Sync** &gt; **Configurations** &gt; **Worker Profile Sync Configurations**.

2.  Update the fields in the record as per your requirements.

    **Important:** For details on how to get the value for each of the fields in the form, refer to this [KB article.](https://support.servicenow.com/kb_view.do?sysparm_article=KB0869827#confignav)

    |Field|Description|
    |-----|-----------|
    |Workday tenant time zone|Time Zone of Workday workers.|
    |Number of days to look ahead for upcoming onboarding and offboarding events|Number of days that is considered to pull the profiles of future workers who are onboarding or off boarding.|
    |Department organization type ID|Unique identifier for the department organization type.|
    |Location usage ID|Unique identifier for the location usage.|
    |Location phone device type ID|Unique identifier for the location phone device type.|
    |Location fax phone device type ID|Unique identifier for the location fax phone device type.|
    |Location communication usage type ID|Unique identifier for the location communication usage type.|
    |Enable dry run|When enabled, data is pulled into staging tables, but is not transformed to target tables.|
    |Enable debugging|When enabled, additional logs are collected.|
    |Worker home email communication usage type ID|Unique identifier for the worker home email communication usage type.|
    |Worker work email communication usage type ID|Unique identifier for the worker work email communication usage type.|
    |Worker work phone communication usage type ID|Unique identifier for the worker work phone communication usage type.|
    |Worker home phone communication usage type ID|Unique identifier for the worker home phone communication usage type.|
    |Worker mobile phone device type ID|Unique identifier for worker mobile phone device type.|
    |Worker phone device Type ID|Unique identifier for worker phone device type.|
    |Worker Home Address Type Reference Communication Usage Type ID|Unique identifier for worker home address.|

3.  Click **Submit**.


## What to do next

Click the Get Reference ID Types related link to run the flow that interacts with Workday to pull the reference ID types that are referenced in the configuration fields.

