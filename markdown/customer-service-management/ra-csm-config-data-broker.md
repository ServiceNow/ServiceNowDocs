---
title: Configure force refresh for recommendations
description: Configure the Trigger Recommendation Refresh data broker to refresh and update the recommendations based on the results from UI events for precise recommendations. Similarly, use the ForceRefreshRecommendations method for configuring an explicit refresh mechanism.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configure force refresh for recommendations

Configure the **Trigger Recommendation Refresh** data broker to refresh and update the recommendations based on the results from UI events for precise recommendations. Similarly, use the `ForceRefreshRecommendations` method for configuring an explicit refresh mechanism.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, or admin

## About this task

Prior to the Zurich family release, the recommendations often remain outdated due to refresh triggers being tied only to updates on primary context records. Starting with the Zurich family release, you can configure explicit and event-driven refreshes for various context updates beyond just the primary context table to improve recommendations relevance.

-   Explicit refresh mechanism: Enables you to trigger recommendation refreshes manually, independent of internal context changes, addressing scenarios where event-driven updates are insufficient.

    Call the `ForceRefreshRecommendations` method. The `ForceRefreshRecommendations` method is shipped with the base system as part of the **NextBestActionServiceImpl** script include.

    `ForceRefreshRecommendations` method:

    ```
    sn_nb_action.NextBestActionService().forceRefreshRecommendations(input.ruleContextSysIds, input.currentRecordSysId, input.refreshAllUsers);
    ```

-   Event-driven refresh: Implements automatic recommendations updates triggered by predefined system events such as attribute changes on related tables or user interactions like button clicks or tab navigation.

    Configure the **Trigger Recommendation Refresh** data broker of a UI component in the UI builder. This data broker is shipped with the base system and is available for all the UI components of the record pages. Perform the following steps to configure this data broker.


## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI builder**.

2.  In the UI builder, open the **Workspace** experience which you want update.

3.  Open the record page containing the UI component for which you want to configure the data broker.

4.  In the content tree, select a UI component.

    A panel opens on the right with Configure, Style and Events tabs.

5.  In the Events tab, select **Execute Data Resource - Trigger Recommendation Refresh 1**.

6.  On the Configure modal, set the following properties.

<table id="table_z4v_sh3_yfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule Context SysIds

</td><td>

Sysid of the rule context records that must be applied to the UI component. The recommendations of these rules are reflected in the recommendations tab when the event is triggered. This property is of String array type.

</td></tr><tr><td>

Current Record SysId

</td><td>

Sysid of the record to which you want to associate the UI event.This property is of String type.

</td></tr><tr><td>

Refresh All Users

</td><td>

Refreshes recommendations for all the active agent, when set to true. By default, the value is set to false.This property is of Boolean type.

</td></tr></tbody>
</table>7.  In the **When to trigger** drop-down, select one of the following.

<table id="choicetable_eqc_b33_yfc"><thead><tr><th align="left" id="d79777e231">

Option

</th><th align="left" id="d79777e234">

Description

</th></tr></thead><tbody><tr><td id="d79777e240">

**Always**

</td><td>

Triggers the refresh every time there’s an update.

</td></tr><tr><td id="d79777e249">

**Conditional**

</td><td>

Triggers the refresh when the defined condition is met.Define the condition in the **Event Handler condition** field.

</td></tr></tbody>
</table>8.  Select **Apply** in the Configure modal.


## Result

When the configured component is triggered, the recommendations are refreshed and updated accordingly in the CSM/FSM Configurable Workspace.

