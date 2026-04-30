---
title: Configure remediation policies on tag audit findings
description: Configure and preview remediation options, generate keys, and perform actions to remediate non-compliance or failures that are based on tag audit reports.
locale: en-US
release: zurich
product: Tag Governance
classification: tag-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Establishing Tag Governance policies, Using Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Configure remediation policies on tag audit findings

Configure and preview remediation options, generate keys, and perform actions to remediate non-compliance or failures that are based on tag audit reports.

## Before you begin

Ensure that tag policies are configured and in Active state.

Role required: sn\_itom\_tag.tag\_governance\_admin, admin

## About this task

You can run remediation automatically if you map a remediation policy to a tag policy. You can also update the tags of non-compliant CIs at the cloud provider's end in real time.

Configure remediation policies and logic and also enable updating tags on cloud resources associated with the following CMDB classes:

-   Virtual Machines
-   Compute Security Groups
-   Storage Volumes
-   Cloud Networks
-   Cloud Subnet
-   Network Interfaces
-   Load Balancers
-   Availability Zones
-   Public IP addresses
-   Storage Accounts
-   Resource Groups

The list of CMDB classes for which you can update tags on CIs in the CMDB as well as cloud resources also displays on the Tag Remediation form. If you select the **Update Tags in Cloud** check box in the Remediation form, remediation will only preview CI failures belonging to the CMDB classes listed.

## Procedure

1.  Navigate to **All** &gt; **Tag Governance** &gt; **Remediation**.

2.  Select **New** to create a new record.

3.  In the **Name** field, provide a unique descriptive name.

4.  In the **Policy** field, select the ![Lookup icon](../image/IconUI16ReferenceLookup.png) lookup icon.

    **Note:** The **Policy Type** field is automatically populated after you select a policy from the lookup list.

5.  In the Tag Policies list, configure a remediation policy in one of the following ways:

    -   Select an existing tag policy from the lookup list.
    -   Select **New**. Fill in fields on the Tag Policies form \(the fields are described in [Tag Policies form](../../itom-cloud-accelerate/reference/tag-gov-tag-policies-form.md).

        **Note:** If you are creating a new tag policy, you must run an audit before you can run remediation flows.

    You have created or selected a policy for the remediation record.

6.  Select the **AutoRemediation** check box to automatically run remediation on non-compliant CIs.

    When an audit run finishes, remediation runs on all CIs with policy failures.

7.  Select the **Update Tags in Cloud** check box to apply remediation and update the tags in the relevant cloud provider environment for supported CMDB CI classes.

    **Important:** The **Update Tags in Cloud** feature works only for AWS and Microsoft Azure Cloud resources for CMDB classes listed in the Tag Remediation form. See [Performing real-time updates to tags for cloud resources](../concept/tag-governance-real-time-updates.md).

8.  On the Tag Remediation form, select **Submit**.

    The remediation policy is configured. The Tag Remediations list opens.


