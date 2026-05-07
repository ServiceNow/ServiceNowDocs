---
title: Configuring Outbound Intel Sharing Templates
description: Outbound Intel Sharing Templates enable you to define and control the data shared externally from the Threat Intelligence Security Center \(TISC\).
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Outbound Intel Sharing Templates

Outbound Intel Sharing Templates enable you to define and control the data shared externally from the Threat Intelligence Security Center \(TISC\).

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

The primary purpose of the sharing templates is to prefill the sharing record details such as sharing record name, description, outbound intelligence profile or groups. For more information, see [Sharing of Outbound Intelligence Records from GUI](../concept/tisc-create-intel-records-lib.md).

These templates specify which entities and attributes are included and the system settings for sharing.

By configuring these templates, organizations can confirm that only relevant and approved intelligence data is shared by maintaining the security and compliance across internal and external collaboration efforts.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Administration** icon on the workspace.

3.  Go to **Outbound Intel Sharing**.

4.  Select **Outbound Intel Sharing Templates**.

5.  Select **New**.

6.  On the form, fill in the fields.

<table id="table_hzv_h12_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template Name

</td><td>

Name of the outbound intelligence sharing template.

</td></tr><tr><td>

Template Description

</td><td>

Description of the outbound intelligence sharing template.

</td></tr><tr><td>

Usage Mode

</td><td>

Indicates how a sharing template is intended to be used.Templates in the Outbound Intelligence Sharing module are versatile and can be applied across multiple sharing scenarios, based on the requirements.

The available sharing options are:

1.  **On-Demand Sharing**: Used for sharing data from GUI.
2.  **Automated Sharing**: Enables scheduled or trigger-based sharing through automation flows.
3.  **Both On-Demand Sharing and Automated Sharing**: Allows the template to be used in either On-Demand or Automated sharing, offering maximum flexibility.
4.  **Automated addition to TAXII Collections**: Automatically adds shared data to TAXII collections for distribution to trusted external partners.
5.  **On-Demand Addition to TAXII Collection**: Allows you to manually add on-demand TAXII collection for distribution to trusted external partners.


</td></tr><tr><td>

Enable Redaction \(Applicable only for automated modes\)

</td><td>

Select this check box to enable **Redaction**, which is the process of replacing sensitive information from shared data to protect confidentiality during intelligence sharing.**Note:** This option applies to **Automated Sharing**, **Automated addition to TAXII Collections**, and **On-Demand addition to TAXII Collections** and does not apply to **On-Demand Sharing**.

</td></tr><tr><td colspan="2">

**Access Controls for On-Demand Sharing**

</td></tr><tr><td colspan="2">

**Important:**

Since these templates are used within a managed sharing model such as when sharing the intelligence for specific objects or observables, you may want to control which users or groups can access them.

To manage this, there’s a dedicated section called **Allow access to all users or groups with outbound intelligence sharing permissions** where you can specify the users and groups that should have visibility to a particular template.

You can restrict access by specifying the individual users or groups, verifying that only the selected users or groups can use the template.

</td></tr><tr><td>

Allow access to all users or groups with outbound intel sharing permissions

</td><td>

Select this check box to grant access to all users or groups that have Outbound Intel Sharing permissions.

</td></tr><tr><td>

Users \(should have 'sn\_sec\_tisc.int\_exch\_write' role\)

</td><td>

Select the users for accessing templates for sharing intelligence.You must have the `sn_sec_tisc.int_exch_write` role to perform outbound intelligence sharing.

**Note:** : These roles are applicable only for On-Demand Sharing.

</td></tr><tr><td>

Groups \(should have 'sn\_sec\_tisc.int\_exch\_write' role\)

</td><td>

Select the groups for accessing templates for sharing intelligence.Groups must have the `sn_sec_tisc.int_exch_write` role to perform outbound intelligence sharing.

**Note:** These roles are applicable only for On-Demand Sharing.

</td></tr><tr><td colspan="2">

**Prefilled Inputs**

</td></tr><tr><td>

Name \(Sharing Record Name\)

</td><td>

Name of the sharing record.This value is pre-populated within the outbound intelligence sharing record.

</td></tr><tr><td>

Description \(Sharing Record Description\)

</td><td>

Description of the sharing record.This value is pre-populated within the outbound intelligence sharing record.

</td></tr><tr><td>

Outbound Intel Sharing Profiles

</td><td>

Indicates the Outbound Intel Sharing Profiles. This value is pre-populated within the outbound intelligence sharing record.For more information, see [Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md).

</td></tr><tr><td>

Outbound Intel Sharing Groups

</td><td>

Indicates the Outbound Intel Sharing Groups. This value is pre-populated within the outbound intelligence sharing record.For more information, see [Configuring Outbound Intel Sharing Groups](tisc-config-inbound-sharing-groups.md).

</td></tr><tr><td>

TAXII Collections

</td><td>

Indicates the TAXII collections. This option is only visible only when you select the Usage mode as **Automated addition to TAXII Collections** or **On-Demand Addition to TAXII Collection**.

</td></tr><tr><td>

Default Confidence \(0 - 100\)

</td><td>

Indicates the default confidence value, which is applied only if the intelligence records within the sharing record don’t specify a confidence value.This value is pre-populated within the outbound intelligence sharing record.

</td></tr><tr><td>

Override TLP

</td><td>

Select this check box to override the TLP \(Traffic Light Protocol\) by applying a specific TLP to all the records within the sharing control. This TLP is used during payload generation, overriding the TLP assigned at the individual record level.

This value is pre-populated within the outbound intelligence sharing record.

