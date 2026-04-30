---
title: The Tenable Vulnerability Integration with Configuration Compliance
description: The Tenable.io product of the Tenable Vulnerability Integration imports policies, controls \(test results\), and configuration tests for processing in the Configuration Compliance application.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuration Compliance imported data, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# The Tenable Vulnerability Integration with Configuration Compliance

The Tenable.io product of the Tenable Vulnerability Integration imports policies, controls \(test results\), and configuration tests for processing in the Configuration Compliance application.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Tenable.io

The Tenable Vulnerability Integration is supported.

You can use imported data to:

-   Identify configuration-related vulnerabilities on your assets listed in your Configuration Management Database \(CMDB\)
-   Verify that your assets are in compliance with your policies and controls.

Assets data, policies, controls \(test results\), and configuration tests are imported with the following integrations:

-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Integration
-   Tenable.io Compliance Results Backfill Integration

The following image illustrates how the integrations work together to import asset and configuration assessment data and reconcile any ignored CIs overlooked during an import.

![Sequence for the three tenable integrations, Assets, Configuration Compliance Results, and Compliance Results Backfill to update test, policy, and test result records](../../secops-integration-vr/tenable/image/vr-tenable-cc-data.png "Import flow for secure configuration assessment results")

Data is imported, updated, and displayed on the test result, policy, and configuration test records in the Configuration Compliance application.

In some cases, the number of imported Configuration Items \(CIs\) is different for the Tenable.io Assets Integration and the Tenable.io Compliance Results Integration. When this occurs, temporary records are created and stored for the ignored asset IDs. These records can be matched later with imported assessment data by imports from the Compliance Results Backfill Integration.

For example, let's say the Assets Integration imports 80 assets on an integration run, but the Compliance Results Integration imports 100.

**Note:** You can verify the number of ignored CIs on integration runs by navigating to **Tenable Vulnerability Integration** &gt; **Administration** &gt; **Integrations**. Click the name of an integration to open the record. On the **Vulnerability Integration Runs** Related Link, open an integration run record and select the **Items** tab to see the value in the **Ignored CIs** field. This field tracks the total of ignored \(missing\) assets from the import.

By comparing values in the **Ignored CIs** fields on each integration run record, there is a difference of 20 ignored CIs. As a result, the backfill integration runs automatically as shown in the preceding image. This integration imports the configuration assessment information for the extra 20 assets found by the Compliance Results Integration but missed by the Assets Integration. Since assessment data for missing assets is not imported, the Tenable.io Compliance Results Backfill Integration imports up to 200 Asset IDs per integration run to reconcile the missing assets with their corresponding assessment data. All records created for missing or ignored assets and listed on the temporary table are deleted after these assets and their data are matched.

**Note:** It may take multiple runs of these integrations to import all the ignored assets.

For more information about how to enable and configure the Tenable.io Asset Integration, see [Configure the Tenable Vulnerability Integration using Setup Assistant](../../secops-integration-vr/tenable/task/vr-tenable-config-in-SA.md). See [Understanding the Tenable Vulnerability Integration](../../secops-integration-vr/tenable/concept/tenableIntegration.md) for more information about the integration.

The Tenable.io Compliance Results Integration and the Tenable.io Compliance Results Backfill Integration are inactive by default.

To activate them:

1.  Navigate to **Tenable Vulnerability Integration** &gt; **Administration** &gt; **Integrations**.
2.  On the Tenable Integrations list, click an integration name to open the record and select the **Active** check box to enable it. You might prefer to leave the schedule settings in their default values for these integrations to start.

