---
title: Create verification settings
description: Create a verification type in the base system to authenticate the user credentials while resetting the password.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the verification methods for service desk process in Service Operations Workspace, Setting up Service Desk assisted Password Reset in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Create verification settings

Create a verification type in the base system to authenticate the user credentials while resetting the password.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Overview**.

2.  On the **Admin Center** page, do one of the following:

    -   In the **Overview** tab, select the **Configure** button in the **Service Desk Assisted Password Reset** card.
    -   In the **Configurations** tab, select **Service Desk Assisted Password Reset** card.
3.  On the **Verification Settings** card, select **Configure** for Verification\(s\).

    The default password reset verifications are displayed.

4.  Select **New** to create a new password reset verification method.

5.  On the form, fill in the fields.

<table id="table_epm_p3n_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the password verification method.

</td></tr><tr><td>

Description

</td><td>

Detailed information of the password verification method.

</td></tr><tr><td>

Label

</td><td>

Option to provide a label for the verification method.

</td></tr><tr><td>

Type

</td><td>

Verification types available in the base system.

 Password Reset supports the following types.

 -   Personal Data Confirmation Verification
-   Personal Data Verification
-   Security Question Verification
-   SMS Code Verification
-   Email code verification


</td></tr><tr><td>

Password Reset Verification Parameters

</td><td>

Parameters used by a verification to configure specific behaviors, like number of questions required to enroll, request expiration time, and columns used.

 Set parameters for any behavior that should be different from the value that is specified in the Password Reset properties.

</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Configure the verification methods for service desk process in Service Operations Workspace](../concept/configuring-verification-methods-pr-sow.md)

