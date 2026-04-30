---
title: Configure Authentication profile for Processor
description: Apply authentication profile for the export processors.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access policy for System/Export Processors, API access policy, Authentication, Access Management]
---

# Configure Authentication profile for Processor

Apply authentication profile for the export processors.

## Before you begin

Role required: admin

Plugin required: Processor Access Policy \(`com.glide.processor.policy`\)

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Process Access Policies**.

2.  To add authentication profile to the processor, click **New**.

3.  On the form, fill in the fields.

<table id="table_kjk_gb5_d4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Processor

</td><td>

Name to identify the authentication policy.**Note:** Public processors are not supported. If a non-supported processor is selected, then an error is displayed during submission of the processor.

</td></tr><tr><td>

Application

</td><td>

Scope of the authentication policy. Default: Global

</td></tr><tr><td>

Authentication Profile

</td><td>

Type of the authentications profile. You can select **ID Token** or **OAuth Token**.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The authentication profile is applied to the processor.

    For example, OAuth authentication profile is configured for the CSV Processor. In this case, you have to use OAuth access token for the exporting using CSV as an export option.

    ![Processor Access Policies](../images/auth-profile-processor.png)


