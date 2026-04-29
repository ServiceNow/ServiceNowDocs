---
title: Integration between EAP and Agile Development 2.0
description: While setting up a configuration in Enterprise Agile Planning, you can establish an integration with Agile Development 2.0. Learn more about the tables connected and the way you access the information.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Integration between EAP and Agile Development 2.0

While setting up a configuration in Enterprise Agile Planning, you can establish an integration with Agile Development 2.0. Learn more about the tables connected and the way you access the information.

![Option to enable sync with Agile Development 2.0 in EAP Configuration.](../images/eap-new-config-form.png)

In the EAP configuration form, when you enable the **Sync with Agile Development** option, information of the following tables is synced between the two apps.

<table id="table_p3h_2qz_21c"><thead><tr><th>

EAP tables

</th><th>

Agile Development 2.0 tables

</th></tr></thead><tbody><tr><td>

Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\]

</td><td>

Sprint \[rm\_sprint\]

</td></tr></tbody>
</table>When this sync is established for a configuration, the following are the functionality changes:

-   **Sprint creation and updates**
    -   Creating a Sprint is suggested to be done from EAP.
    -   Creating a Sprint in EAP creates a related Sprint in Agile Development 2.0.

        If the dates of the Sprint in EAP overlap with a record in the rm\_sprint table, then a new Sprint isn’t created for Agile Development 2.0. You can either choose to create sprints for non-overlapping dates or delete the existing sprint from the rm\_sprint table.

    -   Fields of planned start and end dates for Sprints in Agile Development 2.0 become read-only, and are derived from the business calendar spans mapped to the iterations in EAP.
    -   Updating Sprint details in EAP updates the corresponding Sprint details in Agile Development 2.0.
    -   Deleting Sprints from EAP deletes the corresponding record from the Sprint \[rm\_sprint\] table.
    -   On the Sprint \[rm\_sprint\] table, reference fields are created for parent of the EAP iteration and the EAP team this iteration belongs to.
-   **Story creation and updates**
    -   All Stories scheduled for any Sprints in this configuration can be accessed in Sprints of Agile Development 2.0.

        You can track the progress of this Sprint from the Agile board.

    -   Any changes made to the story details or its progress are visible in both the applications.
    -   On the Story \[rm\_story\] table, reference fields are created for EAP team, iteration, configuration, and parent work item in the EAP fields related list.
    -   If a story is rescheduled to a different sprint or moved to the Backlog on the Agile board, it's updated in EAP and vice versa.

**Note:** The Story records for EAP are by default saved in the Story \[rm\_story\] table, which is installed with the Agile Development 2.0 plugin.

**Parent Topic:**[Enterprise Agile Planning reference](eap-reference.md)

