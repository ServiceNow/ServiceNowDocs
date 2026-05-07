---
title: Create ACLs for AI Data Explorer and Query Generation protected scope access
description: Create Access Control Lists \(ACLs\) in protected scopes to enable AI Data Explorer and Query Generation to access tables within those scopes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 2
keywords: [AI Data Explorer, Query Generation, ACL, protected scope]
breadcrumb: [Enabling access to protected scope apps, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Create ACLs for AI Data Explorer and Query Generation protected scope access

Create Access Control Lists \(ACLs\) in protected scopes to enable AI Data Explorer and Query Generation to access tables within those scopes.

## Before you begin

You must have administrator access to the protected scope where you want to enable AI Data Explorer and Query Generation functionality.

Role required: admin or scope-specific administrator role

## About this task

Protected scopes require their own ACLs that mirror the functionality provided by AI Data Explorer and Query Generation standard ACLs. These ACLs must call a public script include provided by the AI Data Explorer plugin to verify proper access control.

**Note:** For simplicity, the following steps use the Insert and Stay feature on existing paai\_canvas\_component ACLs. You can also use the information in this procedure to create the four necessary ACLs from scratch.

## Procedure

1.  Switch your current scope to the protected scope where you want to enable AI Data Explorer and Query Generation access.

    For example, switch to the Human Resources Core scope or Employee Profile scope.

2.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

3.  Filter the list of access controls on the **Name** field for paai\_canvas\_component.

4.  Create four ACL records for your application scope: one each for read, write, delete, and create operations.

    1.  Open the paai\_canvas\_component record for the write operation.

        Ignore the warning that you're in the wrong scope to edit it.

    2.  Expand the Additional Actions menu.

        ![Additional Actions menu for a paai_canvas_component Access Control record.](../image/access-control-additional-actions.png)

    3.  Select **Insert and Stay**.

        A new Access Control record opens. It has the same field values as the original record, but it is in your current application scope.

    4.  Add security checks, roles, or data conditions as required by your organization's security policies.

    5.  In the Advanced Condition section, change the script as follows:

        -   Change the name of the script that is called from `AICanvasACLUtil()` to `AICanvasACLUtilPublic()`.
        -   Change the parameter of the `canEditCanvas` method call to only pass the component `(current)`, not to call `toString()`.
        The script should be:

        ```javascript
        answer = new sn_pa_ai_canvas.AICanvasACLUtilPublic().canEditCanvas(current);
        ```

    6.  Repeat the process for the other operations, using these scripts:

        |Operation|Script|
        |---------|------|
        |read|`answer = new sn_pa_ai_canvas.AICanvasACLUtilPublic().canReadComponent(current);`|
        |create|`answer = new sn_pa_ai_canvas.AICanvasACLUtilPublic().canEditCanvas(current);` \(Same as write\)|
        |delete|`answer = new sn_pa_ai_canvas.AICanvasACLUtilPublic().isRecordOwner(current);`|

        These scripts check whether the user has read access, has edit access, or is the component owner, respectively.

5.  Confirm that each ACL is active and properly configured.


## Result

AI Data Explorer and Query Generation can now access tables within the protected scope, subject to the security restrictions defined in the ACLs. Users with appropriate permissions can create and read AI Data Explorer records for tables in the protected scope.

## What to do next

You must also create and approve Restricted Caller Access \(RCA\) records to enable Query Generation to fetch data from protected scope tables through API calls.

**Parent Topic:**[Enabling access to protected scope applications for AI Data Explorer and Query Generation](../concept/enable-aide-secure-scope-apps.md)

**Previous topic:**[Enabling access to protected scope applications for AI Data Explorer and Query Generation](../concept/enable-aide-secure-scope-apps.md)

**Next topic:**[Approve RCA records for AI Data Explorer and Query Generation protected scope access](create-rca-records-protected-scope-access.md)

