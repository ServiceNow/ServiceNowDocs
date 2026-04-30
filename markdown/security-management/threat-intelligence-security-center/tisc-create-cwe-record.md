---
title: Create a CWE record
description: Create a Common Weakness Enumeration \(CWE\) record to represent a weakness identified in a system or product, and link it to relevant vulnerabilities.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-02-25"
reading_time_minutes: 1
breadcrumb: [Vulnerability, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a CWE record

Create a Common Weakness Enumeration \(CWE\) record to represent a weakness identified in a system or product, and link it to relevant vulnerabilities.

## Before you begin

Role required: sn\_sec\_tisc.analyst

You must have the appropriate role to create records in the threat intelligence library.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Library** &gt; **Vulnerability Artifacts** &gt; **CWEs**.

2.  Click **New**.

3.  Fill in the fields appropriately.

<table id="table_r4t_s3g_k3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Enter a unique identifier for the CWE.**Note:** The ID is pre-populated with the `CWE#` prefix. Append a unique numeric or alphanumeric value. The system validates uniqueness on save and prevents duplicate IDs.

</td></tr><tr><td>

Name

</td><td>

Name of the CWE weakness.

</td></tr><tr><td>

Description

</td><td>

Enter the description.

</td></tr><tr><td>

Type

</td><td>

Select a **Type**: **Primary** or **Secondary**.**Note:** The type indicates whether this CWE is a primary or secondary weakness as defined by the NVD schema.

</td></tr></tbody>
</table>4.  Click **Save**.

5.  To link vulnerabilities to this CWE, scroll to the **Vulnerabilities** related list and click **Link**.

6.  To link related CWEs, scroll to the **Related Records** &gt; **CWEs** related list and click **Link**.


**Parent Topic:**[Vulnerability](../concept/vulnerability.md)

