---
title: Additional security with Extended Security for EWD
description: Additional security is an ACL enforcement feature available with Extended Security for Enterprise-Wide Deployment that applies partition-based access control to four partitioned tables: Project, Demand, Program, and Portfolio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/additional-security-with-extended-security-ewd.html
release: australia
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Explore, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Additional security with Extended Security for EWD

Additional security is an ACL enforcement feature available with Extended Security for Enterprise-Wide Deployment that applies partition-based access control to four partitioned tables: Project, Demand, Program, and Portfolio.

## What is additional security?

Additional security is an optional feature that strengthens access control in Enterprise Wide Deployment by enforcing partition-based ACL \(Access Control List\) rules at the table level. When enabled for a table, users can only read, create, update, or delete records within their assigned partition, regardless of their role or existing table permissions.

This provides a second layer of protection beyond traditional role-based access control \(RBAC\), ensuring that partition boundaries are enforced at the database level.

## Supported tables

Additional security is available for four tables in Strategic Portfolio Management with Extended Security for EWD.

-   Project \(pm\_project\) — Work initiatives and deliverables
-   Demand \(dmn\_demand\) — Work requests and capacity planning
-   Program \(pm\_program\) — Collections of related projects
-   Portfolio \(pm\_portfolio\) — Strategic collections of programs and projects

You can enable additional security for any combination of these tables. Each table can be configured independently.

## How it works

When additional security is enabled for a table, every database operation is subject to partition-based ACL validation:

-   **Read:** Users see only records assigned to their partition
-   **Create:** New records are automatically assigned to the user's partition
-   **Update:** Users can modify only records in their partition
-   **Delete:** Users can delete only records in their partition

ACL enforcement occurs at the database level and is independent of role assignments, ensuring consistent access control regardless of how permissions are configured.

## When to use additional security

Enable additional security when:

-   Your organization requires strict data isolation between partitions \(business units, geographic regions, or separate entities\)
-   Compliance regulations mandate partition-level access controls \(SOX, GDPR, HIPAA, etc.\)
-   You operate a multi-tenant deployment where customer data must remain segregated
-   You want to prevent accidental cross-partition data visibility through role-based permissions

## Access model

Additional security does not replace partition assignments. Users must still be explicitly assigned to partitions through:

-   Role assignments linked to partitions
-   Team membership with partition scoping
-   Direct partition assignment in the user record

When additional security is enabled, users can only access tables and records within the partitions they are assigned to. Enterprise administrators with access to multiple partitions can see records from all their assigned partitions.

## Configuration

Additional security is configured on a per-table basis in the SPM Configure console under **Partitions** &gt; **Enable additional security**. Each table has a checkbox; when checked, partition-based ACL enforcement is enabled for that table.

Changes take effect immediately after save. Existing records retain their partition assignment; access restrictions apply to all future queries. For instructions to enable additional security, see [Enable additional security for partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enable-additional-security-extended-security-ewd.md).

