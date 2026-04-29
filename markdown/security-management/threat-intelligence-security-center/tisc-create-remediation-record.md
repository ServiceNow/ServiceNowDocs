---
title: Create Remediations
description: Create a remediation record to document a fix or workaround for a vulnerability affecting a specific product.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Vulnerability Artifacts, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create Remediations

Create a remediation record to document a fix or workaround for a vulnerability affecting a specific product.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

At least one vulnerability record and one product record must exist in the system before creating a remediation. Remediations are always created in the context of a vulnerability and product combination.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Library** &gt; **Vulnerability Artifacts** &gt; **Remediations**.

2.  Select **New**.

3.  Fill in the fields appropriately.

<table id="table_qjq_dlg_k3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remediation Id

</td><td>

A unique identifier for the remediation record.

</td></tr><tr><td>

Products

</td><td>

The product or products to which this remediation applies.

</td></tr><tr><td>

Vulnerability

</td><td>

The vulnerability that this remediation addresses.

</td></tr><tr><td>

Type

</td><td>

The category of remediation being documented.-   **Mitigation**: a workaround or partial fix.
-   **Workaround**: a temporary measure.
-   **Vendor Fix**: an official fix from the vendor.
-   **First Fix**: the initial fix available for the vulnerability.
-   **None Available**: no remediation is currently available.
-   **No Fix Planned**: the vendor does not plan to fix the vulnerability.


</td></tr><tr><td>

Description

</td><td>

Description of the remediation, including what it addresses and how it should be applied.

</td></tr><tr><td>

Remediation Published Date

</td><td>

The date on which this remediation was officially published.

</td></tr><tr><td>

Restart category

</td><td>

Indicates what category of restart is required by this remediation to become effective.Select one of the following values, as required:

-   **Connected**: a connected dependency requires a restart.
-   **Dependencies**: dependent services or components must be restarted.
-   **Machine**: the entire machine requires a restart.
-   **Service**: a specific service must be restarted.
-   **System**: the full system requires a restart.
-   **None**: no restart is required.


</td></tr><tr><td>

Action Link

</td><td>

A URL pointing to the remediation resource, advisory, or vendor patch page.Enter a fully qualified URL \(for example, `https://vendor.com/advisory/CVE-2024-1234`\). Use this field to direct users to external remediation guidance or download locations.

</td></tr><tr><td>

Prerequisites

</td><td>

Lists the conditions that must be met for the vulnerability remediation to apply to this product.Use this field to document preparatory actions such as backing up data, stopping services, or verifying system compatibility. All prerequisite values are entered manually.

</td></tr></tbody>
</table>4.  Click **Save**.

5.  To also add **Remediations**, navigate to **Threat Intel Library** &gt; **Vulnerability Artifacts** and open any vulnerability record or product record to which you want to add a remediation.

6.  Go to the **Related Records** section.

7.  Scroll to the **Remediations** related list and click **Add**.

    Clicking **Add** opens the remediation form in a new tab. The parent context \(vulnerability or product\) is automatically populated in the corresponding field. Enter the required form details as explained in the previous steps.

8.  Click **Save**.


## Result

The remediation record is created and appears in the **Remediations** related list of the associated vulnerability and product records. The **Remediated Records Count** field on the vulnerability record is automatically incremented.

**Parent Topic:**[Vulnerability Artifacts](../concept/vulnerability.md)

