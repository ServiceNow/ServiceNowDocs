---
title: Verify integration for the Accurate service
description: The integration is configured to push background check data between the HR service in HR Service Delivery and the Accurate service. You can verify the preconfigured settings and determine whether they meet your needs or if further customization is required.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-11-14"
reading_time_minutes: 3
breadcrumb: [Integrating with the Accurate Background service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Verify integration for the Accurate service

The integration is configured to push background check data between the HR service in HR Service Delivery and the Accurate service. You can verify the preconfigured settings and determine whether they meet your needs or if further customization is required.

## Before you begin

**Important:** Integrating with the Accurate Background service is being prepared for deprecation. It will be hidden and unavailable for activation from Zurich, but will continue to be supported till Brazil. If you have an active subscription, you can still activate the plugin by submitting a [plugin activation request](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/plugins/task/t_RequestAPlugin.html). For more details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: sn\_hr\_integrations.admin

## Procedure

1.  Verify the HR service mappings, which maps the HR service or HR integration outbound services to the HR web services.

    1.  Navigate to **HR Integrations** &gt; **HR Service Mapping**.

    2.  Right-click the **HR external source** column and select **Group By HR external source**.

    3.  For the **Accurate** group, click the arrow to expand the list.

    4.  For each record, click the information icon to verify that the HR service or HR integration outbound services are correctly mapped to the appropriate HR web services.

        **Note:** Make sure to verify the endpoint URL for the **Accurate Background Check API** record.

        |HR service mapping|HR service or HR integration outbound service|HR web service|
        |------------------|---------------------------------------------|--------------|
        |Accurate Background Check - Accurate Background Check - Get Order Updates|Accurate Background Check - Get Order Updates|Accurate Background Check API|
        |Accurate Background Check - Accurate Background Check - Get Report Data|Accurate Background Check - Get Report Data|Accurate Background Check API|
        |Accurate Background Check - Accurate Background Check - Place Order|Accurate Background Check - Place Order|Accurate Background Check API|
        |Accurate Background Check - Request Background Check by Accurate|Request Background Check by Accurate|Accurate Background Check API|

2.  Verify the HR outbound schema mappings.

    1.  Navigate to **HR Integrations** &gt; **HR Outbound Schema Mapping**.

    2.  Right-click the **Source Table** column and select **Group By Source Table**.

    3.  For the HR Talent Management Case \[sn\_hr\_core\_case\_talent\_management\] group, click the arrow to expand the list.

    4.  Click the information icon for each Accurate record to verify that the data fields from the source tables are correctly mapped to the appropriate fields in Accurate.

3.  Verify the HR schema mappings.

    1.  Navigate to **HR Integrations** &gt; **HR Schema Mapping**.

    2.  Right-click the **Source** column and select **Group By Source**.

    3.  For the **Accurate** group, click the arrow to expand the list.

    4.  For each record, click the information icon to verify that the data fields from Accurate are correctly mapped to the appropriate fields in the staging tables.

4.  Verify the HR transform maps.

    1.  Navigate to **HR Integrations** &gt; **HR Transform Maps**.

    2.  In the **Table Transform Maps** list, verify that the staging tables are correctly mapped to the appropriate target tables.

        |Staging table|Target table|
        |-------------|------------|
        |HR Integrations Background Check Staging \[sn\_hr\_integrations\_background\_check\_staging\]|HR Talent Management Case \[sn\_hr\_core\_case\_talent\_management\]|


**Parent Topic:**[Integrating with the Accurate Background service](../concept/integrate-with-accurate-service.md)

**Previous topic:**[Provide source credentials for the Accurate service](hr-integrations-sources-accurate.md)

**Next topic:**[Add background check packages for the Accurate service](background-check-package-for-accurate.md)

