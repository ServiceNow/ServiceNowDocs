---
title: Combined Service Portfolio Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Service Portfolio Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-serviceportfoliomanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Service Portfolio Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Service Portfolio Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Portfolio Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Portfolio Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Service Portfolio Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Set the time zone for availability results in Service Portfolio Management](https://www.servicenow.com/docs/access?context=spm2-set-timezone&family=xanadu&ft:locale=en-US)**

Set the availability system property \[com.snc.availability.v2\] to true so you can set the time zone that you want to calculate availability results. The Availability calculations settings page provides you with the choice to calculate availability using the service offering commitment time zone \(yes or no\). It also provides you with the option to set the global availability time zone by selecting a time zone from a provided list. After you select **Yes** to calculate availability with the commitment time zone, the **Time zone** field on the commitment record is used to calculate the availability results. The **Time zone** field on the availability record is read only. After you opt to set the global time zone, all the availability results will use the time zone that you set as global.

**Note:** The underlying system properties that govern the global time zone and the commitment time zone are exclusive. You can set the global time zone or set the time zone to reflect a service offering commitment but you can't set both at the same time.

-   **[Assign multiple teams to support a service offering in Service Portfolio Management](https://www.servicenow.com/docs/access?context=spm2-assign-teams&family=xanadu&ft:locale=en-US)**

Use the added Teams related list in service offerings to assign different group types to support a service offering. The related list functionality is an existing platform feature that was added to the Service Portfolio Management application so you can see the related support teams in the Digital Portfolio Management view. For more information on the platform feature, see [Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&family=xanadu&ft:locale=en-US).


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Edit and manage service portfolios in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-edit-manage-portfolios&family=yokohama&ft:locale=en-US)**

Use the updated options to edit and manage your service portfolios:

    -   [Manage the CSDM life cycle fields in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-lifecycle-fields&family=yokohama&ft:locale=en-US)
    -   [Remap service portfolio taxonomy nodes in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-remap-taxo-nodes&family=yokohama&ft:locale=en-US)
-   **[Use Service Portfolio Management services](https://www.servicenow.com/docs/access?context=SPM2-services&family=yokohama&ft:locale=en-US)**

Recognize the updated label for technical services. The updated label aligns with the CSDM, version 5.0. Even though the table name hasn't changed, the services label is updated in the Service Portfolio Management application and in all ServiceNow applications or workspace environments that display services. The label for service offerings remains the same for all releases: Service offering in the \[service\_offering\] table.

    |Table name|Label in Xanadu and prior releases|Label in Yokohama and later releases|
    |----------|----------------------------------|------------------------------------|
    |\[cmdb\_ci\_service\_technical\]|Technical Service|Technology Management Service|


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Service Portfolio Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Service Portfolio Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Service Portfolio Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Service Portfolio Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The Service Portfolio Management Core plugin \[com.snc.service\_portfolio\_core\] is available by default for IT Service Management licensed customers. For more information, see [Activate Service Portfolio Management](https://www.servicenow.com/docs/access?context=activate-SPM2-plugin&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

The Service Portfolio Management Core plugin \[com.snc.service\_portfolio\_core\] is available by default for IT Service Management licensed customers. For more information, see [Activate](https://www.servicenow.com/docs/access?context=activate-SPM2-plugin&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

The Service Portfolio Management Core plugin \[com.snc.service\_portfolio\_core\] is available by default for IT Service Management licensed customers. For more information, see [Activate](https://www.servicenow.com/docs/access?context=activate-SPM2-plugin&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Service Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Service Portfolio Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Service Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Updated the availability system property \[com.sn.availability.v2\] so you can set the time zone for service availability records.
    -   Added the ability to change the global time zone for all availability results to reflect that time zone.
    -   Added the ability to set the time zone for availability results to reflect a service offering commitment.
    -   Updated the availability recalculations to reflect the time zone that you set.
    -   Added a read-only time zone field on service availability records.
-   Added a **Teams** related link tab to the service offering records so you can assign more than one team to support a service offering \(one-to-many relationship\).

 See [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Use the added options to edit and manage your service portfolios.
    -   Add life cycle fields to the taxonomy node records of your portfolios to align with the Common Service Data Model \(CSDM\).
    -   Added more flexibility to remap taxonomy nodes. You can move an entire branch of a taxonomy from one portfolio to another, including the automatic move of its child nodes.
    -   Reparent taxonomy nodes when you move them to a new location in a portfolio. You can also add a new taxonomy node in the middle of an existing portfolio, either between two nodes or between a node and a service.
-   Recognize the updated label for technical services.

 See [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Edit your service portfolios to comply with the new Digital Operational Resilience Act \(DORA\) standards:
    -   The Service portfolio record view includes the following key fields that are important for DORA compliance: **Managed by**, **Department**, and **Company** fields.
    -   Select multiple contracts in the **Contracts** field.
-   Delete the service portfolio or taxonomy node from the Digital Portfolio Management \(DPM\) scope.

 See [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

