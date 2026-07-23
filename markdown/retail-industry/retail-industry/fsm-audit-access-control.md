---
title: How access to audit tasks works
description: Field Service for Audit uses a layered access-control framework: platform ACLs enforce role-based deny-first rules, and a scripted extension point delegates fine-grained read/write decisions to consuming apps, with a permissive default when no consumer rule applies.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 2
---

# How access to audit tasks works

Field Service for Audit uses a layered access-control framework: platform ACLs enforce role-based deny-first rules, and a scripted extension point delegates fine-grained read/write decisions to consuming apps, with a permissive default when no consumer rule applies.

## How access decisions are made

Every read and write operation on `wm_audit_task` passes through two layers:

1.  **Platform ACL evaluation** — The platform evaluates the record-level and field-level ACLs defined by this app. These ACLs follow a deny-first pattern: explicit deny ACLs block all authenticated users first, then role-based allow ACLs open targeted access for each persona.
2.  **Extension-point evaluation** — ACL scripts on `wm_audit_task` call `AuditACL.canRead()` or `AuditACL.canWrite()`. Those methods iterate the registered consumer extension instances in order. The first instance whose `handles()` method returns `true` decides the outcome. If no registered instance handles the record, the evaluator returns `true` \(default-allow\).

## Evaluation flow

```
Caller (form save / GlideRecord query / consuming app)
        ↓
Platform ACL evaluation on wm_audit_task
        ↓                              ↓
Role check (auditor / admin)     ACL script → AuditACL.canRead / canWrite
                                               ↓
                                 Iterate sys_extension_instance records
                                 (registered by consuming apps, ordered)
                                               ↓
                                 instance.handles(current, operation, field)?
                                   → first match wins
                                               ↓
                                 matched: instance.canRead / canWrite → answer
                                 no match: default-allow (return true)
        ↓
Read / Write decision returned to platform → access granted or denied
```

## Deny-first ACL pattern

All record-level ACLs on `wm_audit_task` use a deny-first pattern. Explicit deny ACLs \(`securityAttribute: 'user_is_authenticated'`, `localOrExisting: 'Existing'`\) block all authenticated users on Create, Read, Write, and Delete. Role-based allow ACLs then create targeted exceptions for authorized personas. This pattern ensures that no access is silently inherited from the parent `wm_task` ACLs.

## ACL scope override

Every record-level and field-level ACL defined on `wm_task` is explicitly overridden on `wm_audit_task`. This prevents audit access from being silently governed by the parent table's rules.

## Default-allow fallback

In FSM-only deployments where no consuming app has registered an extension instance, every `AuditACL.canRead()` and `AuditACL.canWrite()` call returns `true`. Auditors and Audit Admins can see and edit all audit tasks.

**Related topics**  


[Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-overview.md)

[Custom access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

