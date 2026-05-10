---
title: Send data to the Employee Health Screening log
description: Send data from a third-party system to the Employee Health Screening application log table. You can use this table to create reports and monitor health trends.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with Safe Workplace suite, Safe Workplace, Health and Safety, Employee Service Management]
---

# Send data to the Employee Health Screening log

Send data from a third-party system to the Employee Health Screening application log table. You can use this table to create reports and monitor health trends.

## Before you begin

Role required: sn\_imt\_core.api\_logging\_user

## Procedure

1.  Send a POST request to the Table API on your instance.

    For more information, see [Table API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/c_TableAPI.md).

    1.  Construct the endpoint using the Log Import \[sn\_imt\_core\_log\_import\] table.

        ```
        https://<your-instance>.servicenow.com/api/now/table/sn_imt_core_log_import
        ```

    2.  Set fields in the Log table by defining these request body parameters.

        |Field|Description|
        |-----|-----------|
        |Source|Internal name to identify the third-party system making the log entry.|
        |Level|User status, log level, or any other meaningful string. For example, you can enter `Allowed` or `Denied` to indicate whether the individual is cleared for entry.|
        |Message|Description of the health screening. For example, `Temp too high`.|
        |User|Employee or visitor email from the Health and Safety User \[sn\_imt\_core\_health\_and\_safety\_user\] table.|
        |Additional Info|Data to provide any additional information. For example, `{'temperature':'101', 'location':'San Diego'}`.|

    This example cURL request sends a record to the Log Import table.

    ```
    curl "http://<your-instance>.servicenow.com/api/now/table/sn_imt_core_log_import" \
    --request POST \
    --header "Accept:application/json" \
    --header "Content-Type:application/json" \
    --data "{\"u_source\":\"BadgesRUs\",\"u_message\":\"Temp too high\",\"u_user\":\"abel.tutor@servicenow.com\",\"u_level\":\"Denied\"}" \
    --user 'username':'password'
    ```

    The system automatically inserts the record into the Log \[sn\_imt\_core\_log\] table.

2.  Navigate to the Log \[sn\_imt\_core\_log\] table to check that the data imported correctly.


## What to do next

Generate reports on the data you imported to the Log \[sn\_imt\_core\_log\] table using [Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/reporting-landing-page.md).