</td></tr><tr><td>

TLP

</td><td>

Indicates the Traffic Light Protocol \(TLP\) of the sharing template. This option is visible only when you select the **Override TLP** check box.

</td></tr><tr><td colspan="2">

**System Settings for Sharing**

</td></tr><tr><td>

Outbound Intelligence Sharing Controls

</td><td>

Indicates the Outbound Intelligence Sharing Controls. By default the value in this field is **Outbound Intel Sharing Controls** as this is the only sharing control that is provisioned within the base system.

</td></tr><tr><td>

Outbound Intelligence Exclusion Rules

</td><td>

Indicates the Outbound Intelligence Exclusion Rules. By default the value in this field is **Outbound Data Exclusion Rule** as this is the only exclusion rule that is provisioned within the base system.

</td></tr></tbody>
</table>7.  Select **Save** to save the sharing template.

    A confirmation message is displayed indicating that all the outbound intelligence sharing controls will be automatically copied into this template and will be visible in the **Template Sharing Controls** section within a few seconds.

8.  **Template Sharing Controls:**
9.  Navigate to **Template Sharing Controls** section.

    Template Sharing Controls displays all the sharing controls defined for the selected template, and these sharing controls. These are dependent on the main sharing controls known as outbound intelligence sharing controls. For more information, see [Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md).

10. Select **Add** inside the **Template Sharing Controls** section.

    The Add Entities and Attributes dialog box is displayed.

    You’ll only see those entities that are defined in the main sharing controls. By default, all the entities are included and provisioned within the base system, so you’ll see all the sharing controls initially. However, if you remove an entity from the main sharing control, then that entity will no longer be available for selection within the template’s sharing controls.

    **Important:** These templates are also used within STIX, therefore the validation rules are introduced for STIX. Violating these rules may result in the payload generation failure. If the defined STIX compliance rules aren’t met, the payload may not be sent to the configured endpoint, and the sharing process could be stopped entirely.

    An error message is displayed indicating a STIX validation warning: You must include at least one of the required attributes for this entity.

11. Select **Add all optional attributes** to include the optional attributes in the sharing templates.

12. Additionally, click **Remove all attributes** \(Trash icon available at the bottom of the dialog box\) to remove the optional attributes or select **Remove Entity** button inside the **Edit Entity and Attributes** dialog box to completely remove the entity from the template.

13. After you make the necessary changes to the sharing control then click **Publish** to publish the template sharing controls.

    Once the template sharing controls are published, they become available for use within intelligence outbound sharing templates.

    **Important:** These templates are also applicable during sharing data from GUI setup and can be accessed from the Threat Intelligence Library. For more information, see [Sharing of Outbound Intelligence Records from GUI](../concept/tisc-create-intel-records-lib.md).

14. Select **Edit** button to make any necessary changes to the template.

    **Note:** If you are making changes to the template then a warning message is displayed indicating that there are pending outbound intelligence sharing records that are dependent on the sharing template. Make ensure that there are no pending outbound intelligence share records before editing this template.

    While you edit the sharing template, a confirmation message is displayed indicating that editing this template without first disabling the dependent automation flows may result in errors and do you still want to continue. If you wish to proceed then select **Edit** button to make the changes.

15. Additionally, select **Duplicate** button if you want to create a duplicate of the template, then you clone the current template.

    This action replicates the entire configuration including all the associated sharing controls.

16. **Validation to enable the sharing template:**

    The application checks for various validations before enabling the outbound intelligence sharing templates and are enabled when all the required configurations are complete.

    1.  **Missing Sharing Controls**: If no sharing controls have been added to the template and if the user attempts to publish, the application allows the template to be saved and published but not enabled.

        A validation message appears, helping to prevent the template from being actively used.

    2.  **Draft Sharing Controls at the Main Level**: If the main Outbound Intel Sharing Controls are still in **edit \(draft\) mode**, then the template can’t be enabled. In this case, a warning message is displayed indicating that the sharing controls are in draft status and must be published before proceeding.

        These validations are enforced to confirm that templates are only activated for sharing when all related components are in a **published** and enabled state. This helps prevent incomplete or invalid configurations from being used in operational sharing processes.

    **Note:**

    -   When you select **Publish** and if any of the mentioned criteria is not met then the template will still be published but not enabled.
    -   When you select **Enable** and if any of the mentioned criteria is not met then the template will not be enabled.
    -   **Enable** and **Disable** buttons will only be shown for published templates.
17. Select **Disable** from the **Outbound Intel Sharing Templates** page directly if you want to disable any sharing template.

    **Note:** On the **Outbound Intel Sharing Templates** page list view, you can also perform various actions such as **Duplicate**, **Enable**, or **Disable** by selecting one or more templates.


**Parent Topic:**[Exploring Outbound Intel Sharing](../concept/tisc-outbound-intel-sharing.md)

**Related topics**  


[Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md)

[Configuring Outbound Intel Data Exclusion Rule](tisc-outbound-data-exclusion.md)

[Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md)

[Configuring Outbound Intel Sharing Groups](tisc-config-inbound-sharing-groups.md)

[Defining Approval Rule for Outbound Intel](tisc-approval-outbound-intel.md)

[Working on the Redaction Library](tisc-redaction-library.md)

[Sharing of Outbound Intelligence Records from GUI](../concept/tisc-create-intel-records-lib.md)

[Automated Sharing of Outbound Intelligence Records](../concept/tisc-automated-outbound-intel-share.md)

[Automated Sharing of TAXII Collections](tisc-automated-share-taxii.md)

