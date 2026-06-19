---
title: Release form
description: Product managers or release admins can create a release for a product or service version in Digital Product Release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/create-release-form.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Digital Product Release, IT Service Management]
---

# Release form

Product managers or release admins can create a release for a product or service version in Digital Product Release.

For more information, see [Create a release for a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-release.md).

<table id="table_tbx_pmr_lyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Release name

</td><td>

Unique release name to identify the release.

</td></tr><tr><td>

Release validates a new product version

</td><td>

Option to determine whether the release can validate the version.-   If selected, the version and template selections are impacted as below:
    -   Existing versions that are not validated by other releases are listed in the **Version** field for selection.
    -   Only templates with the **Validates version** set to true are shown in the **Release template** list.
-   If cleared, the version and template selections are impacted as below:
    -   All existing versions, whether validated or not, are listed in the **Version** field for selection. You can also add a new version as needed.
    -   Templates created with the **Validates version** set to false are shown in the **Release template** list.

</td></tr><tr><td>

Product or service

</td><td>

Product or service for which the release is created.

</td></tr><tr><td>

Version

</td><td>

Version of the product or service that is included in the release.The list of available versions is filtered based on the **Release validates a new product version** field.

-   If selected, the list displays only versions that have not been used in a previous release.

If you enter a new version, it will be created and associated with the release.This new version number must be unique.

-   If cleared, the list displays all versions of the product or service, including those with active releases.

</td></tr><tr><td>

Release template

</td><td>

Template that defines the release process. The template applies the predefined phases, tasks, policies, and approvals to this release.**Note:** When product-level release settings are configured, only the templates defined in the release settings are available for selection. For more information, see [Configure product-level release settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-config-product-release-setting.md).

The list of available templates is filtered based on the **Release validates a new product version** field.

-   If selected, the list displays only templates with the validates version option set to true.
-   If clear, the list displays only templates with the validates version option set to false.

For more information, see [Create a release template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-release-template.md).

Based on the template you select, the release follows either a timeline-oriented or stage-oriented release process. For more information, see [Release for a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-product-release.md).

</td></tr><tr><td>

Release readiness target

</td><td>

Release readiness target to indicate when the product or service should be ready for the release. **Note:** When product-level release settings are configured, only the release readiness target dates from the calendars defined in the release settings are available for selection.

For stage-oriented releases, whether this field is required depends on the system property **sn\_dpr.mandate\_release\_target**:

-   When set to false: This field is optional. You can leave it blank if needed.
-   When set to true: This field is required. You must specify a release readiness target before you can proceed.

For more information, see [Create a release readiness target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-rls-readiness-target.md).

This field appears only when **Out of band** is clear.

**Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

</td></tr><tr><td>

Out of band

</td><td>

Option to make this release as an out-of-band release, which means it isn’t associated with any existing release readiness target. Instead, a new release readiness target is created for the selected date.The option to create out-of-band releases depends on the following system properties configuration:

-   **out\_of\_band\_release\_allowed** is set to **true**.
-   You have one of the roles listed in **out\_of\_band\_release\_roles**.

For more information, see [Digital Product Release properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/digital-product-release-properties.md).

</td></tr><tr><td>

Release date

</td><td>

Date of release for an out-of-band release.This field appears only when **Out of band** is selected.

</td></tr><tr><td>

Release calendar

</td><td>

Release calendar on which the release is targeted. If a release target exists on the selected date in the release calendar, the release is added to it. If not, a release target is created and the release is added to it.For more information, see [Create a release calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-release-calendar.md).

This field appears only when **Out of band** is selected.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-reference.md)

