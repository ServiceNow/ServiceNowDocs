---
title: Configure auto-fill inputs on input form screens
description: Streamline form completion on input form screens by configuring auto-filled inputs based on one or more user inputs. Auto-fill inputs are configured by using mobile client scripts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure auto-fill inputs on input form screens

Streamline form completion on input form screens by configuring auto-filled inputs based on one or more user inputs. Auto-fill inputs are configured by using mobile client scripts.

## Before you begin

Role required: admin

## About this task

Auto-fill inputs are configured by using mobile client scripts that run as a UI rule action in the UI rule of an input form screen. These scripts run in UI rules with an **OnChange** trigger type. For more information about UI rules and UI rule actions, see [Mobile UI Rules](../concept/mobile-ui-rules.md).

**Note:**

-   Auto-fill inputs are not supported in offline mode.
-   Only one **Run client script** UI rule action can be configured for each mobile UI rule.
-   Input form screens were formerly called parameter screens. However, the name **Parameter Screen** is still used in the Mobile UI Rule form.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile UI** &gt; **Mobile UI Rules**.

2.  In the Mobile UI Rules list, either select **New** to create a new mobile UI rule or select an existing mobile UI rule to configure it for auto-fill inputs.

    **Important:**

    If you select an existing mobile UI rule, make sure it has the following characteristics:

    -   **Parent Table** is set to **Parameter Screen**.
    -   At least one of the **Triggers** is **OnChange**.
3.  Configure a mobile UI rule for auto-fill inputs on input form screens by completing one of the following options.

    -   **If you selected __New__ in Step 2:**
        1.  In the Mobile UI Rule form, fill in the fields as follows:

<table id="table_krx_jvf_3bc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile UI rule.

</td></tr><tr><td>

Active

</td><td>

Whether the mobile UI rule is active.

</td></tr><tr><td>

Condition

</td><td>

Condition under which the mobile UI rule is used. If the **Condition** field is left empty, this UI rule runs whenever any input changes.

 For example, to trigger this UI rule when a particular input changes, use the **VALCHANGES** operator. Entering `urgencyVALCHANGES` in the **Condition** field causes the UI rule to be triggered only when the value of an input named **urgency** changes.

 For details on the operators available for your condition, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Parent Table

</td><td>

The parent table that the mobile UI rule applies to. Select **Parameter Screen**.

</td></tr><tr><td>

Parent

</td><td>

The input form screen to which your mobile UI rule is applied.

</td></tr><tr><td>

Triggers

</td><td>

Select **onChange**.

</td></tr><tr><td>

User Action Id

</td><td>

A unique value that identifies this action record. It's needed to associate the action with a UI rule.

**Important:** This option doesn't apply to configuring auto-fill inputs on input form screens. Don't set a value for this field.

</td></tr><tr><td>

Order

</td><td>

Order in which the mobile UI rule runs.

**Important:** This option doesn't apply to configuring auto-fill inputs on input form screens. Don't set a value for this field.

</td></tr><tr><td>

Reverse If False

</td><td>

When this field is selected, the mobile UI rule actions are reversed if the condition evaluates as false.

 **Important:** UI rule actions that use the **Run Client Script** operation can't run if the condition evaluates to **false**. Don't select this check box.

</td></tr></tbody>
</table>        2.  Select **Submit**.
    -   **If you selected an existing mobile UI rule to configure it for auto-fill inputs in Step 2:**
        1.  In the Mobile UI Rule form, fill in the fields as follows:

<table id="table_egk_dxf_3bc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Condition

</td><td>

Condition under which the mobile UI rule is used. If the **Condition** field is left empty, this UI rule runs whenever any input changes.

 For example, to trigger this UI rule when a particular input changes, use the **VALCHANGES** operator. Entering `urgencyVALCHANGES` in the **Condition** field causes the UI rule to be triggered only when the value of an input named **urgency** changes.

 For details on the operators available for your condition, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Parent Table

</td><td>

Make sure this field is set to **Parameter Screen**.

</td></tr><tr><td>

Triggers

</td><td>

Make sure that at least one of the **Triggers** is set to **onChange**.

</td></tr></tbody>
</table>        2.  Select and hold \(or right-click\) the banner and select **Save**.
4.  Navigate to the mobile UI rule that you configured in Step 3 to configure the mobile UI rule action for auto-fill inputs on your input form screen.

5.  In the Mobile UI Rule Actions section of the mobile UI rule form, select **New**.

    ![Mobile Rule UI Actions form](../image/autofill-input-form-screen-nu-act.png)

    The Mobile UI Rule Action form appears.

6.  In the Mobile UI Rule Action form **Operation** field, search for and select **Run Client Script**.

    ![Mobile UI Rule Action form with Run Client Script Operation called out](../image/autofil-inpt-frm-scrn-rn-clnt-scrpt.png)

7.  Write the client script in the **Client script** field.

    Client scripts use the m\_form object and the MobileScriptIncludeCaller class. For details on these JavaScript APIs, see [MobileScriptIncludeCaller - Client](https://www.servicenow.com/docs/access?context=MobileScriptInclCallerClientAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) and [m\_form - Client](https://www.servicenow.com/docs/access?context=m_formClientAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) in the API reference documentation.

    When writing the client script, be aware of the following points:

    -   Don't change the signature of the **onChange** function.
    -   The argument inputName is a string that is the name of the input whose value changed.
    -   The argument newValue contains the new value of that input after the change.
8.  Select **Submit**.


