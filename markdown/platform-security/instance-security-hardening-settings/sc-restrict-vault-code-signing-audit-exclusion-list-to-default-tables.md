---
title: Restrict vault code signing audit exclusion to defaults
description: Manage which tables are excluded from Vault Code Signing audit tracking to maintain visibility into changes on protected code artifacts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-restrict-vault-code-signing-audit-exclusion-list-to-default-tables.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Vault Code Signing, audit tracking, code signing, security]
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Restrict vault code signing audit exclusion to defaults

Manage which tables are excluded from Vault Code Signing audit tracking to maintain visibility into changes on protected code artifacts.

The **com.glide.codesigning.tables.excluded\_from\_audit** property lists tables excluded from Vault Code Signing audit tracking. Create, update, and delete operations on these tables don't generate an audit entry, even when a table would otherwise be eligible for Code Signing auditing.

The platform ships this property scoped only to Code Signing's own internal operational tables: certificate storage, crypto module/policy configuration, signing job tracking, and related bookkeeping tables. This prevents the audit noise from internal state changes. Any table name added beyond this default list is also excluded from audit tracking. This property doesn't distinct between an internal housekeeping table and a table containing actual protected, signed code artifacts.

To configure this property:

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Confirm the **com.glide.codesigning.tables.excluded\_from\_audit** property either does not exist in the sys\_properties table or is set to the following comma-separated list of table names:

    ```
    sys_restricted_caller_access,sys_scope_master, sys_kmf_crypto_caller_policy, sys_kmf_crypto_module, sn_cse_codesigning_transaction, sn_cse_configuration_property, sn_cse_quorum_request,sys_certificate,sysauto_script,
                sys_signing_job,sys_mass_encryption_job
    ```


## More information

<table id="table_property_details-restrict-vault-code-signing"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.codesigning.tables.excluded\_from\_audit**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String \(comma-separated table names\)

</td></tr><tr><td>

Recommended value

</td><td>

sys\_restricted\_caller\_access,sys\_scope\_master, sys\_kmf\_crypto\_caller\_policy,sys\_kmf\_crypto\_module,sn\_cse\_codesigning\_transaction, sn\_cse\_configuration\_property, sn\_cse\_quorum\_request,sys\_certificate, sysauto\_script,sys\_signing\_job,sys\_mass\_encryption\_job

</td></tr><tr><td>

Default value

</td><td>

sys\_restricted\_caller\_access,sys\_scope\_master, sys\_kmf\_crypto\_caller\_policy, sys\_kmf\_crypto\_module,sn\_cse\_codesigning\_transaction, sn\_cse\_configuration\_property, sn\_cse\_quorum\_request, sys\_certificate,sysauto\_script, sys\_signing\_job,sys\_mass\_encryption\_job

</td></tr><tr><td>

Fallback value

</td><td>

sys\_restricted\_caller\_access,sys\_scope\_master, sys\_kmf\_crypto\_caller\_policy,sys\_kmf\_crypto\_module, sn\_cse\_codesigning\_transaction,sn\_cse\_configuration\_property, sn\_cse\_quorum\_request, sys\_certificate,sysauto\_script, sys\_signing\_job,sys\_mass\_encryption\_job

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Security risk rating: Medium
-   CVSS score: 5.1
-   Security risk details:

Expanding this list beyond the platform-defined default removes audit visibility for added tables. This can include the very tables that store the protected, signed code artifacts this feature exists to monitor.

An administrator or a compromised integration with write access to this property could narrow audit coverage for a specific table without disabling Code Signing auditing overall. This allows the instance to continue to appear fully audited while visibility into changes on that specific table has been silently removed.


</td></tr><tr><td>

Functional impact

</td><td>

Adding a table name to this property stops audit generation for that table's create, update, and delete operations. Removing a table name \(or restoring the default list\) resumes audit tracking for that table. Changing this property affects only audit trail generation. It has no effect on Code Signing signature validation, enforcement, or the signing mechanism itself. Tables can be excluded from auditing without impacting the signing feature's functionality.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

No effect unless both **com.snc.kmf.signature.validation.optin** and **sn\_cse.com.snc.csf.vault\_audit\_enabled** are true.

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-error-handling-logging.md)

