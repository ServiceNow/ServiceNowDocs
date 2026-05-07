---
title: Approve RCA records for AI Data Explorer and Query Generation protected scope access
description: Approve automatically generated Restricted Caller Access \(RCA\) records to enable AI Data Explorer and Query Generation to fetch data from tables in protected scopes through API calls.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 3
keywords: [AI Data Explorer, Query Generation, RCA, Restricted Caller Access, protected scope]
breadcrumb: [Enabling access to protected scope apps, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Approve RCA records for AI Data Explorer and Query Generation protected scope access

Approve automatically generated Restricted Caller Access \(RCA\) records to enable AI Data Explorer and Query Generation to fetch data from tables in protected scopes through API calls.

## Before you begin

You must have administrator access to the protected scope where you want to enable Query Generation and AI Data Explorer data access.

The necessary ACLs for the protected scope must be created and active.

Role required: admin or scope-specific administrator role

## About this task

When Query Generation and AI Data Explorer attempt to fetch data from protected scope tables through API calls, the system automatically creates Restricted Caller Access \(RCA\) records. These records must be approved by administrators to enable data access. RCA records are created on a per-table basis and must be approved for each table that Query Generation or AI Data Explorer needs to access.

## Procedure

1.  Ask AI Data Explorer a question about a table in the protected scope to trigger RCA record creation.

    You might have to add the table to the semantic data layer.

    The system creates RCA records for the scripted REST resource and generative AI validator operations needed to access the table data.

2.  Navigate to **System Security** &gt; **Restricted Caller Access**.

3.  Filter the records to show only those with the Query Generation or AI Data Explorer source scopes.

    Alternatively, filter on the target being the specific table that you want to access.

    When the source table is the script include that is included with AI Data Explorer, the source scope is also AI Data Explorer. Otherwise, Query Generation is the source scope.

4.  Review each RCA record.

    Each record shows the source scope, target scope, and the specific operation that requires access. Confirm that these operations align with your intended use of AI Data Explorer and Query Generation.

5.  Set the **Status** field to **Allowed** for each approved RCA record.

    Query Generation or AI Data Explorer can now access the specified table data through API calls for the approved operations.

6.  Create RCA records manually for additional tables.

    You can create RCA records manually if you know which tables will be accessed and want to avoid the initial error messages that users might encounter. However, you have to know whether Query Generation or AI Data Explorer is the source scope. If the source scope is AI Data Explorer, set the source type as Script include and choose a script include that is part of AI Data Explorer. Regardless of source, you must know the specific script references and operations that Query Generation or AI Data Explorer uses to access each table. Consider creating some RCA records through requests first, then using those as models to create others manually.


## Result

Query Generation can now fetch data from the approved tables in the protected scope. Users can successfully add tables to AI Data Explorer and ask questions about the data without encountering access errors.

If you encounter error messages such as "Error accessing table data" or "Scope access not granted," verify that the ACLs and RCA records are properly configured and approved. Each table requires its own set of approved RCA records.

If RCA records are not being created automatically, confirm that the ACLs are active and that users have the necessary permissions to trigger the Query Generation operations.

**Parent Topic:**[Enabling access to protected scope applications for AI Data Explorer and Query Generation](../concept/enable-aide-secure-scope-apps.md)

**Previous topic:**[Create ACLs for AI Data Explorer and Query Generation protected scope access](create-acls-protected-scope-access.md)

**Next topic:**[Tuning the semantic layer](../../ai-data-explorer/concept/semantic-layer-tuning-overview.md)

