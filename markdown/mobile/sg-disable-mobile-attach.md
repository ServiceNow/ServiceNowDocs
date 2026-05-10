---
title: Disable attachments in mobile apps
description: Disable attachments for mobile apps by using access control rules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Disable attachments in mobile apps

Disable attachments for mobile apps by using access control rules.

## Before you begin

Role required: admin

**Note:**

-   You need to elevate to the **security\_admin** role to perform these steps. For details on this role, see [security\_admin role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-admin-role.md).
-   The script code that is added in the following procedure must be added to all ACLs on the table.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Access Control \(ACL\)**.

2.  Filter the list for `<Name> <contains> <sys_attachment>` and `<Operation> <is> <read>`.

3.  Find and open the record with the description: **Allow read for records in sys\_attachment, if the ACL script returns true.**

4.  Clear the **Admin overrides** check box.

5.  In the **Script** field, add the following code to the bottom of the script:

    ```
    
    if( gs.isMobile() ){
         answer = false;
    }
    ```

6.  Click **Update**.

    The added code prevents attachments from appearing when the instance is accessed from a mobile device. If you want to prevent your users from uploading attachments, continue on to the next steps.

7.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

8.  Filter the list for `<Name> <contains> <sys_attachemt>` and `<Operation> <is> <create>`.

9.  Find and open the record with the description: **Allow create for records in sys\_attachment, if the ACL script returns true.**

10. Clear the **Admin overrides** check box.

11. In the **Script** field, add the following code to the bottom of the script:

    ```
    
    if( gs.isMobile() ){
         answer = false;
    }
    ```

12. Click **Update**.

    The added code prevents attachments uploading when the instance is accessed from a mobile device.

    **Note:** The ability to rename or delete existing attachments on records in mobile is determined by the access control list \(ACL\) rules on your instance. For more information on these rules and how they effect user permissions on your instance, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).


