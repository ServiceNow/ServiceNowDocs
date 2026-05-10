---
title: Flows in Table Builder
description: You can use the Workflow Studio functionality that is integrated within Table Builder to manage your table's record-based flows. You can manage these flows by using the Flows tab.Use the Flows tab in Table Builder to search and filter a list of flows that are triggered when selected table records are updated, created, or both.Add flows that are triggered when a table record is updated, created, or both updated and created by using the Flows tab in Table Builder.Edit flows that are triggered when table records that you select are updated, created, or both updated and created by using the Flows tab in Table Builder.Delete a record-based flow by using the Flows tab in Table Builder.Create a new record-based flow from an existing flow by using the Flows tab in Table Builder.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Flows in Table Builder

You can use the Workflow Studio functionality that is integrated within Table Builder to manage your table's record-based flows. You can manage these flows by using the **Flows** tab.

Workflow Studio is a ServiceNow AI Platform® feature that enables process owners to automate work. Build multi-step flows from reusable components without having to code.

The **Flows** tab within Table Builder is where you can view and work with record-based flows for a selected data table \(that is, actions that are triggered when a table record is created or updated or both\).

The following diagram shows flow cards in Table Builder.

![Flows tab.](../image/flows-tb.png "Flows tab")

**Parent Topic:**[Using Table Builder](using-fb.md)

## Find a record-based flow

Use the **Flows** tab in Table Builder to search and filter a list of flows that are triggered when selected table records are updated, created, or both.

### Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](fb-application-scope.md).

Role required: personalize\_forms, personalize\_dictionary, and flow\_designer permissions \(or relevant AES user role and delegated developer permissions\). For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Launch Table Builder as described in [Accessing Table Builder](accessing-form-builder.md).

2.  Select the **Flows** tab.

    The flows triggered by the selected table are listed as flow cards.

3.  ![Flows list.](../image/flows-list-tb.png "Flow cards list")

4.  Filter or search the list of flow cards as needed to find the desired flow.

<table id="table_zkp_3zn_15b"><thead><tr><th>

Option

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Search text

</td><td>

Type a keyword in the **Search** box. The list of cards will be filtered as you type.

</td></tr><tr><td>

Sort flows

</td><td>

Select an option from the sorting list to sort the flow cards.1.  Flow name \(a to z\)
2.  Flow name \(z to a\)
3.  Updated by \(a to z\)
4.  Updated by \(z to a\)
5.  Updated \(recent to last\) - Default option
6.  Updated \(last to recent\)


</td></tr><tr><td>

Filter flows by setting up filter criteria

</td><td>

1.  Select the filter icon \(![Filter flows.](../image/filter-flows.png)\).
2.  Add your filter condition criteria including any AND/OR logic.
3.  To add additional conditions, select **+ New condition set**.
4.  Select **Apply**.


</td></tr></tbody>
</table>
### What to do next

