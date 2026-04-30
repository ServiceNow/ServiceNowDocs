---
title: Configuring lookup rules
description: By configuring lookup rules, you can map security exposure data to the correct configuration items \(CIs\) in the CMDB. This mapping is a critical function because associating exposure findings with the right assets is essential for proper risk assessment, assignment, and remediation workflows.Create lookup rules to automatically and accurately associate incoming exposure findings data with the correct configuration items \(CIs\) in the Configuration Management Database \(CMDB\) This is essential for enabling the rest of the vulnerability management process to function correctly.To ignore some configuration item \(CI\) classes, for example Load Balancer \[cmdb\_ci\_lb\], when running CI Lookup Rules, set the ignoreCIClass \[sn\_sec\_cmn.ignoreCIClass\] system property.Reapply the lookup rules on selected discovered items from the discovered item list view select actions. If the configuration item \(CI\) changes after you reapply the rules, the discovered items are updated with the new CI and impacted detections. Vulnerable items are also updated.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring lookup rules

By configuring lookup rules, you can map security exposure data to the correct configuration items \(CIs\) in the CMDB. This mapping is a critical function because associating exposure findings with the right assets is essential for proper risk assessment, assignment, and remediation workflows.

**Related topics**  


[Associating finding with a configuration item using lookup rules](sem-associate-finding-configuration-item-using-lookup-rules.md)

## Create lookup rule

Create lookup rules to automatically and accurately associate incoming exposure findings data with the correct configuration items \(CIs\) in the Configuration Management Database \(CMDB\) This is essential for enabling the rest of the vulnerability management process to function correctly.

### Before you begin

Role required: sn\_vul.vulnerability\_admin

### About this task

Creating lookup rules requires advanced ServiceNow and Unified Security Exposure Management \(USEM\) expertise. Rather than modifying one of the existing lookup rules, consider copying it and modifying the copy. When you are satisfied that the new rule does what you want, deactivate the original.

**Note:** Rules, once removed, cannot be recovered. Rather than removing existing rules, deactivate them when creating new ones.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Look-up rules** tile.

4.  On the Rules page, select **Look-up** in the navigation pane.

5.  Select **New**.

6.  On the form, fill in the fields.

<table id="table_t4d_4bd_5t"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Details

</td></tr><tr><td>

Name

</td><td>

Name of the rule.

</td></tr><tr><td>

Lookup method

</td><td>

Method used for matching. Choices are:-   **Script**: Pre-built \(IP address, DNS name, and so on\) or custom script.
-   **Field matching**: Search on table or field in the CMDB.


</td></tr><tr><td>

Type

</td><td>

Type used with the Script **Lookup method**.

</td></tr><tr><td>

Order

</td><td>

Order of precedence for the rule. Rules with the lowest order are evaluated first.

</td></tr><tr><td>

Active

</td><td>

Check box for whether the rule is active or disabled.

</td></tr><tr><td>

Source

</td><td>

Source used as input to this rule.

</td></tr><tr><td>

Source field

</td><td>

Source field used as input to this rule. Select any field, but it is treated as a string value.

</td></tr><tr><td>

Description

</td><td>

Description of the new look-up rule.

</td></tr><tr><td>

Lookup target

</td><td>

Lookup approach you want to follow. Select from: -   Configuration item
-   Product model


</td></tr><tr><td colspan="2">

If condition is met

</td></tr><tr><td>

Condition

</td><td>

Condition based on which the lookup rule is applied. This condition depends on the attribute from the third-party scanner.**Note:** The asset attribute is a part of the payload. It is received from the third-party scanner. See the Discovered Items table for payload examples.

</td></tr><tr><td colspan="2">

Then set this value

</td></tr><tr><td>

Lookup method

</td><td>

Method used for matching. Choices are: -   Script: Pre-built \(IP address, DNS name, and so on\) or custom script.
-   Field matching: Search on table or field in the CMDB.


</td></tr><tr><td>

Search on CI table

</td><td>

Table to search within the CMDB. Used with field matching **Lookup Method**.

</td></tr><tr><td>

Search on product table

</td><td>

If you choose the Product model Lookup target, the default value is Application Model.

</td></tr><tr><td>

Search on CI field

</td><td>

Field that contains information that can be used to locate a CI. Used with the field matching **Lookup method**. This field may be on the CI record, or on a related record, such as a network adapter.

</td></tr><tr><td>

Search on product model field

</td><td>

If you choose the Product model Lookup target, the default value is Name.

</td></tr><tr><td>

Type

</td><td>

Type used with the Script Lookup method.

