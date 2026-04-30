---
title: Use script includes to suppress filters and breadcrumbs
description: You can use a script to restrict filters and breadcrumbs to specific roles, either on a per-table or global basis. Using a script is an advanced option that offers additional flexibility compared to using list control.
locale: en-US
release: zurich
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Restrict filters and breadcrumbs with fixed queries, Administer, List administration, Forms, fields, and lists, Configure core features, Administer]
---

# Use script includes to suppress filters and breadcrumbs

You can use a script to restrict filters and breadcrumbs to specific roles, either on a per-table or global basis. Using a script is an advanced option that offers additional flexibility compared to using list control.

## Before you begin

Using a script include requires knowledge of JavaScript.

Role required: script\_include\_admin

## About this task

The examples shown must be modified for your environment.

## Procedure

1.  Create a script include with the name &lt;tablename&gt;DisplayFilter.

    The script section contains one function with the same name as the script include.

2.  Use your function to set the global variable *answer* to either true \(show the filters and breadcrumbs\) or false \(hide them.\)

    The following example restricts filters and breadcrumbs on the Incident table to users with any role. Be sure that the name of the script matches the function name exactly, including case.

    ```
    function incidentDisplayFilter() {
        if (gs.getUser().hasRoles()) {
            answer = "true";
        } else {
            answer = "false";
        }
    
        return answer;
    }
    ```

3.  To exclude a specific role from having access to filters and breadcrumbs, make the following change.

    ```
    function incidentDisplayFilter() {
        if (gs.getUser().hasRoles() && !gs.getUser().hasRoles('newrole')) {
            answer = "true";
        } else {
            answer = "false";
        }
    
        return answer;
    }
    ```

    Users with the role `newRole` do not have access to filters and breadcrumbs.

4.  To let all users use filters and breadcrumbs on the Incident table, make the following change to your script.

    ```
    function incidentDisplayFilter() {
        var answer = true;
    
        return answer;
    }
    ```

5.  To modify filter and breadcrumb access for another table, create a script include using the name of that table instead of Incident.


