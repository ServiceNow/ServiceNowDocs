---
title: Define policy reason mappings
description: You can define the reason choices to be available to any user who requests an exception.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Requesting and approving an exception for a remediation task, Remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Define policy reason mappings

You can define the reason choices to be available to any user who requests an exception.

## Before you begin

Role required: sn\_vul.compliance.manager and sn\_vulc.admin

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policy Exceptions** &gt; **Integration Registry**.

    **Note:** You can either select a reason from the reason choices available in the Reason Choices table or add a new reason.

2.  Click the Container Vulnerability Response - CVIT integration registry.

3.  To add an existing reason choice, perform the following steps:

    1.  In the Reason Choices list, click **New**.

    2.  Click the magnifying glass icon to select a reason.

4.  To add new reason choices to the Reason Choices table, perform the following steps:

    1.  In Reason Choices list, click **New**.

    2.  Click the magnifying glass icon.

    3.  Click **New**.

    4.  On the form, fill in the fields.

<table id="table_sl1_hh3_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label for this choice.

</td></tr><tr><td>

Value

</td><td>

Unique value for this choice.

 This value is mapped in the Policy Exception Reason Mappings table for the respective applications. To navigate to this table, enter sn\_sec\_cmn\_policy\_reason\_mapping.LIST in the filter navigator.

</td></tr><tr><td>

Order

</td><td>

Order for this choice. Reasons are ordered based on this number.

</td></tr><tr><td>

Default

</td><td>

Option to indicate that this reason choice will be available whenever an on demand policy exception is requested. If the integration registry doesn’t contain any application-specific choices, then all reason choices that have the **Default** field selected will be available.

</td></tr><tr><td>

Active

</td><td>

Option to display the choice in the list of reason choices.

</td></tr></tbody>
</table>5.  Click **Submit**.


