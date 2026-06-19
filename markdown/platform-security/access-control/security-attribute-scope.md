---
title: Security Attribute Scope
description: Security Attributes supports scoping capabilities.Existing and local security attributes let you control the scope of your security attribute condition sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/access-control/security-attribute-scope.html
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Attributes, Access Management]
---

# Security Attribute Scope

Security Attributes supports scoping capabilities.

## Security Attribute Scoping

Security Attributes scoped behavior is consistent with Platform's scoping behaviors. Security Attributes created within a scope are only available in access controls in the same scope.

## Local and Existing security attributes

Existing and local security attributes let you control the scope of your security attribute condition sets.

### About local and existing scopes

Security attributes, which are building blocks that evaluate context for user and session, can be used in both security data filters and access control lists \(ACLs\). When you add an attribute to a security data filter or ACL, you select a scope: local or existing.

-   **Local**

    An attribute that is defined inside the security data filter or ACL. No record exists outside of it, and nothing else can reference it. It's unique to the security data filter or ACL from which it was created. Local is the default for security attribute conditions.

-   **Existing**

    An attribute that is a reference to a security attribute record. The security data filter or ACL points to the record. Other security data filters and ACLs can reference it as well.


### Scope advantages and disadvantages

Local scope keeps things contained: no shared surface area, no governance overhead, and it's fast to create. The downside is duplication. If you re-create the same local security attribute across 10 security data filters or ACLs, you now have 10 copies to keep in sync and 10 places to update when business logic changes.

Existing scope flips that tradeoff. Existing scope advantages include having one security attribute definition, one place to update, and consistent semantics platform-wide. The cost is governance—the security attribute becomes a named, shared object that other people rely on, so changes require caution. The more security data filters or ACLs that share an existing attribute, the greater the impact of any change to it.

### Which scope to use

Use Local scope when the security attribute is genuinely a one-off: specific to a security data filter, an ACL, a table, or a scenario. The logic may be a simple condition, straightforward to create, and isn't reused. Local scope may also be ideal when you're prototyping and don't know if the security attribute will generalize.

Use Existing scope when the security attribute represents a reusable semantic concept that will appear in many security data filters or ACLs. For example, UserIsAIAgent, UserHasClearance, or UserInRegion. One source of truth ensures all filters or ACLs agree on what "AI agent" means. The attribute is discoverable, auditable, and reviewable as its own artifact \(Access Analyzer surfaces named attributes more usefully than inline attributes\). The logic is non-trivial to create and you don't want it implemented inconsistently.

As a general guideline, if you'd give the attribute a name in a design doc, it should be Existing scope. If it's just a column comparison for one filter, keep it Local scope \(default\).

