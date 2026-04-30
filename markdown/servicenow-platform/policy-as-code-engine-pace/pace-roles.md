---
title: Key user personas and roles
description: This section describes different user personas and roles in PaCE. These personas are defined with the application where PaCE is being used.
locale: en-US
release: yokohama
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Understanding PaCE, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Key user personas and roles

This section describes different user personas and roles in PaCE. These personas are defined with the application where PaCE is being used.

All roles except the super administrator role must be assigned to a calling service or application where PaCE is being used. The assigned calling service defines the scope for the user role.

|Role|High-level Permissions|Persona|
|----|----------------------|-------|
|sn\_pace.execution\_reader|A read-only user with view-only access. This user can view policies, categories, and executions.|Policy user, internal auditor.|
|sn\_pace.code\_reader|Can review PaCE versions, policy code, and run tests.|Internal auditor|
|sn\_pace.code\_editor|This user has all the sn\_pace\_code\_reader permissions plus the ability to create PaCE policy versions.|Policy developer|
|sn\_pace.policy\_reader|This user has all the sn\_pace\_code\_reader permissions plus the ability to review policy details and mapping information.|Policy user, internal auditor|
|sn\_pace.policy\_editor|This user has all the sn\_pace\_policy\_reader and sn\_pace.code\_editor permissions plus the ability to create policies and mappings.|Policy developer|
|sn\_pace.mapping\_admin|This user can map policies and edit config parameters for policy mappings.|Mapping admin|
|sn\_pace.admin|This user has the permissions of all the other roles plus the ability to create categories, policies, mappings, and code.|Policy admin|
|sn\_pace.super\_admin|This user has all the sn\_pace.admin role permissions across all calling services.|Not applicable|
|Maint role|Internal user who can create default content.|Not applicable|