-   Select the flow card to edit your new flow using Workflow Studio. See [Modify a record-based flow](flows-tb.md#).
-   Create a new record-based flow from an existing one. See [Copy a record-based flow](flows-tb.md#).
-   Delete the flow. See [Delete a record-based flow](flows-tb.md#).

## Add a record-based flow

Add flows that are triggered when a table record is updated, created, or both updated and created by using the **Flows** tab in Table Builder.

### Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](fb-application-scope.md).

Role required: personalize\_forms, personalize\_dictionary, and flow\_designer permissions \(or relevant AES user role and delegated developer permissions\). For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Launch Table Builder as described in [Accessing Table Builder](accessing-form-builder.md).

2.  Select the **Flows** tab.

3.  Select the **Add new flow** button.

4.  On the New Flow form, fill in the following fields for your new flow.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify your flow. The system computes the internal name of the flow from the name.|
    |Description|Description of your flow.|

5.  To enter advanced options for your flow, select **Show advanced options** on the New Flow form.

<table id="table_kdg_zxh_ldb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protection

</td><td>

Option that you can select if the flow is read-only. You can only select a value when you create the flow in an application scope that you own.

</td></tr><tr><td>

Run as

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows.

 To create a flow that can run with a personal OAuth token, select the user who initiates the session option. If the user who is running the flow has a personal OAuth token, the flow runs with that token. For more information about creating a personal OAuth token, see [OAuth 2.0 credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/oauth-2-credentials.md).

 When flows run as the user who initiates the session, the system limits the flow actions by user access control list \(ACL\) restrictions. Ensure that security restrictions don't prevent users who trigger the flow from performing flow actions. Flows that are run by the initiating user also respect user-specific settings, such as the date/time formats.

 **Note:** Inbound email flows ignore this setting and always run as the user who initiates the session. To test access controls for an inbound email flow, impersonate a typical inbound email user and manually trigger the flow.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the flow runs with. This option is only available when **Run as** is set to **user who initiates the session**.

</td></tr></tbody>
</table>6.  Select **Continue**.

7.  Choose the event that your flow will be triggered by.

<table id="choicetable_nl2_cmz_ztb"><tbody><tr><td id="d80785e753">

**When the record is created**

</td><td>

Create a flow that is triggered when a record in the selected table is created.

</td></tr><tr><td id="d80785e762">

**When the record is updated**

</td><td>

Create a flow that is triggered when a record in the selected table is updated.

</td></tr><tr><td id="d80785e771">

**When the record is created or updated**

</td><td>

Create a flow that is triggered when a record in the selected table is created or updated.

</td></tr></tbody>
</table>    The flow that you just created is displayed in the flow diagramming view. See [Flow diagramming view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-diagramming-view.md).

8.  Select **Add node**, and then select one of the following options to modify your flow:

<table id="table_smq_3ys_tcb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Select the desired action. Workflow Studio includes [Workflow Studio actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-actions.md) that are available to flows and subflows. Alternatively, a user with the action\_designer role can create additional actions to add to flows. The [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/integrationhub.md) and [Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/spokes.md) plugins install additional actions.

 To add draft actions from the More Actions menu, set **Show draft actions** to **true**.

 To view spokes that are available in the ServiceNow Store, set **Show store spokes** to **true** from the More Actions menu.

**Note:** Under **Not Installed Spokes**, the system displays spokes that are available in the ServiceNow Store based on compatibility with the ServiceNow version and application dependency on Workflow Studio.

</td></tr><tr><td>

Flow Logic

</td><td>

Select an option to specify conditional or repeated operations.

</td></tr><tr><td>

Subflow

</td><td>

Select a published subflow and define the input values. In addition to adding a subflow as a flow action, you can enable the **Show triggered flows** option from the More Actions menu to select an activated flow and define the required inputs. Running a triggered flow ignores its trigger conditions and runs all actions.

</td></tr></tbody>
</table>    **Note:** Alternately, you may toggle the Workflow Studio default view from the view selector, and then select **Add an Action, Flow Logic, or Subflow** in that view of Workflow Studio. For more information, see [Flow diagramming view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-diagramming-view.md).

9.  Continue modifying your flow in Workflow Studio.

    **Note:** For detailed information on how to work with flows for your application, see [Create a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md).

10. Select **Save**.

    Workflow Studio saves a draft of the flow, trigger, and actions.


### What to do next

Test your flow until you're ready to activate it. For more information on testing and editing flows, see [Activate a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-activate.md).

**Note:** Your application can trigger only activated flows. For detailed information on how to design, test, and activate flows for your application, see [Flows in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-flows.md).

To return to the comprehensive list of flows related to the selected table after editing a flow, select the Additional actions \( ![Additional actions menu.](../image/ellipsisIcon.png)\) menu to the right of the **Flows** tab, and then select **All flows** as shown in the following example.

![All flows.](../image/return-to-flow-list.png "All flows")

## Modify a record-based flow

Edit flows that are triggered when table records that you select are updated, created, or both updated and created by using the **Flows** tab in Table Builder.

### Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](fb-application-scope.md).

Role required: personalize\_forms, personalize\_dictionary, and flow\_designer permissions \(or relevant AES user role and delegated developer permissions\). For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### About this task

The **Flows** tab in Table Builder provides a list of flows that are triggered by record changes to a table and enables you to manage them from the record table that triggers the workflow.

### Procedure

1.  Launch Table Builder as described in [Accessing Table Builder](accessing-form-builder.md).

2.  Select the **Flows** tab.

    The available flows that are triggered by the table are listed as flow cards.

3.  Filter or search the list of flow cards as needed to find the desired flow.

    See [Find a record-based flow](flows-tb.md#).

4.  Select a flow card to open the flow for editing.

5.  Edit the record-based flow by using Workflow Studio.

    For detailed information on how to work with flows for your application, see [Create a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md).

    **Note:** To return to the list of flow cards that are related to the table, select the Additional actions \( ![Additional actions menu.](../image/ellipsisIcon.png)\) menu to the right of the **Flows** tab, and then select **All flows**.

6.  Select **Save**.


### What to do next

Test your flow until you're ready to activate it. For more information on testing and editing flows, see [Activate a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-activate.md).

**Note:** Your application can trigger only activated flows. For detailed information on how to design, test, and activate flows for your application, see [Flows in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-flows.md).

To return to the list of flows related to the table that you selected after you edited a flow, select the Additional actions \( ![Additional actions menu.](../image/ellipsisIcon.png)\) menu to the right of the **Flows** tab, and then select **All flows** as shown in the following example.

![All flows.](../image/return-to-flow-list.png "All flows")

## Delete a record-based flow

Delete a record-based flow by using the **Flows** tab in Table Builder.

### Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](fb-application-scope.md).

Role required: personalize\_forms, personalize\_dictionary, and flow\_designer permissions \(or relevant AES user role and delegated developer permissions\). For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Launch Table Builder as described in [Accessing Table Builder](accessing-form-builder.md).

2.  Select the **Flows** tab.

    The available flows that are triggered by the table are listed as flow cards.

3.  Filter or search the list of flow cards as needed to find the desired flow.

    See [Find a record-based flow](flows-tb.md#).

4.  Select the Additional actions \( ![Additional actions menu.](../image/ellipsisIcon.png)\) menu in the top-right corner of the flow that you want to delete, and then select **Delete** from the list of options.

5.  In the delete confirmation window, enter `DELETE`, and then select **Delete**.

6.  Select **Save**.


## Copy a record-based flow

Create a new record-based flow from an existing flow by using the **Flows** tab in Table Builder.

### Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](fb-application-scope.md).

Role required: personalize\_forms, personalize\_dictionary, and flow\_designer permissions \(or relevant AES user role and delegated developer permissions\). For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Launch Table Builder as described in [Accessing Table Builder](accessing-form-builder.md).

2.  Select the **Flows** tab.

    The available flows that are triggered by the table are listed as flow cards.

3.  Filter or search the list of flow cards as needed to find the desired flow.

    See [Find a record-based flow](flows-tb.md#).

4.  Select the Additional actions \( ![Additional actions menu.](../image/ellipsisIcon.png)\) menu in the top-right corner of the flow that you want to delete, and then select **Copy** from the list of options.

5.  In the Create a copy of the flow window that appears, enter a name for the new flow that you want to create from the existing flow, and then select **Copy**.

6.  Edit your new flow by using Workflow Studio.

    For detailed information on how to work with flows for your application, see [Create a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md).

7.  Select **Save**.

    **Note:** To return to the list of flows after editing a flow, select the Additional actions \( ![Additional actions menu.](../image/ellipsisIcon.png)\) menu to the right of the **Flows** tab, and then select **All flows**.


