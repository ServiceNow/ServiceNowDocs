---
title: Edit a data interface
description: Update a published data interface in place when source data or consumer requirements change, without unpublishing or recreating the interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/edit-data-interface-wdf.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 3
breadcrumb: [Managing data interfaces, Data Products, Workflow Data Fabric]
---

# Edit a data interface

Update a published data interface in place when source data or consumer requirements change, without unpublishing or recreating the interface.

## Before you begin

The data interface must be in the Published state.

Role required: data\_product\_admin, df\_data\_steward, delegated\_developer, df\_data\_steward, and delegatedadmin \(scope admin\)

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Data Workbench**.

2.  Open the published data interface and select **Edit**.

    An edit mode banner appears at the top of the wizard and remains visible throughout the edit session as a reminder that table, column, and combination changes affect consumers and that consumers aren't notified automatically.

3.  Update the interface label and select **Continue**.

    The **Unique name** field is locked because downstream consumers reference the data interface by name.

4.  On the **Select source tables** page, add or remove source tables and select **Continue**.

    **Note:** You can't remove a source table that is referenced by a join condition. Remove the join condition first.

5.  On the **Combination method** step, keep or change the combination method and select **Continue**.

    If you select a different combination method, the Change combination method dialog opens. Select **Change method** to restructure the target table, remove the current column mappings, and clear any saved join configurations. This action can't be undone.

6.  On the **Select columns** step, update the column selection and select **Continue**.

7.  On the **Define target table** step, review the column mappings, adjust target column labels and types as needed, and select **Create table**.

    For target columns that were part of the published interface, the column name is locked. The target column label and type remain editable. If you select a target type that doesn't match the source type, the field shows a type-mismatch warning.

    If you made structural changes — added or removed source tables, changed the combination method, or changed join conditions — the Confirm structure changes dialog opens. The dialog lists the structural changes that will be applied. Select **Confirm changes** to apply them. The earlier wizard steps lock and the wizard advances to the **Connect and verify** step. All source tables must be re-verified and permissions reviewed before you can save.

8.  On the **Connect and verify** step, verify each source table.

    The **Tables verified** count on the Data interface summary panel tracks progress. The **Preview output** button remains inactive until all tables are verified.

    1.  Select **Connect and verify** next to a source table.

    2.  Select the connector for your source system from the list of available connections.

    3.  Select **Verify**.

        The table shows a Verified status when the connection is confirmed.

9.  Review sample data from the updated interface by selecting **Preview output**.

    The preview shows the top 10 live records from the combined output. Confirm the columns and data match what consumers expect before continuing.

10. Review the permissions and select **Continue**.

    For data interfaces built on external source tables such as Snowflake, the access roles required are configured automatically.

    **Note:** For data interfaces that includes any ServiceNow tables, this step requires a manual permissions request. Copy the email template provided and send it to your security administrator. The security administrator must add the correct read roles to the composite role generated for the data interface. Select the confirmation check box before continuing.

11. Review the updated data interface configuration on the **Review** page and select **Save changes**.

    The edits are applied and the data interface overview page opens. The data interface remains in the Published state.


## Result

The published data interface reflects your updates. Existing consumers continue to use the data interface but must reconnect and verify their tables to pick up structural changes such as added or removed source tables, a changed combination method, or new target columns.

**Important:** There is a delay between saving an edit and its appearance in the Data Catalog. The metadata collector must run before consumers see the changes. To make the changes available without waiting for the scheduled run, ask your administrator to run the collector manually from Connect Hub.

**Parent Topic:**[Managing data interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/manage-data-interfaces_wdf.md)

