---
title: Combined Data Privacy release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Data Privacy from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-dataprivacy-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Data Privacy release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Data Privacy from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Privacy release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Privacy to Zurich

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

Licensing changes enable you to install Data Discovery, Data Discovery APIs, Data Anonymization, and Data Privacy APIs without an entitlement, but you must have an entitlement to run a job.

</td></tr><tr><td>

Yokohama

</td><td>

Licensing changes enable you to install Data Discovery, Data Discovery APIs, Data Anonymization, and Data Privacy APIs without an entitlement, but you must have an entitlement to run a job.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Data Privacy.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Create tests from the anonymization page](https://servicenow-staging.fluidtopics.net/access?context=dps-data-anonymization&family=washingtondc&ft:locale=en-US)**

You can now create tests directly from the anonymization page.

-   **[Create pattern technique mappings from the Policy page](https://servicenow-staging.fluidtopics.net/access?context=dps-create-anonymization-techniques&family=washingtondc&ft:locale=en-US)**

You can now create data patterns for anonymization techniques for partial anonymization directly from the Policy page.

-   **Support for pattern ordering**

You can see the ordering of the patterns during partial data anonymization job execution.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Child job execution](https://servicenow-staging.fluidtopics.net/access?context=dps-create-anonymization-policies&family=xanadu&ft:locale=en-US)**

Run child parallel jobs to optimize the duration of your job executions.

-   **[Encrypt with column level encryption \(CLE\)](https://servicenow-staging.fluidtopics.net/access?context=data-classification&family=xanadu&ft:locale=en-US)**

As a security admin, view whether the discovery field is encrypted or can be encrypted.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[AL/ML Based Data Discovery for Real Time Anonymization](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-data-privacy-landing&family=yokohama&ft:locale=en-US)**

Use AI/ML data discovery using Named Entity Recognition \(NER\) models to discover sensitive data that does not follow a pattern like name, address, organizations, and more; and run real-time anonymization.

-   **[Configuring Data Privacy for Now Assist](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-data-privacy&family=yokohama&ft:locale=en-US)**

Sanitize sensitive data entered in Now Assist prompts to prevent data leakage without impacting the response.

-   **[Discover sensitive data from attachments.](https://servicenow-staging.fluidtopics.net/access?context=configure-data-discovery-jobs&family=yokohama&ft:locale=en-US)**

Discover and report on sensitive data from attachments.


</td></tr><tr><td>

Zurich

</td><td>

-   **[New Data Discovery experience](https://servicenow-staging.fluidtopics.net/access?context=data-discovery-landing&family=zurich&ft:locale=en-US)**

Use the new Data Discovery experience, which simplifies the experience of discovering and anonymizing PII.

-   **[Column-level discovery](https://servicenow-staging.fluidtopics.net/access?context=granular-configuration&family=zurich&ft:locale=en-US)**

Select a specific column of a table for granular scanning during data discovery jobs.

-   **[Anonymization of encrypted field](https://servicenow-staging.fluidtopics.net/access?context=dps-data-anonymization&family=zurich&ft:locale=en-US)**

Anonymize encrypted columns to help you achieve compliance with data privacy regulations and defense-in-depth data protection.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Data Privacy features.

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

-   **[Discover and anonymize journal fields](https://servicenow-staging.fluidtopics.net/access?context=classifying-data&family=xanadu&ft:locale=en-US)**

Journal fields are now supported for Data Discovery and Data Anonymization with Workspace UI.

-   **[Data pattern regular expression length increased](https://servicenow-staging.fluidtopics.net/access?context=configure-data-discovery-patterns&family=xanadu&ft:locale=en-US)**

The data pattern regular expression length limit is increased to 1000 characters.

-   **[New base system data patterns](https://servicenow-staging.fluidtopics.net/access?context=default-data-patterns&family=xanadu&ft:locale=en-US)**

New base system data patterns are supported. See [Default data patterns](https://servicenow-staging.fluidtopics.net/access?context=default-data-patterns&family=xanadu&ft:locale=en-US) for more information.

-   **[Indicators for Security Center dependencies](https://servicenow-staging.fluidtopics.net/access?context=sec-center&family=xanadu&ft:locale=en-US)**

Indicators for missing Security Center dependencies have been added.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Full scan support added](https://servicenow-staging.fluidtopics.net/access?context=configure-data-discovery-jobs&family=zurich&ft:locale=en-US)**

Data Discovery jobs support full type scans, which scan for sensitive data patterns in all the records. You can also use an incremental scan, which acts as a delta scan from the point of the last full scan.

-   **[XLS and CSV support added](https://servicenow-staging.fluidtopics.net/access?context=data-discovery-attachment-scanning&family=zurich&ft:locale=en-US)**

Data Discovery attachment scan type jobs now support XLS and CSV files. Attachment scans are incremental scans by default.

-   **[Text to Regex from a LLM](https://servicenow-staging.fluidtopics.net/access?context=configure-data-discovery-patterns&family=zurich&ft:locale=en-US)**

Create a regex data pattern with the help of Now Assist, which supports all third-party LLMs approved by ServiceNow.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Data Privacy features or functionality were removed.

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

Between your current release family and Zurich, some Data Privacy features or functionality were deprecated.

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

Review information on how to activate Data Privacy.

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

Data Privacy is available with activation of the Data Privacy Plugin \(sn\_dp\_store\_app\). For details, see [Activate data privacy](https://servicenow-staging.fluidtopics.net/access?context=dps-activate-data-privacy&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Data Privacy is available with activation of the Data Privacy plugin \(sn\_dp\_store\_app\). For details, see [Activate data privacy](https://servicenow-staging.fluidtopics.net/access?context=dps-activate-data-privacy&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data Privacy we have noted them here.

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

If any specific browser requirements were introduced or changed for Data Privacy we have noted them here.

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

Review details on accessibility information for Data Privacy, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Data Privacy we have noted them here.

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

If there are specific highlight considerations for Data Privacy we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Faster workflows by creating tests straight from the Anonymization page
-   Get more insight from an enhanced Data Privacy UI experience

 See [Data Privacy](https://servicenow-staging.fluidtopics.net/access?context=data-privacy-landing&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Navigate an improved Data Privacy and Data Discovery UI in Next Experience dashboards.
-   Discover and anonymize sensitive data as it's entered with the real-time anonymization policy.
-   Anonymize and discover journal fields with expanded support and an increased data pattern regular expression limit of up to 1000 characters.

 See [Platform Privacy](https://servicenow-staging.fluidtopics.net/access?context=privacy-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Leverage Data Privacy in Now Assist to discover sensitive data in Now Assist prompts and data send to models.
-   Sanitize sensitive data from Now Assist prompts without impacting response.
-   Discover sensitive data from attachments using enhanced Data Discovery jobs.

 See [Platform Privacy](https://servicenow-staging.fluidtopics.net/access?context=privacy-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use a revamped Data Discovery interface, enhancing your Data Discovery experience with intuitive widgets, a streamlined user experience, and a guided setup for first-time users.
-   Target scans on specific table columns for discovery using column-level discovery and expanded support for Field Encryption.
-   Discover PII in Microsoft Excel and CSV files with expanded file support.
-   Generate regex patterns using prompts with the text-to-regex feature, which leverages Now Assist and supports all large language models \(LLMs\) approved by ServiceNow.

 See [Platform Privacy](https://servicenow-staging.fluidtopics.net/access?context=privacy-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

