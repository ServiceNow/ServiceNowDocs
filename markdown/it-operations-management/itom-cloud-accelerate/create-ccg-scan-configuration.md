---
title: Create a scan configuration
description: Create a scan configuration in Cloud Configuration Governance to scan the cloud resources against one or more policy sets and identify the policy violations.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scan configuration, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a scan configuration

Create a scan configuration in Cloud Configuration Governance to scan the cloud resources against one or more policy sets and identify the policy violations.

## Before you begin

-   Ensure that a suitable policy set is available for the scan. The policy set enforces a given security or organizational standard. For more information on creating the policy set, see [Create a policy set](create-ccg-policy-set.md).
-   Role required: sn\_itom\_ccg.scheduling\_admin

## About this task

**Note:** Starting with Cloud Configuration Governance version 1.3.7, the base system contents are moved to the CCG Content Pack. Install the CCG Content Pack to access the base system Cloud Configuration Governance contents.

## Procedure

1.  Navigate to **Cloud Configuration Governance** &gt; **Scan Configurations**.

2.  Select **New**.

3.  Fill the values on the Scan Configuration form.

    For a description of the form fields, see [Cloud Configuration Governance Scan configuration form](../reference/ccg-scan-configuration-form.md).

4.  Select **Submit**.

5.  To create a schedule to execute the scan configuration, select **Setup Schedule**.

    1.  Set a criteria to cancel the long running scan runs.

        To import the configuration data of the cloud resources, Cloud Configuration Governance resource collectors and configuration collectors use Workflow Studio subflows. Sometimes, the subflow errors out and it doesn't report the error. In such cases, the scan run can run indefinitely. Setting a cancellation criteria helps to cancel such scans.


## What to do next

Run the scan configuration to evaluate the resource configuration of the given cloud against the specified policy sets and identify the policy violations. For more information, see [Run the scan configuration](run-ccg-scan-configuration.md).

