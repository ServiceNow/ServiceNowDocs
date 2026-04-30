---
title: Access limitations for external location agents
description: Explore the limitations that an external location agent faces when using various platform modules during case resolution. You can use this topic to get a comprehensive overview of the modules that are supported and unsupported with the external location agent persona.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [External business location \(EBL\) as a fulfiller, Service Model Foundation cases, Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Access limitations for external location agents

Explore the limitations that an external location agent faces when using various platform modules during case resolution. You can use this topic to get a comprehensive overview of the modules that are supported and unsupported with the external location agent persona.

## Supported and unsupported modules

List of modules and submodules under the customer service platform that are supported and unsupported:

<table id="table_fjn_lyd_ybc"><thead><tr><th>

Modules

</th><th>

Submodules

</th><th>

Supported/unsupported

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

 

</td><td>

Supported

</td></tr><tr><td>

Knowledge

</td><td>

 

</td><td>

Supported

</td></tr><tr><td rowspan="8">

Cases

</td><td>

Create New

</td><td rowspan="8">

Supported

</td></tr><tr><td>

My Cases

</td></tr><tr><td>

Assigned to My Locations

</td></tr><tr><td>

Requested by My Locations

</td></tr><tr><td>

All

</td></tr><tr><td>

Open

</td></tr><tr><td>

Unassigned

</td></tr><tr><td>

Escalated

</td></tr><tr><td>

Escalations

</td><td>

All

</td><td>

Supported

</td></tr><tr><td rowspan="3">

Customer

</td><td>

Partners

</td><td rowspan="3">

Supported

</td></tr><tr><td>

Accounts

</td></tr><tr><td>

Contacts

</td></tr><tr><td>

Customer Relationships

</td><td>

Account Team Members

</td><td>

Supported

</td></tr><tr><td rowspan="3">

Service Organization

</td><td>

Internal Business Locations

</td><td rowspan="3">

Supported

</td></tr><tr><td>

External Business Locations

</td></tr><tr><td>

Service Organization External Staffs

</td></tr><tr><td rowspan="2">

Contracts

</td><td>

Service Contracts

</td><td rowspan="2">

Unsupported

</td></tr><tr><td>

Entitlements

</td></tr><tr><td rowspan="3">

Products

</td><td>

Assets

</td><td>

Supported

</td></tr><tr><td>

Product Models

</td><td>

Unsupported**Note:** All configuration management database \(CMDB\) tables are unsupported.

</td></tr><tr><td>

Outsourced Service Providers

</td><td>

Supported

</td></tr><tr><td rowspan="4">

Interaction

</td><td>

All

</td><td rowspan="4">

Unsupported

</td></tr><tr><td>

Active

</td></tr><tr><td>

Assigned to Me

</td></tr><tr><td>

Overview

</td></tr><tr><td>

Special Handling Notes

</td><td>

Special Handling Notes

</td><td>

Supported

</td></tr><tr><td>

Configuration

</td><td>

 

</td><td>

Unsupported

</td></tr><tr><td rowspan="7">

**Knowledge** &gt; **Articles**

</td><td>

Create New

</td><td rowspan="3">

Unsupported

</td></tr><tr><td>

Import Articles

</td></tr><tr><td>

Open Submissions

</td></tr><tr><td>

Unpublished

</td><td rowspan="4">

Supported

</td></tr><tr><td>

Published

</td></tr><tr><td>

Retired

</td></tr><tr><td>

All

</td></tr><tr><td rowspan="4">

**Knowledge** &gt; **Feedback Management**

</td><td>

My Flagged

</td><td rowspan="4">

Supported

</td></tr><tr><td>

My Submitted Tasks

</td></tr><tr><td>

My Assigned Tasks

</td></tr><tr><td>

My Closed Tasks

</td></tr><tr><td>

**Knowledge** &gt; **Homepage**

</td><td>

 

</td><td>

Supported

</td></tr><tr><td>

**Knowledge** &gt; **Notification Settings**

</td><td>

 

</td><td>

Unsupported

</td></tr><tr><td>

Email Client

</td><td>

Email Drafts

</td><td>

Unsupported

</td></tr><tr><td>

Workspaces

</td><td>

CSM Configurable Workspace

</td><td>

Unsupported**Note:** All aspects of the workspace experience remain inaccessible to external location agents.

</td></tr></tbody>
</table>Other notable limitations:

-   The Launch Interactive Analysis option in the Case list form context menu isn’t functional.
-   Related cases can’t be accessed from the related search results on the Case.

However, with an external business location as a fulfiller, the external location agents can:

-   Access Service Model Foundation data, such as internal business location, external business location, service organization members, and responsibilities, on the platform.
-   Access customer foundation data, including accounts, contacts, sold products, and install base items on the platform.
-   Access the case form on the platform.
-   Self-assign and start working on a case.
-   View related search results.
-   Add comments or work notes.
-   View the activity stream, work notes, and case timelines.
-   Add resolution notes, propose a solution, and close the case.
-   Create and update case tasks.
-   View service definitions.

