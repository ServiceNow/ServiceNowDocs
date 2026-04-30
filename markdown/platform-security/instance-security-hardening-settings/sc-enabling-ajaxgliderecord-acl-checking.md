---
title: Require AJAXGlideRecord ACL checking \[Updated in Security Center 1.3\]
description: Use the glide.script.secure.ajaxgliderecord property to perform access control rule \(ACL\) validation when server-side records, such as tables, are accessed using GlideAjax APIs within a client script.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Require AJAXGlideRecord ACL checking \[Updated in Security Center 1.3\]

Use the **glide.script.secure.ajaxgliderecord** property to perform access control rule \(ACL\) validation when server-side records, such as tables, are accessed using GlideAjax APIs within a client script.

From client scripts, it is possible to query arbitrary data from the server using the AJAXGlideRecord \([GlideAjax - Client](https://www.servicenow.com/docs/access?context=c_GlideAjaxAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)\) API, by using a syntax such as a server-side glide record. It is a powerful and useful tool in many deployments.

If you choose to apply Access Control Lists \(ACL\) to GlideAjax API calls, you can only query data to which the currently connected user has access. For example, if an ESS user who has no rights to read the cmn\_location table is logged in, any GlideAjax API call to that table would fail.

If the ServiceNow AI Platform is running without GlideAjax ACL call checking, an API can return information that the currently logged in user could not otherwise access.

Use GlideRecordSecure when querying data to ensure the highest level of security. GlideRecord relies on ACL enforcement through configurations whereas GlideRecordSecure applies stricter security controls. GlideRecordSecure offers a more secure, out-of-the-box solution for handling sensitive data.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.script.secure.ajaxgliderecord**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

Ensure security ACLs are checked and validated even when the records are accessed through Client Side APIs.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

8.1

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces the ACL relationship with server-side records when the requests are made using the AJAXGlideRecord API calls. If the ACL configuration is not properly configured, then there is potential impact. For more details on its impact, and how to identify it, see Refer to the [Audit and review client-side GlideRecord \(AJAXGlideRecord\) transactions \[KB0550828\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0550828) article in the HI Knowledge Base.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Through client scripts, it is possible to query arbitrary data from the server through the GlideAjax API. Server-side resources can be accessed without proper authorization, so using ACL validation helps the application validate the request based on the configured authorization.

</td></tr><tr><td>

Workaround

</td><td>

Ensure that proper ACLs are created for script includes, processors, and other entities used by a GlideAjax \(AJAXGlideRecord\) API so that it executes under proper authorization.

 Implement methods like `canRead ()`, `canWrite()`, `canCreate ()`, and `canDelete ()` to perform user authorization before accessing table records using GlideRecord.

 Another method is to use GlideRecordSecure. The class is inherited from the GlideRecord Server that performs the same functions as GlideRecord, and also enforces ACLs.

</td></tr><tr><td>

References

</td><td>

[Apply ACLs to AJAXGlideRecord \(client-side Glide record\)](../../security/reference/r_ApplyACLsToAJAXGlideRecord.md) This property belongs to the same family of properties that secure and restrict execution of scripts originating from the client, such as **glide.script.allow.ajaxevaluate**. For more information, see [Enable AJAXEvaluate](sc-disable-ajaxevaluate.md).

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

