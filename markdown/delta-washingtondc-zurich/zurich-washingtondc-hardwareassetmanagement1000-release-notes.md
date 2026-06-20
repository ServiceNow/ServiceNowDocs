---
title: Combined Hardware Asset Management 10.0.0 release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Hardware Asset Management 10.0.0 from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-hardwareassetmanagement1000-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Hardware Asset Management 10.0.0 release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Hardware Asset Management 10.0.0 from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Hardware Asset Management 10.0.0 release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Hardware Asset Management 10.0.0 to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

After your upgrade to Washington DC, keep in mind the following upgrade scenarios for the Total Cost of Ownership \(TCO\) of assets:

-   Upgrade works for all Hardware Asset Management flow tasks.
-   You must have task rate cards for each workflow task.
-   TCO upgrade populates an asset and expense category field on the expense line corresponding to each task.
-   Expense category is populated based on the expense lines and the source of the expense line.
-   You must populate the TCO benchmark cost and the TCO benchmark threshold field on all existing models manually or using the bulk import functionality.
-   TCO upgrade populates the following fields on assets:
    -   Asset end of useful life: Created date along with useful life in months.
    -   Asset first used date: Same as the created date.
    -   Asset TCO: Aggregated sum of all the expense lines related to the asset. For simple assets, Asset TCO is the aggregated sum of expense lines under it. For complex assets, Asset TCO is the aggregated sum of expense lines of the parent as well as its child assets.

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
</table>## New features

