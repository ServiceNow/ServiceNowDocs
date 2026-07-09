---
title: Custom access rules
description: The access-control extension point is the mechanism consuming apps use to register their own read and write access rules for audit tasks without modifying Field Service for Audit. Each consuming app implements the contract in its own scope on its own release cadence, and multiple consumers coexist through a deterministic first-match-wins evaluation order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-custom-access-rules.html
release: australia
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 3
breadcrumb: [Retail Store Audit Operations, Explore, Retail]
---

# Custom access rules

The access-control extension point is the mechanism consuming apps use to register their own read and write access rules for audit tasks without modifying Field Service for Audit. Each consuming app implements the contract in its own scope on its own release cadence, and multiple consumers coexist through a deterministic first-match-wins evaluation order.

## What the extension point does

The `sn_fsm_audit` app defines a `sys_extension_point` record that describes the contract consuming apps must implement. Each consuming app that needs custom access logic:

1.  Creates a `sys_extension_instance` record in its own scope that references this extension point.
2.  Implements the three contract methods: `handles()`, `canRead()`, and `canWrite()`.

At runtime, `AuditACL.canRead()` and `AuditACL.canWrite()` load all registered instances, iterate them in order, and call `handles()` on each. The first instance that returns `true` from `handles()` is asked for the `canRead()` or `canWrite()` answer.

## Extension-point contract

A consuming app's extension instance must implement the following methods:

|Method|Signature|Returns|Description|
|------|---------|-------|-----------|
|`handles`|`handles(current, operation, field)`|boolean|Return `true` if this implementation governs access for the given record, operation \(`'read'` or `'write'`\), and optional field name. Return `false` to pass to the next registered instance.|
|`canRead`|`canRead(current, field)`|boolean|Called only when `handles()` returned `true`. Return `true` to grant read access, `false` to deny.|
|`canWrite`|`canWrite(current, field)`|boolean|Called only when `handles()` returned `true`. Return `true` to grant write access, `false` to deny.|

## Scope isolation

Extension instances live entirely in the consuming app's scope. Field Service for Audit calls them via the platform's cross-scope privilege mechanism. This means:

-   The consuming app ships, updates, and rolls back its access logic independently.
-   Field Service for Audit never needs a new release when a consumer changes access rules.
-   Multiple consumers can coexist because each instance's `handles()` scopes it to the records it owns.

## Field-level extension rules

Consuming apps can also register extension instances that govern access at the field level for their own custom fields on `wm_audit_task`. The `field` parameter in `handles()`, `canRead()`, and `canWrite()` identifies the specific field. When `field` is absent, the rule applies at the record level.

## Multi-consumer rule evaluation

When multiple consuming apps have registered access-control extension instances, Field Service for Audit evaluates them in a deterministic order and stops at the first instance whose `handles()` method claims the record.

**Evaluation order**

Extension instances are evaluated in a stable, ordered sequence determined by the `order` field on each `sys_extension_instance` record. Instances with a lower order value are evaluated first.

**First-match-wins rule**

The evaluator stops as soon as one instance's `handles()` returns `true`. The outcome \(`canRead` or `canWrite`\) is taken entirely from that instance. No subsequent instances are consulted for that record or field.

**No-match fallback**

If every registered instance returns `false` from `handles()`, or if no instances are registered, `AuditACL` returns `true` \(default-allow\).

**Multi-consumer coexistence guidelines**

-   Set a unique, non-overlapping `order` value for each consumer's extension instance.
-   Write `handles()` to scope narrowly — check a field or relationship that uniquely identifies records the consumer owns.
-   Do not rely on evaluation order alone to resolve ambiguity; overlapping `handles()` logic produces non-deterministic behavior if order values change.

**Parent Topic:**[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

**Related topics**  


[Access control framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-access-control.md)

[Register an access-control extension instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-t-set-up-access-rules.md)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

