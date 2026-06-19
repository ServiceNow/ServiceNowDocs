---
title: Import and export foundation data sync configuration
description: Export ETL configurations for foundation data sync \(FDS\) from one instance to another using update sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/service-exchange/import-and-export-fds-configuration.html
release: zurich
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure FDS as a consumer, Install and configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Import and export foundation data sync configuration

Export ETL configurations for foundation data sync \(FDS\) from one instance to another using update sets.

## Before you begin

FDS requires the following fields on a subscription to be identical in both the exporting and importing instances to support linking or using imported configurations:

-   Offering definition name
-   List of tables offered as part of the offering
-   Cadence in subscription
-   Provider company name
-   FDS compatibility.

Also, the offering definition and connection company must be identical in both the exporting and importing instances.

Role required: admin

## About this task

You can export ETL configurations from one instance and import them into another. For example, you can configure ETL in a pre-production environment and then export those configurations and import them into a production environment. FDS supports this transfer through update sets, which enable seamless reuse of configurations.

## Procedure

1.  Export the ETL configuration.

    1.  Create a local update sets and mark it as current.

    2.  Request a foundation data sync \(FDS\) offering, complete the configuration, and verify that the data sync is working correctly.

        For more information on how to request a foundation data sync \(FDS\) offering, see [Request foundation data sync offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-request-fds-offerings.md).

    3.  Complete the update sets and export it.

        For more information on update sets, see .

2.  Import the ETL configuration to another instance.

    1.  In the new instance, request a foundation data sync \(FDS\) offering with same cadence as in [Step 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/import-and-export-fds-configuration.md).

    2.  After a subscription is created for your FDS request, and the request is in awaiting validation state, import the configuration that you have exported in Step 1.

        If you have any errors in the update sets, you can skip those files and commit the remaining files. Your configuration won't be affected. For more information on update sets, see .

    3.  Open the subscription and the subscription item.

    4.  Select **ETL Transform Map Assistance**.

        In the guided setup, step 1, step 2, and step 3 are marked as completed. For more information, see [Validate foundation data sync subscription items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-validate-fds-subscription.md)

    5.  Verify all the steps in ETL configuration to make sure everything is mapped correctly, and run the integration and perform rollback.

        For details, see .


