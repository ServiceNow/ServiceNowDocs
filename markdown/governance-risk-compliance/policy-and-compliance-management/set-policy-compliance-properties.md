---
title: Set Policy and Compliance Management properties
description: Set properties to control various aspects and behaviors in the software.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Perform Policy and Compliance Management administration, Implementing Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Set Policy and Compliance Management properties

Set properties to control various aspects and behaviors in the software.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Properties**.

<table id="table_ght_bmm_vs"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

States for which the control is active \(the first state is the default active state\)sn\_compliance.active\_states

 **Note:** Controls in active states only, as mentioned in this property, are considered during compliance score calculation.

</td><td>

Compliance administrators can change this setting.-   Type: string
-   Default value: draft, assess, review, monitor
-   Location: **Policy and Compliance** &gt; **Administration** &gt; **Properties**


</td></tr><tr><td>

States for which control is inactive \(the first state is the default inactive\)sn\_compliance.closed\_states

 **Note:** Controls in inactive states, as mentioned in this property, are not considered during compliance score calculation.

</td><td>

Compliance administrators can change this setting.-   Type: string
-   Default value: retired
-   Location: **Policy and Compliance** &gt; **Administration** &gt; **Properties**


</td></tr><tr><td>

Name of the assessment metric type that is used for attestationssn\_compliance.default\_attestation

</td><td>

System administrators can change this setting.-   Type: string
-   Default value: GRC Attestation
-   Location: **Policy and Compliance** &gt; **Administration** &gt; **Properties**


</td></tr><tr><td>

This is a platform-level system property that is used to run client scripts in strict mode with direct DOM disabled. When this property is set to true, you cannot use jquery or change the DOM directly. sn\_compliance.glide.script.block.client.globals

</td><td>

-   Type: true or false
-   Default value: false
-   Location: **Policy and Compliance** &gt; **Administration** &gt; **Properties**


</td></tr><tr><td>

Name of the knowledge base used to publish Policy articlessn\_compliance.knowledge\_base

</td><td>

Compliance administrators can change this setting.-   Type: string
-   Default value: Governance, Risk, and Compliance
-   Location: **Policy and Compliance** &gt; **Administration** &gt; **Properties**


</td></tr></tbody>
</table>
## What to do next

Return to the [Policy and Compliance Management setup checklist](policy-compliance-impl-checklist.md).

**Parent Topic:**[Perform Policy and Compliance Management administration](../concept/perform-policy-compliance-admin.md)