Between your current release family and Zurich, new features were introduced for Hardware Asset Management 10.0.0.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Measure the maturity of your Hardware Asset Management application through Success portal](https://servicenow-staging.fluidtopics.net/access?context=hard-suc-port&family=washingtondc&ft:locale=en-US)**

Measure the maturity and improve the value return of your Hardware Asset Management application within your organization through the Success portal view in Hardware Asset Workspace. You can visualize, identify, and report the capabilities or features you must focus on to use Hardware Asset Management efficiently.

-   **[Understand and analyze your total cost of ownership of assets](https://servicenow-staging.fluidtopics.net/access?context=asset-mgmt-tco&family=washingtondc&ft:locale=en-US)**

Manage resources efficiently by tracking the Total Cost of Ownership \(TCO\) of assets, where the total cost includes initial capital cost and operation cost.

-   **[Improved Hardware Asset Management \(HAM\) licensing method for custom model categories](https://servicenow-staging.fluidtopics.net/access?context=ham-licensing&family=washingtondc&ft:locale=en-US)**

Access Hardware Asset Management features and workflows by associating your custom model category with a parent model category that is linked to a licensable and opted-in Resource Category. The ITAM License Report shows all custom model categories associated with licensable and opted-in Resource categories. A custom model category that isn’t associated with a licensable parent model category can't access Hardware Asset Management workflows and features.

-   **[View and track the asset warranty details received from Lenovo](https://servicenow-staging.fluidtopics.net/access?context=view-asset-warranty-details&family=washingtondc&ft:locale=en-US)**

Manage your hardware assets based on the warranty information received from Lenovo. You can view the details of the warranties associated with a hardware asset directly on the asset form. You can also view all the warranties from a central location using the Asset operations view of the Hardware Asset Workspace. You can also track the hardware assets that are approaching the warranty expiration date and take necessary action.

-   **[Gain visibility into the TRM lifecycle phases of hardware products and manage unapproved products](https://servicenow-staging.fluidtopics.net/access?context=trm-for-tech-onboarding&family=washingtondc&ft:locale=en-US)**

Manage hardware products within your organization efficiently by using the TRM lifecycle phase details. With these details, you can understand if any hardware product used in your organization isn’t part of TRM or if it isn't approved to use.

-   **[Manage the operational assets of your organization with Product Instance](https://servicenow-staging.fluidtopics.net/access?context=product-instance-for-assets&family=washingtondc&ft:locale=en-US)**

Manage an asset throughout its lifecycles in the Hardware Asset Management application and workflows by representing the asset as a Product Instance, which is a logical grouping of operational asset, Configuration Item \(CI\), and Install Base Item \(IBI\) classes. A unique Product Instance Identifier \(PID\) links the pre-existing related asset, CI, and IBI classes. On the Product Instance, the status fields of Asset, CI, and IBI classes are synchronized.

-   **[License prioritization for Hardware Asset Management solutions](https://servicenow-staging.fluidtopics.net/access?context=licensing-ham-solutions&family=washingtondc&ft:locale=en-US)**

Manage your Hardware Asset Management subscriptions with the License prioritization feature within HAM licensing. While purchasing more than one Hardware Asset Management solution, any licensable and opted-in resource category is licensed only under one solution according to the priority defined in the HAM licensing framework. For example, the Server resource category is licensed only under Hardware Asset Management integration with Telecommunications Network Inventory even if the Hardware Asset Management application is activated explicitly on your ServiceNow instance. The ITAM License Report shows the details of resource categories counted under each Hardware Asset Management solution.

**Note:** The License prioritization feature is available with Hardware Asset Management version 10.1.0 and later.

-   **[New resource categories for Hardware Asset Management](https://servicenow-staging.fluidtopics.net/access?context=ham-licensing&family=washingtondc&ft:locale=en-US)**

Avail Hardware Asset Management features and workflows by opting in printers, monitors, storage devices, and unclassified hardware resource categories.

**Note:** These resource categories are available starting from Hardware Asset Management version 10.1.0 onwards.


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
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Hardware Asset Management 10.0.0 features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[System property to cache asset and CI mappings](https://servicenow-staging.fluidtopics.net/access?context=c_ManagingAssets&family=washingtondc&ft:locale=en-US)**

The **sn\_itam\_enable\_cache\_for\_asset\_ci\_mapping** system property enables you to cache the following mappings:

    -   Asset and CI fields
    -   Asset state and CI install status
    -   Asset state and CI hardware status

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
</table>## Removed

Between your current release family and Zurich, some Hardware Asset Management 10.0.0 features or functionality were removed.

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
</table>## Deprecations

Between your current release family and Zurich, some Hardware Asset Management 10.0.0 features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The Hardware Asset Management Core UI deprecation is planned for future releases.

 Beginning with the Washington DC release, limited support is provided for the Hardware Asset Management Core UI interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, the best approach is to move to the Workspace experience. For more information, see [Hardware Asset Workspace](https://servicenow-staging.fluidtopics.net/access?context=using-ham-workspace&family=washingtondc&ft:locale=en-US).

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

Review information on how to activate Hardware Asset Management 10.0.0.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

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
</table>## Additional requirements

If any additional requirements were introduced or changed for Hardware Asset Management 10.0.0 we have noted them here.

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

If any specific browser requirements were introduced or changed for Hardware Asset Management 10.0.0 we have noted them here.

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

Review details on accessibility information for Hardware Asset Management 10.0.0, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Hardware Asset Management 10.0.0 we have noted them here.

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

If there are specific highlight considerations for Hardware Asset Management 10.0.0 we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Gain insights into the total cost of assets and use the information for strategic planning and execution within the asset estate.
-   Assess and evaluate the maturity of your Hardware Asset Management application through the Success portal view in Hardware Asset Workspace.
-   Gain insights into hardware asset warranty details received directly from Lenovo.
-   Manage onboarding of hardware products with Technology Reference Model \(TRM\) of Application Portfolio Management.
-   Streamline the Hardware Asset Management \(HAM\) licensing method for custom model categories to access Hardware Asset Management features and workflows.

 See [Hardware Asset Management](https://servicenow-staging.fluidtopics.net/access?context=ham-landing-page&family=washingtondc&ft:locale=en-US) for more information.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

