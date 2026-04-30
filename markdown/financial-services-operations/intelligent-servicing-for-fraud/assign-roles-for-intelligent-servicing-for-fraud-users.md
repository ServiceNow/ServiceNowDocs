---
title: Assign roles for Intelligent Servicing for Fraud users
description: Assign roles to control access to features, capabilities, and data in the Intelligent Servicing for Fraud application.
locale: en-US
release: xanadu
product: Intelligent Servicing for Fraud
classification: intelligent-servicing-for-fraud
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Intelligent Servicing for Fraud, Intelligent Servicing for Fraud, Banking applications, Financial Services Operations \(FSO\)]
---

# Assign roles for Intelligent Servicing for Fraud users

Assign roles to control access to features, capabilities, and data in the Intelligent Servicing for Fraud application.

## Before you begin

Role required: sn\_bom\_fraud.admin or admin

## About this task

Users with the roles listed in the following table can use the Intelligent Servicing for Fraud application.

<table id="table_qzw_m3l_4pb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_bom\_fraud.admin

</td><td>

Creates, reads, updates, and deletes \(CRUD\) operations on fraud cases.

</td><td>

-   decision\_table\_admin
-   sn\_bom.service\_definition\_admin
-   sn\_bom\_fraud.agent
-   sn\_doc\_processor.admin

</td></tr><tr><td>

sn\_bom\_fraud.agent

</td><td>

Accesses and views fraud data as a fraud agent.

</td><td>

-   sn\_doc\_processor.agent
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

sn\_bom\_fraud.viewer

</td><td>

Grants access to view fraud cases.

</td><td>

-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr><tr><td>

sn\_bom\_fraud.manager

</td><td>

Approves or rejects fraud cases.

</td><td>

sn\_bom\_fraud.agent

</td></tr><tr><td>

sn\_bom\_fraud.contributor

</td><td>

Creates a fraud case on behalf of the customer.

</td><td>

-   sn\_bom.account\_viewer
-   sn\_doc\_processor.collector
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_sla\_definition\_read
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr><tr><td>

sn\_bom\_fraud.agent\_connector

</td><td>

Creates, views, and edits fraud cases and works with consumers to resolve cases.

</td><td>

-   sn\_doc\_processor.agent
-   sn\_sla\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr></tbody>
</table>## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    -   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

