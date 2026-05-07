---
title: Working on the Redaction Library
description: Redaction is the process of replacing sensitive information from shared data to protect confidentiality during intelligence sharing.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Working on the Redaction Library

Redaction is the process of replacing sensitive information from shared data to protect confidentiality during intelligence sharing.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

This feature allows the you to redact or replace sensitive or personalized information with specific values.

Within the outbound intelligence sharing record, you can apply redaction library to automatically filter out specific attributes or content before the payload is generated.

In Threat intelligence sharing, the sensitive information which is defined as redaction category values, and is replaced with the corresponding redaction category.

This is especially useful when sharing data with external organizations, where only the relevant and non-sensitive information should be disclosed.

By leveraging the Redaction Library feature, TISC administrators and analysts can define reusable redaction configurations and apply them consistently across multiple sharing templates.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Administration** icon on the workspace.

3.  Go to **Outbound Intel Sharing**.

4.  Select **Redaction Library**.

    The Redaction Library list view is displayed.

5.  Select **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Redaction Category|Specify the redaction category for the outbound intelligence sharing record.|
    |Status|The status of the redaction category. By default, all the redaction categories are enabled. However, you can choose to disable a specific redaction category.|

7.  Click **Save**.

8.  Go to **Redaction Category Values** section.

9.  Select **New** to create Redaction Category Value record.

<table id="choicetable_qsf_s3c_qfc"><thead><tr><th align="left" id="d383923e204">

Field

</th><th align="left" id="d383923e207">

Description

</th></tr></thead><tbody><tr><td id="d383923e213">

**Redaction Category**

</td><td>

Indicates the redaction category. Few examples of Redaction Category are as follows:

-   IP Address \(IPv4/IPv6\)
-   Organization\_Name
-   Domain Name
-   Email Address
-   Identification\_Number


</td></tr><tr><td id="d383923e241">

**Value**

</td><td>

Indicates the value that needs to be redacted.

</td></tr></tbody>
</table>10. **System Property for Redaction Library**:

<table id="table_m3s_bwf_qfc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sec\_tisc.case\_sensitive\_for\_redaction

</td><td>

This property enables or disables case sensitivity when applying redaction to shared intelligence.Default: Disabled \(`false`\), meaning redaction is case insensitive by default.

**Note:** By default, this property is disabled making the redaction case insensitive. For example, Service\_Now and service\_now would both be redacted equally. Enabling it \(`true`\) means the redaction will only apply if the case matches exactly.

</td></tr></tbody>
</table>11. Select **Save**.


-   **[Bulk Import of Redaction Categories and Values](tisc-bulk-import-redaction.md)**  
Import redaction categories. Bulk importing of redaction categories and their associated values.

**Parent Topic:**[Exploring Outbound Intel Sharing](../concept/tisc-outbound-intel-sharing.md)

**Related topics**  


[Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md)

[Configuring Outbound Intel Data Exclusion Rule](tisc-outbound-data-exclusion.md)

[Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md)

[Configuring Outbound Intel Sharing Groups](tisc-config-inbound-sharing-groups.md)

[Defining Approval Rule for Outbound Intel](tisc-approval-outbound-intel.md)

[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

