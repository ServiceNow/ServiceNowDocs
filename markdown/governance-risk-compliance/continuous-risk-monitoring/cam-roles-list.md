---
title: CAM user roles
description: Assign users and groups with roles to prepare them to user the CAM application.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: reference
last_updated: "2025-10-08"
reading_time_minutes: 6
breadcrumb: [Reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# CAM user roles

Assign users and groups with roles to prepare them to user the CAM application.

## Role permissions and responsibilities

<table id="table_o14_t2s_2mb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Authorization Official\(sn\_irm\_cont\_auth.authorization\_official\)

</td><td>

Responsible for accepting an information system into an operational environment at a known risk level.The Authorization Official is entitled to approve and update authorization packages.

You can perform the following actions:

-   Activate/Deactivate Package
-   Generate SSP
-   Generate SAR
-   Generate POA&amp;M
-   Refresh Risk Summary
-   Approve the approval requests


You can read the following:

-   Authorization Boundary \(If Authorization official is named\)
-   Authorization Package \(If Authorization official is named\)
-   System Elements
-   Information Types
-   Information Types Library
-   Control Objectives
-   Control Objective Requirements
-   Control Overlays
-   All Controls
-   Control Requirements
-   Assessment Procedures
-   POA&amp;Ms

You can update the following fields in the package:

-   Mission/Business process
-   Add comments
-   Name
-   Acronym
-   800-53 version
-   System purpose
-   PTA/PIA section fields
-   Roles and responsibilities section \(SCA, ISSO, ISSM, AODR\)

Active


</td><td>

sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

Continuous Authorization and Monitoring administrator\(sn\_irm\_cont\_auth.admin\)

</td><td>

Responsible for all system administration duties in the CAM application.You can create, read, update, and delete the following:

-   Authorization Boundary
-   Boundary Filter \(You have access to create\)
-   System Elements \(You have access to create and read\)
-   Delete Authorization Boundary
-   Authorization Package
-   Activate/Deactivate Package
-   Move the Package to Next Stage
-   Information Types
-   Baseline Controls Add
-   Baseline Controls Mark as Common
-   Baseline Controls Mark as Not Applicable
-   Baseline Controls Inherit from Provider
-   Baseline Controls Hybrid
-   Baseline Controls - Return to Baseline Control
-   Generate SSP
-   Generate SAR
-   Generate POA&amp;M
-   Export OSCAL
-   Refresh Risk Summary
-   Back To Previous
-   Delete Authorization Pack
-   Send PIA
-   PIA Take Response
-   PIA View Response
-   Update Control Overlay on Package
-   Information Types Library
-   Control Objectives \(You have access to create, read, and update\)
-   Control Objectives Requirement \(You have access to create, read, and update\)
-   Control Overlays \(You have access to create, read, and update\)
-   Issues \(You have access to create, read, and update\)
-   All Engagements
-   Control Tests
-   Test Plans
-   Test Templates
-   All Controls
-   Control Requirement
-   Assessment Procedures

You can update the POA&amp;Ms.

</td><td>

-   sn\_audit.manager
-   sn\_irm\_cont\_auth.reader
-   sn\_irm\_cont\_auth.scheduler
-   sn\_compliance.admin
-   sn\_audit.admin
-   sn\_doc.admin
-   sn\_risk.admin
-   sn\_grc\_workspace.state\_model\_admin
-   sn\_grc\_doc\_design.admin
-   sn\_irm\_shared\_cmn.word\_template\_creator

</td></tr><tr><td>

Executive Reader\(sn\_irm\_cont\_auth.executive\_read\)

</td><td>

Read-only access to all modules of the CAM application.You can read the following:

-   Authorization Boundary
-   Boundary Filter
-   System Elements
-   Authorization Package
-   Information Types
-   Refresh Risk Summary
-   Information Types Library
-   Control Objectives
-   Control Objectives Requirement
-   Control Overlays
-   Control Tests
-   Test Plans
-   Test Templates
-   All Controls
-   Control Requirement
-   Assessment Procedures
-   POA&amp;Ms

</td><td>

sn\_irm\_cont\_auth.reader. Users with this role can access CAM Workspace.

</td></tr><tr><td>

Information Owner\(sn\_irm\_cont\_auth.information\_owner\)

</td><td>

Responsible for statutory, management, or operational authority and the establishment of policies and procedures governing its generation, collection, processing, dissemination, and disposal. The user can also update information types of an authorization package.You can create, read, update, and delete the following:

-   PIA Take Response
-   PIA View Response
-   Information Types \(You have access to create and delete\)
-   Refresh Risk Summary
-   Assessment Procedures
-   Issues \(You have access to create, read, and update\)
-   Test Plans \(You have access to create, read, and update\)
-   Test Templates \(You have access to create, read, and update\)

You can read the following:

-   Authorization Boundary
-   System Elements
-   Authorization Package
-   Information Types Library
-   Control Objectives
-   Control Objectives Requirement
-   Control Overlays
-   All Engagements
-   Control Tests
-   All Controls
-   Control Requirement

You can update the POA&amp;Ms.

</td><td>

-   sn\_audit.user
-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

Information System Security Manager\(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)

</td><td>

Responsible for conducting information system security management activities. They develop and maintain the system-level cybersecurity program.Can update the authorization package.

You can create, read, update, and delete the following:

-   Activate/Deactivate Package
-   Generate SSP
-   Generate SAR
-   Generate POA&amp;M
-   Export OSCAL
-   Refresh Risk Summary
-   PIA Take Response
-   PIA View Response
-   Update Control Overlay on Package
-   Authorization Package \(You can only read and update\)
-   Control Objectives \(You can only create, read, and update\)
-   Control Objectives Requirement \(You can only create, read, and update\)
-   Control Overlays \(You can only create, read, and update\)
-   Issues \(You can only create, read, and update\)
-   All Controls \(You can only create, read, and update\)
-   Control Requirement \(You can only create, read, and update\)

You can read the following:

-   Authorization Boundary
-   System Elements
-   Information Types
-   Information Types Library
-   Assessment Procedures

You can update the POA&amp;Ms.

</td><td>

-   sn\_compliance.user
-   sn\_irm\_cont\_auth.reader
-   sn\_risk.user

</td></tr><tr><td>

Information System Security Officer\(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)

</td><td>

Responsible for ensuring that the appropriate operational security posture is maintained for an information system.Can update the authorization package.

You can create, read, update, and delete the following:

-   Activate/Deactivate Package
-   Move the Package to Next Stage
-   Baseline Controls Add
-   Baseline Controls Mark as Not Applicable
-   Baseline Controls Mark as Common
-   Baseline Controls Inherit from Provider
-   Baseline Controls Hybrid
-   Baseline Controls - Return to Baseline Control
-   Generate SSP
-   Generate SAR
-   Generate POA&amp;M
-   Export OSCAL
-   Refresh Risk Summary
-   Send PIA
-   PIA Take Response
-   PIA View Response
-   Update Control Overlay on Package
-   Assessment Procedures
-   Information Types Library \(You can only read and update\)
-   Authorization Package \(You can only read and update\)
-   Control Objectives \(You can only create, read, and update\)
-   Control Objectives Requirement \(You can only create, read, and update\)
-   Control Overlays \(You can only create\)
-   Test Plans \(You can only create, read, and update\)
-   Test Templates \(You can only create, read, and update\)
-   All Controls \(You can only create, read, and update\)
-   Control Requirement \(You can only create, read, and update\)

You can update the following:

-   POA&amp;Ms
-   Authorization Boundary

You can read the following:

-   System Elements
-   Information Types
-   All Engagements
-   Control Tests

</td><td>

-   sn\_risk.user
-   sn\_compliance.user sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

Reader\(sn\_irm\_cont\_auth.reader\)

</td><td>

Read-only role. Users with this role can access CAM Workspace.You can read the following:

-   Information Types
-   Information Types Library
-   Control Objectives
-   Control Objectives Requirement
-   Control Overlays
-   Control Tests
-   Test Plans
-   Test Templates
-   All Controls
-   Control Requirement
-   Assessment Procedures
-   POA&amp;Ms

</td><td>

-   sn\_vul.read\_all
-   sn\_si.read
-   sn\_audit.reader
-   sn\_incident\_read
-   sn\_grc\_workspace.task\_reader
-   sn\_change\_read
-   sn\_compliance.reader
-   sn\_grc\_workspace.user

</td></tr><tr><td>

Scheduler\(sn\_irm\_cont\_auth.scheduler\)

</td><td>

Responsible for running all scheduled jobs for the application. This role is for a technical user.

</td><td>

sn\_irm\_cont\_auth..system\_owner

</td></tr><tr><td>

Security Control Assessor\(sn\_irm\_cont\_auth.sec\_control\_assessor\)

</td><td>

Responsible for conducting a thorough assessment of the management, operational, and technical security controls of an information system.You can create, read, update, and delete the following:

-   Refresh Risk Summary
-   PIA Take Response
-   PIA View Response
-   Assessment Procedures
-   Authorization Package \(You can only read and update\)
-   All Engagements \(You can only read and update\)
-   Control Tests \(You can only read and update\)
-   Test Plans \(You can only create, read, and update\)
-   Test Templates \(You can only create, read, and update\)
-   All Controls \(You can only create, read, and update\)
-   Control Requirement \(You can only create, read, and update\)
-   Control Objectives \(You can only create, read, and update\)
-   Control Objectives Requirement \(You can only create, read, and update\)
-   Control Overlays \(You can only create, read, and update\)

You read the following:

-   Authorization Boundary
-   System Elements
-   Information Types
-   Information Types Library

You can update the POA&amp;Ms.

</td><td>

-   sn\_audit.manager
-   sn\_compliance.user
-   sn\_irm\_cont\_auth.reader

</td></tr><tr><td>

System Owner\(sn\_irm\_cont\_auth.system\_owner\)

</td><td>

Responsible for procuring, developing, integrating, modifying, operating, and maintaining an information system.You can create, read, update, and delete the following:

-   Authorization Boundary
-   Boundary Filter
-   System Elements
-   Delete Authorization Boundary
-   Authorization Package
-   Activate/Deactivate Package
-   Move the Package to Next Stage
-   Information Types
-   Baseline Controls Mark as Common
-   Baseline Controls Inherit from Provider
-   Baseline Controls Hybrid
-   Baseline Controls - Return to Baseline Control
-   Generate SSP
-   Generate SAR
-   Generate POA&amp;M
-   Export OSCAL
-   Refresh Risk Summary
-   Send PIA
-   PIA Take Response
-   PIA View Response
-   Update Control Overlay on Package
-   Assessment Procedures
-   Control Objectives \(You don’t access to delete\)
-   Control Objectives Requirement \(You don’t access to delete\)
-   Test Plans \(You don’t access to delete\)
-   Test Templates \(You don’t access to delete\)
-   All Controls \(You don’t access to delete\)
-   Control Requirement \(You don’t access to delete\)

You can read the following:

-   Information Types Library
-   All Engagements
-   Control Tests

You can create the Control Overlays.

You can update the POA&amp;Ms.

</td><td>

-   sn\_audit.user
-   sn\_compliance.user
-   sn\_irm\_cont\_auth.reader
-   sn\_risk.user

</td></tr><tr><td>

System User\(sn\_irm\_cont\_auth.system\_user\)

</td><td>

Responsible for performing actual work in the system. They can update authorization boundaries, filter, elements, milestones, and acceptance tasks.

</td><td>

-   business user
-   sn\_audit.user
-   sn\_irm\_cont\_auth.reader

</td></tr></tbody>
</table>**Parent Topic:**[CAM reference](../concept/reference-grc-cam.md)

