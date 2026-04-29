---
title: Import and export foundation data sync configuration
description: Export ETL configurations for foundation data sync \(FDS\) from one instance to another using update sets.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring inbound FDS as consumers, Configure for consumers, Service Exchange for Consumers, Service Exchange]
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

        For more information on how to request a foundation data sync \(FDS\) offering, see [Request foundation data sync offerings](service-bridge-v2-request-fds-offerings.md).

    3.  Complete the update sets and export it.

        For more information on update sets, see [General guidelines for planning the update process](https://www.servicenow.com/docs/access?context=get-started-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US).

2.  Import the ETL configuration to another instance.

    1.  In the new instance, request a foundation data sync \(FDS\) offering with same cadence as in [Step 1](import-and-export-fds-configuration.md#substeps_dwc_5l1_cgc).

    2.  After a subscription is created for your FDS request, and the request is in awaiting validation state, import the configuration that you have exported in Step 1.

        If you have any errors in the update sets, you can skip those files and commit the remaining files. Your configuration won't be affected. For more information on update sets, see [General guidelines for planning the update process](https://www.servicenow.com/docs/access?context=get-started-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US).

    3.  Open the subscription and the subscription item.

    4.  Select **ETL Transform Map Assistance**.

        In the guided setup, step 1, step 2, and step 3 are marked as completed. For more information, see [Validate foundation data sync subscription items](service-bridge-v2-validate-fds-subscription.md)

    5.  Verify all the steps in ETL configuration to make sure everything is mapped correctly, and run the integration and perform rollback.

        For details, see [IntegrationHub ETL](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).


