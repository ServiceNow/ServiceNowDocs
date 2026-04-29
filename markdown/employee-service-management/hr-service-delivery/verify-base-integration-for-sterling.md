---
title: Verify integration for the Sterling service
description: The integration is configured to push background check data between the HR service in HR Service Delivery and the Sterling service. You can verify the preconfigured settings and determine whether they meet your needs or if further customization is required.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with the Sterling Talent Solutions service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Verify integration for the Sterling service

The integration is configured to push background check data between the HR service in HR Service Delivery and the Sterling service. You can verify the preconfigured settings and determine whether they meet your needs or if further customization is required.

## Before you begin

Role required: sn\_hr\_integrations.admin

## Procedure

1.  Verify the HR service mappings, which maps the HR service to the HR web service.

    1.  Navigate to **HR Integrations** &gt; **HR Service Mapping**.

    2.  Right-click the **HR external source** column and select **Group By HR external source**.

    3.  For the **Sterling** group, click the arrow to expand the list.

    4.  For each record, click the information icon to verify that the HR service is correctly mapped to the appropriate HR web service.

        **Note:** Make sure to provide the endpoint URL for the **Sterling Background Check API** record.

        |HR service mapping|HR service|HR web service|
        |------------------|----------|--------------|
        |Sterling Background Check - Request Background Check by Sterling|Request Background Check by Sterling|Sterling Background Check API|

2.  Verify the HR outbound schema mappings.

    1.  Navigate to **HR Integrations** &gt; **HR Outbound Schema Mapping**.

    2.  Right-click the **Source Table** column and select **Group By Source Table**.

    3.  For the HR Talent Management Case \[sn\_hr\_core\_case\_talent\_management\] group, click the arrow to expand the list.

    4.  Click the information icon for each Sterling record to verify that the data fields from the source tables are correctly mapped to the appropriate fields in Sterling.

3.  Verify the HR schema mappings.

    1.  Navigate to **HR Integrations** &gt; **HR Schema Mapping**.

    2.  Right-click the **Source** column and select **Group By Source**.

    3.  For the **Sterling** group, click the arrow to expand the list.

    4.  For each record, click the information icon to verify that the data fields from Sterling are correctly mapped to the appropriate fields in the staging tables.

4.  Verify the HR transform maps.

    1.  Navigate to **HR Integrations** &gt; **HR Transform Maps**.

    2.  In the **Table Transform Maps** list, verify that the staging tables are correctly mapped to the appropriate target tables.

        |Staging table|Target table|
        |-------------|------------|
        |HR Integrations Background Check Staging \[sn\_hr\_integrations\_background\_check\_staging\]|HR Talent Management Case \[sn\_hr\_core\_case\_talent\_management\]|


**Parent Topic:**[Integrating with the Sterling Talent Solutions service](../concept/integrate-with-sterling-service.md)

**Previous topic:**[Provide source credentials for the Sterling service](hr-integrations-sources-sterling.md)

**Next topic:**[Add background check packages for the Sterling service](background-check-package-for-sterling.md)

