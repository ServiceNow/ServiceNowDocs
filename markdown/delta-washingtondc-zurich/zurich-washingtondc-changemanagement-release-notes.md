---
title: Combined Change Management release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Change Management from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-changemanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Change Management release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Change Management from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Change Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Change Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

As part of the update to use Flow instead of Progress Workers for conflict detection, the Conflict Checker Progress UI Formatter record references a new UI macro, change\_conflict\_worker\_progress\_gate. This macro checks the **change.conflict.useprogressworker** system property to determine the conflict detection mechanism and then displays the corresponding UI macro to work with either Progress Workers or the Change Management Worker table. For more information, see [Conflict detection](https://servicenow-staging.fluidtopics.net/access?context=c_ConflictDetection&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Change Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[User role for service desk agents](https://servicenow-staging.fluidtopics.net/access?context=installed-with-cm-itsm-roles&family=yokohama&ft:locale=en-US)**

With the sn\_service\_desk\_agent user role, increase operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

The sn\_service\_desk\_agent role includes the following roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
Additionally, with the installation of the **ITSM Gen AI** \(**com.sn.itsm.gen.ai**\) plugin, the knowledge\_user and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

The sn\_service\_desk\_agent user role can be used starting with Service Operations Workspace version 6.1.

-   **[Change model Type field](https://servicenow-staging.fluidtopics.net/access?context=t_CreateAChange&family=yokohama&ft:locale=en-US)**

A new **Model** option has been added to the change model Type field to help users identify a change that is controlled by a change model. **Model** is the default if a Type has not been set for the change request of a certain change model.

-   **[No default Risk value for change requests](https://servicenow-staging.fluidtopics.net/access?context=t_CreateAChange&family=yokohama&ft:locale=en-US)**

There is no longer a default value for the Risk field on the Change Request table. The Risk value is set to **-- None --** until the risk is evaluated for the change request. This change ensures that no risk value is pre-assigned, allowing for a more accurate assessment before advancing the change

-   **[Mandatory field transition condition](https://servicenow-staging.fluidtopics.net/access?context=create-a-change-model&family=yokohama&ft:locale=en-US)**

Ensure mandatory fields are completed before advancing through states for a change request, as defined by the Change Model. This feature enables change managers to mandate the completion of required fields before states can progress according to the Change Model.

-   **[Deny-unless ACLs on core tables](https://servicenow-staging.fluidtopics.net/access?context=features-itsm-enhanced-security-change&family=yokohama&ft:locale=en-US)**

Prevent unauthorized access to change\_request and change\_task tables using deny-unless ACLs. The deny-unless ACLs restrict access on these tables for a non-authenticated user to perform actions such as read, write, delete, or create.

This feature is available for new or zBoot customers with the installation of the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin. Existing or upgrade customers must test and evaluate in their sub production instance before installing the plugin and implementing the security change in their production instance.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Control opening of CAB meetings](https://servicenow-staging.fluidtopics.net/access?context=attend-cab-meeting-using-cab-workbench&family=zurich&ft:locale=en-US)**

Control the opening of a CAB meeting from the CAB Meeting calendar in the CAB Meeting workbench in Service Operations Workspace or in the Core UI through the **sn\_change\_cab.com.snc.change\_management.cab.use\_sow\_meeting** system property. For more information, see [Change Management properties](https://servicenow-staging.fluidtopics.net/access?context=r_ChangeManagementProperties&family=zurich&ft:locale=en-US).

-   **[Track conflict detection](https://servicenow-staging.fluidtopics.net/access?context=c_ConflictDetection&family=zurich&ft:locale=en-US)**

Track the progress of conflict detection using the Change - Conflict Detection flow \(that runs as a system user\) and the Change Management Worker table instead of Progress Workers. You can choose between the Flow and Progress Worker options by updating the **change.conflict.useprogressworker** system property.

A new UI formatter **change\_conflict\_worker\_progress\_gate.xml** has been introduced to the change request form to replace the existing **change\_request\_conflict\_progress.xml**. This update supports the **change.conflict.useprogressworker** system property when you upgrade to Zurich. The new formatter displays the same Conflict tab but selects the macro version to render the form according to the value of the new system property.

-   **[Define the maximum records for conflict detection](https://servicenow-staging.fluidtopics.net/access?context=configure-conflict-properties&family=zurich&ft:locale=en-US)**

Limit the maximum number of conflict records that can be generated for each conflict type when conflict detection runs through the **change.conflict.max\_count** system property; create this system property if it is not already present.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Change Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Propose a standard change template in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=propose-standard-change-sow&family=zurich&ft:locale=en-US)**

As a user with the itil role, you can create a standard change template proposal in Service Operations Workspace.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Change Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Change Management workflows have been removed and replaced by flows for new customers. Existing customers that use these workflows are unaffected. The flows are available to both new and existing customers. You can use ServiceNow® Workflow Studio to customize or extend these flows. For more information, see [Flow Designer](https://servicenow-staging.fluidtopics.net/access?context=flow-designer&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Change Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Change Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Change Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Change Management is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Change Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   Increase operational efficiency of tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Require specified field details to be updated before transitioning the state of a change request by converting existing optional fields to mandatory fields.
-   Restrict unauthorized access to Change Management tables using deny ACLs.

 See [Change Management](https://servicenow-staging.fluidtopics.net/access?context=c_ITILChangeManagement&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Review and authorize change requests and review recently implemented changes in the Change Advisory Board Workbench in the Service Operations Workspace \(SOW\).
-   Track conflict detection using the Change - Conflict Detection flow and the Change Management Worker table instead of Progress Workers.
-   Limit the number of conflict records for each conflict type through the **change.conflict.max\_count** system property.
-   Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.


 See [Change Management](https://servicenow-staging.fluidtopics.net/access?context=c_ITILChangeManagement&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

