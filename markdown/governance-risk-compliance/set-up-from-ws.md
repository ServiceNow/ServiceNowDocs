---
title: Set up pillars and entity types from Workspace UI
description: Set up the pillars and entity types from the Operational Resilience Workspace UI. You must activate the pillars first and then activate the entity types. If you prefer the classic experience, you can navigate to the module using the Admin setup in the Core UI.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up pillars, entity types, entity filters, and entities, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up pillars and entity types from Workspace UI

Set up the pillars and entity types from the Operational Resilience Workspace UI. You must activate the pillars first and then activate the entity types. If you prefer the classic experience, you can navigate to the module using the Admin setup in the Core UI.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** and select **Setup****Pillars** from the List view.

    The list of pillars available with the base system are shown in the example. All pillars are shipped in the inactive state.

    ![Pillars view.](../image/setup-pillars-view.png)

    For information on the default and supporting pillars, refer to the following table.

<table id="table_npy_1fg_d3c"><thead><tr><th>

Total pillars

</th><th>

Default pillars

</th><th>

Supporting pillars

</th></tr></thead><tbody><tr><td>

Here are the available pillars: -   Application Services
-   Business Services
-   Data
-   Facilities
-   Processes
-   People
-   Services
-   Service Offerings
-   Suppliers
-   Technology


</td><td>

The default pillars are listed: -   Business Services
-   Processes
-   Services
-   Service Offerings


</td><td>

The supporting pillars are listed: -   Application Services
-   Data
-   Facilities
-   People
-   Suppliers
-   Technology


</td></tr></tbody>
</table>    Beginning with Operational Resilience, Release 21.x.x, the \[sn\_grc\_choice\] table includes an **Active** field. The pillars are shipped in an inactive state by default. You must activate the pillars from the list view before activating the entity types, as the entity types depend on the pillars. You can activate entity types only after activating the pillars.

2.  Activate the pillars first by opening the desired GRC Choice pillar records.

    **Note:** Verify that you are editing this record in the GRC: Operational Resilience application. Switch scope in the UI if necessary so that you can activate the pillars.

    1.  Select the pillar that you want to activate.

        For more information on the fields in the form, see [GRC Choices form](../reference/pillars-reference.md).

    2.  Select the Active check box.

        The example shows how you can activate the Business Services pillar.

        ![Activate the Business Services pillar.](../image/activate-bs-pillar.png)

    3.  To save the settings, select **save**.

        The active setting for the Business Services pillar is marked as "true."

        ![Business Services pillar is marked as "true".](../image/bs-pillar-activated.png)

    4.  To activate other pillars according to your requirements, repeat these steps.

        **Note:** Pillars must be activated before activating the entity types. Attempting to activate entity types while their parent pillars are inactive leads to an error.

3.  Activate the entity types next.

    1.  Switch to the **Entity types** module from the Workspace List view.

    2.  Review default entity types that are filtered by active pillars.

    3.  Activate an entity type by selecting and opening its record.

        For more information on the fields in the form, see [Entity type New record form](../reference/entity-type-reference.md).

        The example shows the entity types that are set up in the instance.

        ![Entity types view.](../image/setup-entity-types-view-ws.png)

    4.  Select the Active check box.

        The example shows that the Active check box is selected.

        ![Active check box is selected.](../image/bs-ent-type-marked-active.png)

    5.  Add optional **Description**.

    6.  To save entity type, select **Save**.

        The example shows that the entity type is set to active.

        ![Entity type is set to active.](../image/bs-ent-type-set-to-true.png)

    7.  Repeat these steps for all required entity types.

4.  Create a custom entity type.

    1.  From Entity types view, select **New**.

        The example shows how to create an entity type.

        ![How to create an entity type.](../image/ent-type-create-new.png)

    2.  Enter **Name**.

    3.  Select the Active check box.

    4.  Add **Description**.

    5.  Select a pillar from the available options.

    6.  Add a functional domain for the entity type such as IT risk and compliance.

    7.  To save settings and create entity type, select **Save**.

        The entity type is displayed in the Setup - Entity types list.


## What to do next

Once pillars and entity types are set up from the Workspace UI, configure the entity filters. For more information, see [Configure the entity filters](conf-ent-filter.md).

