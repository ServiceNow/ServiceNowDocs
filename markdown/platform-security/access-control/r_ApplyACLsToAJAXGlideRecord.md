---
title: Apply ACLs to AJAXGlideRecord \(client-side Glide record\)
description: Use a system property to perform access control list \(ACL\) rule validation when server-side records \(for example, tables\) are accessed using GlideAjax APIs within a client script.
locale: en-US
release: xanadu
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Advanced ACL configuration, Access Control List Rules, Access Management]
---

# Apply ACLs to AJAXGlideRecord \(client-side Glide record\)

Use a system property to perform access control list \(ACL\) rule validation when server-side records \(for example, tables\) are accessed using GlideAjax APIs within a client script.

If you choose to apply access control lists \(ACL\) to GlideAjax API calls, then you can only query data to which the currently connected user has rights to access. For example, if the user is logged in as an ESS user who has no rights to read the `cmn_location` table, then any GlideAjax API call by the user will fail.

If the ServiceNow AI Platform is running without GlideAjax ACL call checking, an API can return information that the currently logged in user could not otherwise access.

Use GlideRecordSecure when querying data to ensure the highest level of security. GlideRecord relies on ACL enforcement through configurations whereas GlideRecordSecure applies stricter security controls. GlideRecordSecure offers a more secure, out-of-the-box solution for handling sensitive data.

**Note:** Set this property in **System Properties** &gt; **Security**.

|Property|Default|
|--------|-------|
|Apply standard security ACLs to AJAXGlideRecord calls|ACL checking enforced|

**Warning:** The `sys_class_name, sys_id` and `sys_domain` are ignored for ACL checks.

To learn more about this property, see [Require AJAXGlideRecord ACL checking \[Updated in Security Center 1.3\]](../../security-center/reference/sc-enabling-ajaxgliderecord-acl-checking.md) in Instance Security Hardening Settings.

