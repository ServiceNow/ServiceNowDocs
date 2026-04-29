---
title: Runtime access tracking
description: Runtime access tracking allows administrators to manage script access to application resources by creating a list of script operations and targets that the system authorizes to run.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Runtime access tracking

Runtime access tracking allows administrators to manage script access to application resources by creating a list of script operations and targets that the system authorizes to run.

Runtime access tracking provides the following options:

<table id="table_mxm_sm1_jv"><thead><tr><th>

Option

</th><th>

Tracking done

</th><th>

Authorization done

</th><th>

Results

</th></tr></thead><tbody><tr><td>

None

</td><td>

The system does not track runtime access requests.

</td><td>

The system does not require authorization to run access requests.

</td><td>

Application scripts can access resources from other applications as long as the table-level access settings allow it.

</td></tr><tr><td>

Tracking

</td><td>

During development, the system creates a Cross-Scope Privilege record for each runtime access request.

 After installation, the system no longer tracks new runtime access requests.

</td><td>

The system sets the status of the Cross-Scope Privilege record to **Allowed**.

</td><td>

The system runs the tracked operation as long as the table-level access settings allow it.

</td></tr><tr><td>

Enforcing

</td><td>

During development, the system creates a Cross-Scope Privilege record for each runtime access request.

 After installation, the system no longer tracks new runtime access requests.

</td><td>

The system sets the status of the Cross-Scope Privilege record to **Requested**.

</td><td>

The system blocks the tracked operation from running until an Administrator manually changes the status to **Allowed** and the table-level access settings allow it.

</td></tr></tbody>
</table>During development, application designers must run all of an application's script logic to ensure the system tracks and authorizes the access requests to other applications.

**Parent Topic:**[Application design and runtime settings](../reference/r_ApplicationDesignAndRuntimeSettings.md)

