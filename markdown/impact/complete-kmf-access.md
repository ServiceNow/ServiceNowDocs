---
title: Grant Key Management Framework access on an instance
description: Give the setup user KMF roles and approve the Scan Engine decryption policy so that imported credentials can be decrypted on the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/complete-kmf-access.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 2
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Grant Key Management Framework access on an instance

Give the setup user KMF roles and approve the Scan Engine decryption policy so that imported credentials can be decrypted on the instance.

## Before you begin

This task must be completed on each instance that receives imported OAuth or basic authentication records, before you select **Validate Connection**.

Role required: admin and security\_admin

## About this task

KMF encrypts `password_2` fields with a key that exists only on the instance that created them. When you import a record from another instance, the password can't be decrypted until you re-enter it on the receiving instance. A pending or rejected Scan Engine decryption policy blocks decryption as well, and the connection validation fails with the error `User not set up on target instance`.

**Important:** You need the KMF admin role, `sn_kmf.admin`, to complete these steps. It is an elevated privilege that isn't assigned like other roles. A user with the `admin` and `security_admin` roles assigns it after elevating to `security_admin`, and your organization decides who receives it. For instructions, see [Assign Key Management Framework roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/assign-kmf-roles.md).

## Procedure

1.  In the navigator, enter `key` and select **Key Management Administration**.

2.  Add your user account to the selected users list, then select **Save**.

    The `sn_kmf.admin` role is assigned to your account.

3.  Log out, then log back in.

4.  Open your user record.

5.  In the **Roles** related list, select **Edit**, add `sn_kmf.cryptographic_manager`, and select **Save**.

6.  Log out, then log back in to activate both roles.

7.  Navigate to `sys_script_include.list`, filter on **Name** for `ScanEngineApiUtil`, and open the record.

    The script include API name is `sn_se.ScanEngineApiUtil`. The **Name** column shows `ScanEngineApiUtil` without the scope prefix.

    Copy the record's **sys\_id** for the next step.

8.  Navigate to **All** &gt; **Key Management Framework** &gt; **Module Access Policies** &gt; **All**.

9.  Filter the **Target script** reference field on the sys\_id you copied.

    Searching by name doesn't return results because **Target script** is a reference field.

10. Open the matching policy record, set **Result** to **Track**, and select **Save**.

    If the policy shows **Reject** or a pending request, the decryption attempt fails until you approve it.


## Result

KMF can decrypt the imported credentials on this instance. Return to [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/validate-instance-connection.md) to confirm the connection.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

