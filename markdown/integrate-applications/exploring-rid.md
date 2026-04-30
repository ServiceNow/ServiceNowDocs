---
title: Exploring Requirement Intake Diagram
description: Learn about the Requirement Intake Diagram application key features, flow, and workspace.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-05"
reading_time_minutes: 1
breadcrumb: [Requirement Intake Diagram, Creating integrations with applications]
---

# Exploring Requirement Intake Diagram

Learn about the Requirement Intake Diagram application key features, flow, and workspace.

## Requirement Intake Diagram overview

Use Requirement Intake Diagram to design the automation requirements visually. The diagram provides a way to visualize the complete requirements, which depend on different departments and involve multiple activities. Once the diagram is created, it will be translated into a detailed Playbook Experience process, which can then be configured and executed as actual running automation.

## Requirement Intake Diagram users

<table id="table_ddp_3pg_wtb"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

-   sn\_ac.automation\_admin
-   playbook.activity\_def\_read
-   playbook.write
-   connection\_admin
-   cmdb\_read

</td><td>

Sets up Requirement Intake Diagram application configurations. Performs all the actions in the Requirement Intake Diagram application. Possesses CRUD access for all tables.

</td><td>

-   sn\_ac.automation\_business\_user
-   sn\_ac.automation\_technical\_user
-   sn\_ac.automation\_admin

</td></tr><tr><td>

-   sn\_ac.automation\_technical\_user
-   playbook.activity\_def\_read
-   playbook.write
-   connection\_admin
-   cmdb\_read

</td><td>

Creates a requirement diagram, translates it into a Playbook Experience process, and eventually creates the automation.

</td><td>

playbook.write contains pd\_shared.user

</td></tr><tr><td>

-   sn\_ac.automation\_business\_user
-   playbook.activity\_def\_read
-   playbook.write

</td><td>

Requests for an automation by providing the requirement diagram.

</td><td>

playbook.write contains pd\_shared.user

</td></tr></tbody>
</table>## Requirement Intake Diagram flow

The following diagram shows the flow of the Requirement Intake Diagram. Users with sn\_ac.automation\_business\_user, playbook.activity\_def\_read, and playbook.write roles request a requirement diagram. Users with sn\_ac.automation\_technical\_user, playbook.activity\_def\_read, playbook.write, connection\_admin, and cmdb\_read roles create a requirement diagram, translate it into a Playbook Experience process, and eventually creates the automation.

![This image describes the flow of how a diagram is requested, created, and then translated to a Playbook Experience process, and then an automation.](../images/rid-flow.png "Requirement Intake Diagram flow")

1.  The requester or business user submits an automation request from the Service Portal.
2.  After saving the request, the fulfiller or technical user gets a review request for the automation request.
3.  The fulfiller or technical user checks if the requirement diagram is available.

    If the diagram is not available, the fulfiller or technical user sends a request to the requester or business user to create a requirement diagram.

4.  If the diagram is available, the fulfiller or technical user starts creating the automation in the Workflow Studio using Playbook Experience.

