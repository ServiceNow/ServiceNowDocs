---
title: Constrain the assigned to field by role
description: This example shows how to use JavaScript and a business rule to restrict the incident Assigned to field choices to only the users with the itil\_admin role.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure reference qualifiers, Reference qualifiers, Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Constrain the assigned to field by role

This example shows how to use JavaScript and a business rule to restrict the incident **Assigned to** field choices to only the users with the itil\_admin role.

## Before you begin

Role required: personalize\_dictionary or admin

## About this task

You can also change itil\_admin to any other role on a reference field that refers to the User \[sys\_user\] table.

## Procedure

1.  Open an incident.

2.  In the upper-left corner of the screen, click the form context menu, and then select **Configure** &gt; **Dictionary**.

3.  In the **Reference qual** field, enter `javascript:"sys_idIN"+getRoledUsers("itil_admin").join(",")`.

4.  Save the record.

5.  To see the base system business rule that this JavaScript code calls, navigate to **System Definition** &gt; **Business Rules**.

6.  Open **getRoledUsers**.

    The business rule uses the following JavaScript code.

    ```
    // Return an array of sys_ids of the users that have at least one role
    // optional parameters allow the exclusion (NOT IN) of some roles or
    // look for specific roles (IN)
    //
    // optional: queryCondition - 'IN' or 'NOT IN'
    // optional: roleList - a comma separated list of role names
    //
    function getRoledUsers(queryCondition, roleList) {
       var roleListIds;
       if (queryCondition && roleList) {
          roleListIds = getRoleListIds(roleList);
       }
    
       var users = {};
       var now_GR = new GlideRecord('sys_user_has_role');
       if (roleListIds) {
          now_GR.addQuery('role', queryCondition, roleListIds);
       }
       now_GR.query();
       while (now_GR.next()) {
          users[now_GR.user.toString()] = true;
       }
       
       var ids = [];
       for (var id in users)
          ids.push(id);
          
       return ids;
    }
    
    // get sys_id's for the named roles
    function getRoleListIds(roleList) {
       var ids = [];
       var now_GR = new GlideRecord('sys_user_role');
       now_GR.addQuery('name','IN',roleList);
       now_GR.query();
       while (now_GR.next()) {
          ids.push(now_GR.sys_id.toString());
       }
       return ids;
    }
    ```