</td></tr><tr><td>

Script

</td><td>

Editable sample script, based on the **Type**, is shown. Implement the custom script following the comments included in the template of the default function.**Note:**

The process function has three parameters: **rule**, **sourceValue**, and **sourcePayload**

</td></tr></tbody>
</table>7.  Select **Save**.

    For more implementation information for lookup rules see, [Steps to help prevent duplicate or orphaned records after running Vulnerability Response CI lookup rules](../../security-operations-common/concept/ci-identifier-rules-impl-test.md).

    ![CI lookup rule using a condition builder for version 12.0.](../../security-operations-common/image/CI-LookupRules-v12.png "Example of a CI lookup rule using a condition builder for V12.0")

    ![CI lookup rule using a script](../../security-operations-common/image/CI-LookupRules.png "Example of a CI lookup rule using a script prior to V12.0")


**Related topics**  


[Vulnerability Response vulnerable item form fields](../../vulnerability-response/reference/vulnerable-item-fields.md)

## Ignore CI classes

To ignore some configuration item \(CI\) classes, for example Load Balancer \[cmdb\_ci\_lb\], when running CI Lookup Rules, set the **ignoreCIClass** \[**sn\_sec\_cmn.ignoreCIClass**\] system property.

### Before you begin

Role required: admin

**Note:**

The **ignoreCIClass** system property is available starting with Vulnerability Response v9.0. However, the property functionality is not available upon upgrade from any previous version.

If you have upgraded from any Security Operations application, prior to version 9.0, see [KB0788209](https://support.servicenow.com/kb_view.do?sysparm_article=KB0788209) for instructions on how to enable this functionality.

### Procedure

1.  Enter `sys_properties.list` in the left navigation bar.

2.  Click **Enter**.

3.  In the **Search** menu, under **Name** enter `sn_sec_cmn.ignoreCIClass`.

4.  In the **Value** text box, enter the CI classes to exclude in a comma-separated list.

    ![ignoreCI Class system property example.](../../security-operations-common/image/ignoreCIClass.png)

5.  Click **Update**.

    This list is used by CI Lookup Rules during the next import. Vulnerable items created during import are not associated to a CI of any type listed in the **Value** field of the `sn_sec_cmn.ignoreCIClass` system property.


## Reapply lookup rules on selected discovered items

Reapply the lookup rules on selected discovered items from the discovered item list view select actions. If the configuration item \(CI\) changes after you reapply the rules, the discovered items are updated with the new CI and impacted detections. Vulnerable items are also updated.

### Before you begin

Roles required: admin

### About this task

For more information, see [CI changes for discovered items](../../vulnerability-response/concept/reapply-discovered-items-ci-changes.md).

For more information on the concepts of CI matching and the CMDB, discovered item lookup, rule-based identification, see the [CI matching in Vulnerability Response \[KB0998706\] article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0998706) in the HI Knowledge Base.

### Procedure

1.  Navigate to **All** &gt; **Security operations** &gt; **CMDB** &gt; **Discovered Items**.

2.  Select the required discovered items and select **Action on selected rows**.

    ![Reapply CI lookup rules on Discovered Items.](../../vulnerability-response/image/reapply-action-di.png)

3.  From the list, select **Reapply CI lookup rules**.

    **Note:** You can skip the reapplication of lookup rules on discovered items with the substate ‘CI Decommissioned’ by enabling the system property **sn\_sec\_cmn.skipItemsWithCIDecommissioned**.

    The rules are reapplied on these discovered items.

4.  Select **View status** in the message.

    The status displays on the background job form.

    **Note:** In the **Notes** field, the `Discovered items could not be process due to exception` attribute with a non-zero value indicates that there’s an error or exception while reapplying a look-up rule. Check the system logs for more details.

5.  Reapply only applies to items scanned within the last 90 days based on the **last\_scan\_date, last\_comp\_scan\_date, non\_infra\_last\_scan\_date, non\_infra\_last\_comp\_scan\_date** column.

    Added ci\_lifecycle\_status\_source \(scope = sn\_sec\_cmn\) system property for configuring CI lifecycle status columns \(for example, Install Status, Operational Status\). You can configure additional columns for retiring CIs.

    Columns are added to the background job list view:

    -   Elapsed Time\(ms\): The time required for processing the background job.
    -   Items Processed: The number of items processed until now.
    -   Total Items to be Processed: The total number of items remaining to be processed.
    -   Time Until Completion\(ms\): The time remaining until the background job is processed. These columns provide visibility into job progress. These columns are available for each form view for you to add according to requirement.

