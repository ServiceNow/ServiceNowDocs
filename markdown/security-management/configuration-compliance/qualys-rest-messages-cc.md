---
title: Qualys REST messages
description: Qualys REST messages are used to make calls to the Qualys API to fetch the compliance data.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Qualys, Integrate with other applications, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Qualys REST messages

Qualys REST messages are used to make calls to the Qualys API to fetch the compliance data.

The following rest messages are shipped with the base system.

## Qualys PC Policies REST message

The Qualys PC Policies REST message retrieves policy data from Qualys. The changes to the REST message method record impact the request made to Qualys to retrieve policy information.

Starting with v12.21.0 of Qualys Integration for Security Operations and v30.3.0 of Unified Security Exposure Management, the API version has been updated to version 5.0.

<table id="table_v2g_x1q_dt"><thead><tr><th>

Parameter Name

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

list

</td><td>

Indicates the type of operation requested. Required parameter.

</td></tr><tr><td>

details

</td><td>

All

</td><td>

Indicates the level of detail shown for policies retrieved.

 It is safe to modify as per your requirement.

</td></tr></tbody>
</table>## Qualys PC Controls REST message

The Qualys PC Controls rest message retrieves compliance controls information for different control IDs from Qualys.

<table id="table_n3s_b1p_mxb"><thead><tr><th>

Parameter Name

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

list

</td><td>

Indicates the type of operation requested. Required parameter.

</td></tr><tr><td>

details

</td><td>

All

</td><td>

Indicates the level of detail shown for controls retrieved.

 It is safe to modify as per your requirement.

</td></tr></tbody>
</table>## Qualys PC Policies Detail REST message

The Qualys PC Policies Detail REST message retrieves the complete policy details, such as technologies and sections.

Starting with v12.21.0 of Qualys Integration for Security Operations and v30.3.0 of Unified Security Exposure Management, the API version has been updated to version 5.0.

<table id="table_v2g_x1q_du"><thead><tr><th>

Parameter

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

list

</td><td>

Indicates the type of operation being requested. Required parameter.

</td></tr><tr><td>

show\_user\_controls

</td><td>

Boolean

</td><td>

-   Set to 1 to include user-defined controls \(UDCs\) in the XML output.
-   When not specified, UDCs are not included.


 This is an optional parameter. It is safe to modify as per your requirement.

</td></tr><tr><td>

show\_appendix

</td><td>

Boolean

</td><td>

\(Optional\) Set to 1 to show the appendix section in the XML output. When unspecified.

</td></tr></tbody>
</table>## Qualys PC Results REST message

The Qualys PC Results rest message retrieves compliance posture records from Qualys.

<table id="table_v2g_x1q_dv"><thead><tr><th>

Source Field

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

list

</td><td>

Indicates the type of operation requested. Required parameter. Changes are not recommended.

</td></tr><tr><td>

show\_extended\_evidence

</td><td>

Boolean

</td><td>

-   Set to 1 to show the extended evidence information in the output.
-   Set to 0 or when unspecified, the extended evidence information is not shown in the output.

 **Note:**

-   You cannot specify `show_extended_evidence=1` in the same request as `hide_evidence=1`. This results in an error. The extended evidence is a part of the evidence data and it’s shown only when evidence data is shown.
-   This parameter is not shipped with the base system.

</td></tr><tr><td>

cause\_of\_failure

</td><td>

Boolean

</td><td>

If you pass '1', Qualys will return the cause of failure.

 If you pass '0', Qualys will not return these attributes.

 **Note:** This parameter is not shipped with the base system.

</td></tr><tr><td>

policy\_id

</td><td>

 

</td><td>

Shows compliance posture information records for a specified policy. A valid policy ID is required.

</td></tr><tr><td>

details

</td><td>

All

</td><td>

Indicates the level of detail shown for postures retrieved.

 It is safe to modify as per your requirement.

</td></tr><tr><td>

show\_remediation\_info

</td><td>

 

</td><td>

\(Optional\) Set to 1 to show remediation information in the XML or CSV output. By default, the output does not include the remediation information. When not specified, the remediation information is not included in the output.

</td></tr></tbody>
</table>## Qualys PCRS Policy Host Integration REST message

The Qualys PCRS Policy Host Integration retrieves host data from Qualys and processes it in your instance.

Starting with v12.21.0 of Qualys Integration for Security Operations and v30.3.0 of Unified Security Exposure Management, the API version has been updated to version 5.0.

<table id="table_v2g_x1q_dw"><thead><tr><th>

Parameter Name

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

policyId

</td><td>

$\{lastRunDatetime\}

</td><td>

Policy IDs for compliance evaluation.

</td></tr></tbody>
</table>## Qualys PCRS Test Results Integration

The table shows the request parameters that are sent.

Starting with v12.21.0 of Qualys Integration for Security Operations and v30.3.0 of Unified Security Exposure Management, the API version has been updated to version 5.0.

<table id="table_bpb_pgp_mxb"><thead><tr><th>

Parameter Name

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

evidenceRequired

</td><td>

1

</td><td>

-   The default value is 1, which indicates that evidence data will be retrieved for the host posture.
-   Set the value to 0 to retrieve the evidence data.

**Note:** Changing the value to 1 increases the time required to fetch posture data.


</td></tr><tr><td>

compressionRequired

</td><td>

0

</td><td>

-   The default value is 0, which indicates that the output will not be compressed.
-   Set the value to 1, if you want the data to be compressed.

**Note:** Not compressing the data increases the time required to fetch posture data.


</td></tr></tbody>
</table>## Qualys Comprehensive PCRS Policy Host Integration REST message

The Qualys Comprehensive PCRS Policy Host Integration retrieves host data from Qualys and processes it in your instance.

Starting with v12.21.0 of Qualys Integration for Security Operations and v30.3.0 of Unified Security Exposure Management, the API version has been updated to version 5.0.

| | | |
|---|---|---|
|policyId|$\{policyId\}|Policy IDs for compliance evaluation.|

## Qualys Comprehensive PCRS Test Results Integration

The table shows the request parameters that are sent.

Starting with v12.21.0 of Qualys Integration for Security Operations and v30.3.0 of Unified Security Exposure Management, the API version has been updated to version 5.0.

<table id="table_kmd_ppw_l3c"><thead><tr><th>

Parameter Name

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

evidenceRequired

</td><td>

1

</td><td>

-   The default value is 1, which indicates that evidence data will be retrieved for the host posture.
-   Set the value to 0 to retrieve the evidence data.

**Note:** Changing the value to 1 increases the time required to fetch posture data.


</td></tr><tr><td>

compressionRequired

</td><td>

0

</td><td>

-   The default value is 0, which indicates that the output will not be compressed.
-   Set the value to 1, if you want the data to be compressed.

**Note:** Not compressing the data increases the time required to fetch posture data.


</td></tr></tbody>
</table>