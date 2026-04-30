---
title: CAM user roles
description: Assign users and groups with roles to prepare them to user the CAM application.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CAM reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# CAM user roles

Assign users and groups with roles to prepare them to user the CAM application.

## Role permissions and responsibilities

<table id="table_o14_t2s_2mb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authorization Official\(sn\_irm\_cont\_auth.authorization\_official\)

</td><td>

Responsible for accepting an information system into an operational environment at a known risk level.The Authorization Official is entitled to approve and update authorization packages.

The role and contains:

-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

Continuous Authorization and Monitoring administrator\(sn\_irm\_cont\_auth.admin\)

</td><td>

Responsible for all system administration duties in the CAM application.The role contains:

-   sn\_audit.manager
-   sn\_compliance.admin
-   sn\_doc.admin
-   sn\_irm\_cont\_auth.reader
-   sn\_irm\_cont\_auth.scheduler

</td></tr><tr><td>

Executive Reader\(sn\_irm\_cont\_auth.executive\_read\)

</td><td>

Read-only access to all modules of the CAM application. The role contains: sn\_irm\_cont\_auth.reader. Users with this role can access CAM Workspace.

</td></tr><tr><td>

Information Owner\(sn\_irm\_cont\_auth.information\_owner\)

</td><td>

Responsible for statutory, management, or operational authority and the establishment of policies and procedures governing its generation, collection, processing, dissemination, and disposal. The user can also update information types of an authorization package. The role contains:

-   sn\_audit.user
-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

Information System Security Manager\(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)

</td><td>

Responsible for conducting information system security management activities. They develop and maintain the system-level cybersecurity program.Can update the authorization package. The role contains:

-   sn\_compliance.user
-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

Information System Security Officer\(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)

</td><td>

Responsible for ensuring that the appropriate operational security posture is maintained for an information system.Can update the authorization package. The role contains:

-   sn\_compliance.user
-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

Reader\(sn\_irm\_cont\_auth.reader\)

</td><td>

Read-only role. Users with this role can access CAM Workspace.The role contains:

-   sn\_audit.reader
-   sn\_grc\_workspace.task\_reader
-   sn\_grc\_workspace.user
-   sn\_compliance.reader
-   sn\_incident\_read
-   sn\_change\_read
-   sn\_vul.read\_all
-   sn\_si.read

</td></tr><tr><td>

Scheduler\(sn\_irm\_cont\_auth.scheduler\)

</td><td>

Responsible for running all scheduled jobs for the application. This role is for a technical user.The role contains: sn\_irm\_cont\_auth..system\_owner.

</td></tr><tr><td>

Security Control Assessor\(sn\_irm\_cont\_auth.sec\_control\_assessor\)

</td><td>

Responsible for conducting a thorough assessment of the management, operational, and technical security controls of an information system.The role contains:

-   sn\_audit.manager
-   sn\_compliance.user
-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

System Owner\(sn\_irm\_cont\_auth.system\_owner\)

</td><td>

Responsible for procuring, developing, integrating, modifying, operating, and maintaining an information system.The role contains:

-   sn\_audit.user
-   sn\_compliance.user
-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

System User\(sn\_irm\_cont\_auth.system\_user\)

</td><td>

Responsible for performing actual work in the system. They can update authorization boundaries, filter, elements, milestones, and acceptance tasks.The role contains:

-   sn\_audit.user
-   sn\_irm\_cont\_auth.reader
-   business user

</td></tr></tbody>
</table>**Parent Topic:**[CAM reference](../concept/reference-grc-cam.md)

