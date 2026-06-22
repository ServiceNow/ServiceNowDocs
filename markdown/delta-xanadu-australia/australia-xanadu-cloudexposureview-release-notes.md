---
title: Combined Cloud Exposure View release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Cloud Exposure View from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-cloudexposureview-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Cloud Exposure View release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Cloud Exposure View from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Cloud Exposure View release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Cloud Exposure View to Australia

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

The Cloud Exposure View is a workspace in the Cloud Security for Cloud Workspace application that is supported by the Unified Security Exposure Management application. Unified Security Exposure Management \(USEM\) and the Cloud Security for Cloud Workspace applications are required. USEM is available to all customers who are entitled to Vulnerability Response. See [Unified Security Exposure Management release notes](https://www.servicenow.com/docs/access?context=secops-sem-rn&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Cloud Exposure View.

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

-   **[Enhancements to the Wiz Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=zurich&ft:locale=en-US)**
    -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key.

**Note:** This enhancement is supported for new customers only.

For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination of vulnerability, asset\_id, and proof.

    -   Added the source\_id column to the Container Image Finding table \(sn\_vul\_container\_image\_findings\) and mapped the id attribute from the Wiz import to this field on findings records.

**Note:** Perform a full import after upgrading to view the enhancement on container image findings, container image, and container image vulnerabilities records.

    -   The image repository name format for new and existing discovered container images has been updated to align with the discovery format. The supported format is registry/repository. A separate finding is created for a repository present in each registry.
    -   Appended all repositories that are associated with an image to the Repository field on the Discovered Container Image \[sn\_vul\_container\_image\] table, which can help you see images from specific repositories.
    -   You can configure the **First** parameter for the Wiz Asset Integration to help you resolve 504 errors. You can reduce the page size if you are having memory issues or generating errors. The default value is 500.
    -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includes src\_ci, vulnerability, package, image\_layer, and image\_repository.
-   **[\[Placeholder link text to key bundle-security.vr-cloud-security-exploring\]](https://www.servicenow.com/docs/access?context=vr-cloud-security-exploring&family=zurich&ft:locale=en-US)**

The Cloud Exposure View module provides a single location for cloud security teams to monitor and act on all their cloud-related security findings from multiple vendors across their cloud environments.

    -   Configure widgets that display interactive visualizations and filter assets by category for findings, assets, and exceptions.
    -   View panels with links on a single page that direct you to the following detailed lists:
        -   Needs Attention
        -   Cloud resources with active findings
        -   Top Accounts/Assets by Risk
        -   Toxic combinations
        -   Compliance scores
    -   View aggregated security data imported from third-party vendors.
See [Unified Security Exposure Management release notes](https://www.servicenow.com/docs/access?context=secops-sem-rn&family=zurich&ft:locale=en-US) for more information about Unified Security Exposure Management.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Cloud Exposure View features.

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

Between your current release family and Australia, some Cloud Exposure View features or functionality were removed.

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

Between your current release family and Australia, some Cloud Exposure View features or functionality were deprecated.

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

Review information on how to activate Cloud Exposure View.

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

Install the required applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Cloud Exposure View we have noted them here.

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

If any specific browser requirements were introduced or changed for Cloud Exposure View we have noted them here.

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

Review details on accessibility information for Cloud Exposure View, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Cloud Exposure View we have noted them here.

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

If there are specific highlight considerations for Cloud Exposure View we have noted them here.

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

-   Monitor and act on all your cloud-related security findings from multiple vendors across your cloud environments.
-   Configure widgets that display interactive visualizations and filter assets by category for findings, assets, and exceptions.
-   View panels that link you to lists for more details about your findings.
-   View aggregated security data imported from third-party vendors.
-   Aggregated data from the Cloud Exposure View can be viewed in the Unified Cloud workspace that is supported by ITOM Cloud Accelerate. See [ITOM Cloud Accelerate release notes](https://www.servicenow.com/docs/access?context=itom-cloud-accelerate-rn&family=zurich&ft:locale=en-US) for more information.

 See [Exploring Cloud Exposure View](https://www.servicenow.com/docs/access?context=vr-cloud-security-exploring&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

