---
title: Configuring Outbound Intel Sharing Controls
description: Use this section to configure outbound sharing controls, which determine the entities enabled for intelligence sharing from TISC to external systems.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Outbound Intel Sharing Controls

Use this section to configure outbound sharing controls, which determine the entities enabled for intelligence sharing from TISC to external systems.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Outbound Intel Sharing**.

2.  Select **Outbound Intel Sharing Controls**.

    Outbound Intel Sharing Controls is the default sharing control provisioned in the base system. By default, this control is set to the **Published** state.

    **Note:**

    -   These are the high-level sharing controls, which can later be used within intelligence sharing templates.
    -   Every action performed on the outbound sharing controls is recorded, and a work note is posted in the activity stream for each entity that is created, modified, or deleted.
3.  **Editing Sharing Controls:**
4.  Select **Edit** to modify the required fields if you want to change the default sharing control record.

    Whenever you edit the sharing control record, a validation message is displayed indicating you to disable all templates and confirm that there are no pending outbound intelligence sharing records before proceeding.

    If the above validations are successful, then another warning message is displayed indicating that any automation flows based on these settings can fail if you proceed without disabling them first.

    **Warning:** Editing these settings without first disabling the associated automation flows may cause errors. Do you want to proceed?

    If you acknowledge this risk and want to proceed, you can modify the sharing control.

5.  **Managing Entity-Level Sharing Controls:**
6.  Go to **Sharing Controls** section to view all the sharing controls available for the entities.

    By default all threat intelligence library entities present in the application including the observables, indicator, and objects are included.

7.  Select any entity to view its required and optional attributes.

    The **Edit Entity and Attributes** dialogue box is displayed.

8.  **Adding or Removing Entities:**
9.  Select **Remove Entity** if you want to remove any entity.

    This action **Remove Entity** removes the entity and automatically excludes it from outbound intelligence sharing. Once removed, the entity can’t be used for sharing within TISC and removal automatically removes the entity from all the templates, which has this entity as part of the sharing controls.

    Additionally, select **Remove all attributes** \(Trash icon available at the bottom of the dialog box\) to remove all the optional attributes. Removing any of these attributes directly impacts the corresponding intelligence sharing templates.

    **Note:**

    -   If there are any outbound sharing templates, which includes the selected entity then a warning message is displayed on the **Edit Entity and Attributes** dialog box indicating that removing the selected entity or any of its attributes automatically excludes them from the \{\#total number of templates\} outbound intelligence sharing templates they’re currently included in. The affected templates are listed on the **Edit Entity and Attributes** dialog box itself.
    -   A list of affected templates, for example: IOC Sharing Template is displayed for your review.
    -   If there are certain entities you don’t want to share with external systems, you can remove them from the sharing controls.
    -   Only the entities configured within the sharing controls will be available for selection when creating or modifying intelligence outbound sharing templates.
10. Select **Add all optional attributes** to include all the optional attributes of the selected entity in the outbound intelligence sharing.

11. After you make the necessary changes to the sharing controls, then select **Publish** to publish the sharing controls.

    Once the sharing controls are published, they are available for use within intelligence outbound sharing templates. For more information, see [Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md).


## What to do next

Refer to the following sections for guidance on external intelligence sharing using both the GUI and automated procedures.

-   [Sharing of Outbound Intelligence Records from GUI](../concept/tisc-create-intel-records-lib.md)
-   [Automated sharing of high-risk IOC's with trusted partners](tisc-automated-sharing-flow.md)[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

**Parent Topic:**[Exploring Outbound Intel Sharing](../concept/tisc-outbound-intel-sharing.md)

**Related topics**  


[Configuring Outbound Intel Data Exclusion Rule](tisc-outbound-data-exclusion.md)

[Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md)

[Configuring Outbound Intel Sharing Groups](tisc-config-inbound-sharing-groups.md)

[Defining Approval Rule for Outbound Intel](tisc-approval-outbound-intel.md)

[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

[Working on the Redaction Library](tisc-redaction-library.md)

