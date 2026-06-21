---
title: Combined Change Management release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Change Management from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-changemanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Change Management release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Change Management from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Change Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Change Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Change Management.

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

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=installed-with-cm-itsm-roles&family=yokohama&ft:locale=en-US)**

With the sn\_service\_desk\_agent user role, increase operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

The sn\_service\_desk\_agent role includes the following roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
Additionally, with the installation of the **ITSM Gen AI** \(**com.sn.itsm.gen.ai**\) plugin, the knowledge\_user and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

The sn\_service\_desk\_agent user role can be used starting with Service Operations Workspace version 6.1.

-   **[Change model Type field](https://www.servicenow.com/docs/access?context=t_CreateAChange&family=yokohama&ft:locale=en-US)**

A new **Model** option has been added to the change model Type field to help users identify a change that is controlled by a change model. **Model** is the default if a Type has not been set for the change request of a certain change model.

-   **[No default Risk value for change requests](https://www.servicenow.com/docs/access?context=t_CreateAChange&family=yokohama&ft:locale=en-US)**

There is no longer a default value for the Risk field on the Change Request table. The Risk value is set to **-- None --** until the risk is evaluated for the change request. This change ensures that no risk value is pre-assigned, allowing for a more accurate assessment before advancing the change

-   **[Mandatory field transition condition](https://www.servicenow.com/docs/access?context=create-a-change-model&family=yokohama&ft:locale=en-US)**

Ensure mandatory fields are completed before advancing through states for a change request, as defined by the Change Model. This feature enables change managers to mandate the completion of required fields before states can progress according to the Change Model.

-   **[Deny-unless ACLs on core tables](https://www.servicenow.com/docs/access?context=features-itsm-enhanced-security-change&family=yokohama&ft:locale=en-US)**

Prevent unauthorized access to change\_request and change\_task tables using deny-unless ACLs. The deny-unless ACLs restrict access on these tables for a non-authenticated user to perform actions such as read, write, delete, or create.

This feature is available for new or zBoot customers with the installation of the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin. Existing or upgrade customers must test and evaluate in their sub production instance before installing the plugin and implementing the security change in their production instance.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Change Management features.

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Change Management features or functionality were removed.

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

Change Management workflows have been removed and replaced by flows for new customers. Existing customers that use these workflows are unaffected. The flows are available to both new and existing customers. You can use ServiceNow® Workflow Studio to customize or extend these flows. For more information, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Change Management features or functionality were deprecated.

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

 See [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

