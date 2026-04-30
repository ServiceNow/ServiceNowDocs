---
title: Enable script sandbox \[Updated in Security Center 1.3\]
description: Use the glide.script.use.sandbox property to enable script sandboxing.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable script sandbox \[Updated in Security Center 1.3\]

Use the **glide.script.use.sandbox** property to enable script sandboxing.

Prevent unauthorized or unauthenticated users from executing privileged script on your instance by enabling the script sandbox feature. The script sandbox is used to execute client-generated scripts, such as query conditions and GlideAjax expressions, in a "sandbox" environment that has restricted rights.

Without the script sandbox, unauthorized/unauthenticated users can execute privileged script on an instance. This can impact security across all areas, including, but not limited to potentially malicious access to all data on the instance.

Enable the script sandbox feature on your instance by setting the **glide.script.use.sandbox** system property to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

There are two cases in the ServiceNow AI Platform that enable the client to send scripts to the server for evaluation:

-   **Filters or queries**

    It is legal to send a filter to the server such as `assigned_to=JavaScript:getMyGroups()`.

-   **System API**

    API call enables the client to run arbitrary scripts on the server and receive a response.


If you enable the script sandbox, the script being evaluated at either of these two entry points runs in a sandbox with reduced rights, with the following characteristics:

-   Only those business rules marked **Client callable** are available within the sandbox.
-   Only script includes marked **Sandbox enabled** are available within the sandbox.
-   Certain API calls \(largely, but not entirely, limited to ones dealing with direct DB access are not allowed.\)
-   You can't insert, update, or delete data from within the sandbox. For example, any calls to `current.update()`, are ignored. If you run the ServiceNow AI Platform without enabling script sandboxing, none of these restrictions apply.

**Note:** Beginning with the Xanadu release, script includes marked as **Glide AJAX enabled** \(previously named **Client callable**\) aren’t accessible within the sandbox. Only those marked **Sandbox enabled** are available within the sandbox. When upgrading to the Yokohama release from the Washington DC release or earlier, any script includes marked as **Client callable** are also marked as **Sandbox enabled**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.script.use.sandbox**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

Enforces validation for the client-side JavaScript queries that are launched against the platform

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

10

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces validation for the client-side JavaScript queries that are launched against the ServiceNow AI Platform. There is a potential impact if customer has customizations that include hard-coded JavaScript queries to perform CRUD operations.

</td></tr><tr><td>

Security risk

</td><td>

\(Critical\) The ServiceNow AI Platform provides wide variety of features and functionality through JavaScript queries. However, without appropriate authorization and validation, there is a potential for an attacker to perform unauthorized operations against the platform.

</td></tr><tr><td>

References

</td><td>

[Configuring Script sandbox property](../../security/reference/r_ScriptSandboxing.md) **glide.script.use.sandbox** belongs to the same family of properties that secure and restrict execution of scripts originating from the client:

-   **glide.script.allow.ajaxevaluate**: See [Disable AJAXEvaluate](sc-disable-ajaxevaluate.md).
-   **glide.script.secure.ajaxgliderecord**: See [Require AJAXGlideRecord ACL checking \[Updated in Security Center 1.3\]](sc-enabling-ajaxgliderecord-acl-checking.md).

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

