---
title: Roles installed with Impact
description: Impact offers many roles to assign to fit your business needs. When you log in to Impact, you’ll see a personalized view of your objectives, metrics, and recommendations tied directly to your role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/impact-roles.html
release: brazil
topic_type: reference
last_updated: "2026-11-04"
reading_time_minutes: 3
breadcrumb: [General reference, Impact reference, Impact]
---

# Roles installed with Impact

Impact offers many roles to assign to fit your business needs. When you log in to Impact, you’ll see a personalized view of your objectives, metrics, and recommendations tied directly to your role.

Impact platform roles control access across administration, development support, code scanning, system monitoring, and user engagement. Assign roles based on user responsibilities and access requirements.

<table><thead><tr><th>

Category

</th><th>

Role

</th><th>

API Role Name

</th><th>

Key Capabilities

</th></tr></thead><tbody><tr><td>

Administrative

</td><td>

Impact Platform Owner

</td><td>

sn\_impact\_common.Impact Platform Owner

</td><td>

-   Full access to all Impact features
-   Premium access management for Instance Observer and Developer Support
-   Access Platform Owner dashboard
-   Request Accelerators and advisory sessions
-   Can't assign or configure roles to users or groups \(See Impact App Admin\)

</td></tr><tr><td>

Administrative

</td><td>

Impact Portfolio Owner

</td><td>

sn\_impact\_common.Impact Portfolio Owner

</td><td>

-   Full CRUD on Impact tables
-   Access Platform Owner dashboard
-   Request Accelerators and advisory sessions

</td></tr><tr><td>

Administrative

</td><td>

Impact Permissions Authorizer

</td><td>

Impact Permissions Authorizer

</td><td>

-   Approve permissions for Impact features requiring consent
-   Manage initiative permissions
-   Manage group permissions
-   Approve pending activity requests
-   Decline pending activity requests

</td></tr><tr><td>

Administrative

</td><td>

Impact Admin

</td><td>

sn\_impact\_common.Impact Admin \(BDA\)

</td><td>

-   Full access to all Impact features
-   Premium access management for Instance Observer and Developer Support
-   User account management
-   Day-to-day platform administration

</td></tr><tr><td>

Administrative and Scan Engine

</td><td>

Impact App Admin

</td><td>

sn\_impact\_common.Impact App Admin

</td><td>

-   Full CRUD access to Impact tables
-   Assign and configure roles to users or groups
-   Configure Platform Health
-   Scan Engine capabilities:
    -   Manage scan settings
    -   Manage exception reasons
    -   Initiate scans
    -   Execute scans

</td></tr><tr><td>

Development and Scan Engine

</td><td>

Impact Developer

</td><td>

sn\_impact\_common.Impact Developer

</td><td>

-   Access Scan Engine findings and developer workflows
-   View personal technical debt and findings
-   Perform on-demand scans excluding scheduled scans
-   Access developer dashboard
-   View Scan Engine results
-   Submit exception requests

</td></tr><tr><td>

Development and Scan Engine

</td><td>

Development Team Lead

</td><td>

sn\_impact\_common.Impact Development Team Lead

</td><td>

-   View all team findings and scan results
-   Manage team members
-   Access Development Team Lead dashboard
-   Perform on-demand scans excluding scheduled scans

</td></tr><tr><td>

Development and Support

</td><td>

Impact Developer Support

</td><td>

Impact Developer Support

</td><td>

-   Submit Developer Support cases for break-fix troubleshooting for Advanced and Total packages
-   Request custom development work

</td></tr><tr><td>

Instance Observer

</td><td>

IO Standard

</td><td>

io\_standard

</td><td>

-   Full access to all Instance Observer features
-   Create alert rules, manage alert rules, manage alert groups
-   Access performance dashboards, generate reports, manage dashboards, triage alerts
-   Schedule reports
-   Access availability insights

</td></tr><tr><td>

Instance Observer

</td><td>

IO Read Only

</td><td>

io\_readonly

</td><td>

-   View alerts
-   View rules
-   View integrations
-   View reports

</td></tr><tr><td>

User-Level

</td><td>

Impact Executive

</td><td>

sn\_impact\_common.Impact Executive

</td><td>

-   Read access to all Impact features
-   Access Executive Dashboards, Scan Engine
-   Access strategic documents, capability maps, adoption roadmaps, objectives, and value journey
-   Create and update conversations

</td></tr><tr><td>

User-Level

</td><td>

Impact User

</td><td>

sn\_impact\_common.Impact User

</td><td>

-   Read-only access to Impact
-   Read-only access to all tables
-   Create and update conversations

</td></tr><tr><td>

User-Level

</td><td>

Impact Partner

</td><td>

sn\_impact\_common.Impact Partner

</td><td>

-   Read-only access to Impact
-   Read access to Capabilities Maps, Product Adoption Roadmaps, Objectives, and Accelerators
-   Request advisory sessions

</td></tr></tbody>
</table>## Scan Engine roles and groups

After installation, Scan Engine provides groups that include the Scan Engine roles, so you can assign access by group instead of creating groups manually. The groups don't change the existing Impact role hierarchy.

<table><thead><tr><th>

Role

</th><th>

API Role Name

</th><th>

Included in groups

</th><th>

Key Capabilities

</th></tr></thead><tbody><tr><td>

Scan Engine Admin

</td><td>

sn\_se.scan\_engine\_admin

</td><td>

Scan Engine Admin

</td><td>

-   Full access to all Scan Engine functions and results
-   Configure and manage Scan Engine
-   Manage exception reasons
-   Manage approval workflows
-   Enable AI-generated code fix capabilities
-   View all scan results and findings
-   Initiate scans

</td></tr><tr><td>

Scan Engine User

</td><td>

sn\_se.scan\_engine\_user

</td><td>

-   Scan Engine User
-   Code Fix User

</td><td>

-   Access Scan Engine findings
-   Access to scan initiation
-   View Scan Engine results

</td></tr><tr><td>

Scan Engine Read User

</td><td>

sn\_se.scan\_engine\_read\_user

</td><td>

-   Scan Engine Read User
-   Scan Engine Exception Approver

</td><td>

-   Read-only access to scan results, findings, and scan definitions
-   Can't initiate scans

</td></tr><tr><td>

Exception Approver

</td><td>

sn\_se.scan\_engine\_exception\_approver

</td><td>

Scan Engine Exception Approver

</td><td>

-   Approve and reject exception reason requests
-   Receive and triage exception notifications

</td></tr><tr><td>

AI Fix User

</td><td>

sn\_impact\_gen\_ai.ai\_fix\_user

</td><td>

Code Fix User

</td><td>

-   Access AI-generated code fix capabilities
-   View code fix suggestions from Now Assist
-   Apply AI-generated remediation code

</td></tr><tr><td>

Internal REST Integration

</td><td>

sn\_se.internal\_rest\_integration

</td><td>

None

</td><td>

-   Enable REST API calls between instances
-   Sync Scan Engine definitions
-   Sync exception reasons
-   Sync Update Set scanning data
-   Perform automated data synchronization

</td></tr><tr><td>

Platform REST API Access

</td><td>

snc\_platform\_rest\_api\_access

</td><td>

None

</td><td>

-   Allows REST API access when REST API access control lists are enabled on an instance
-   Required for the integration user only on instances where REST API access control lists are enabled

</td></tr></tbody>
</table>**Parent Topic:**[General reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/general-reference.md)

