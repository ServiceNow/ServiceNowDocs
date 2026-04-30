---
title: Employee to-dos approval roles
description: Roles determine who can approve, reject, or comment on employee requests.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Employee tasks page, Setup task management, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Employee to-dos approval roles

Roles determine who can approve, reject, or comment on employee requests.

Use the following roles to define how employee requests on the Employee to-dos page are handled:

<table id="table_vfx_wgq_fsb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

approver\_user​

</td><td>

Required role for Approver users. Approver users can modify requests for approval routed to them. They also have all capabilities of Requesters. Note there is a fee associated with this role. Do not assign it to users without confirming your organization has the appropriate entitlement.

</td><td>

None

</td></tr><tr><td>

sn\_request\_read

</td><td>

Provides read access to the Request Management Application and related functions \(It does not check for approving records\).Can read REQs and RITMS.

</td><td>

None

</td></tr><tr><td>

sn\_request\_approver\_read

</td><td>

Provides read access to the Request Management Application and related functions \(allows access only if user has an approving record for the request record\).User with this role can read approvals.

</td><td>

None

</td></tr><tr><td>

sn\_request\_write

</td><td>

Provides write access to the Request Management Application and related functions.User with this role can comment on requests.

</td><td>

-   task\_editor
-   sn\_request\_read
-   dependency\_views
-   agent\_workspace\_user
-   view\_changer
-   cmdb\_read
-   sn\_request\_approver\_read

</td></tr><tr><td>

sn\_hr\_core.case\_reader​

</td><td>

Provides access and ability to read all HR cases.

</td><td>

None

</td></tr></tbody>
</table>