---
title: Combined Data Privacy release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Data Privacy from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-dataprivacy-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Data Privacy release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Data Privacy from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Privacy release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Privacy to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Data Privacy.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Create tests from the anonymization page](https://www.servicenow.com/docs/access?context=dps-data-anonymization&family=washingtondc&ft:locale=en-US)**

You can now create tests directly from the anonymization page.

-   **[Create pattern technique mappings from the Policy page](https://www.servicenow.com/docs/access?context=dps-create-anonymization-techniques&family=washingtondc&ft:locale=en-US)**

You can now create data patterns for anonymization techniques for partial anonymization directly from the Policy page.

-   **Support for pattern ordering**

You can see the ordering of the patterns during partial data anonymization job execution.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Child job execution](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&family=xanadu&ft:locale=en-US)**

Run child parallel jobs to optimize the duration of your job executions.

-   **[Encrypt with column level encryption \(CLE\)](https://www.servicenow.com/docs/access?context=data-classification&family=xanadu&ft:locale=en-US)**

As a security admin, view whether the discovery field is encrypted or can be encrypted.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[AL/ML Based Data Discovery for Real Time Anonymization](https://www.servicenow.com/docs/access?context=now-assist-for-data-privacy-landing&family=yokohama&ft:locale=en-US)**

Use AI/ML data discovery using Named Entity Recognition \(NER\) models to discover sensitive data that does not follow a pattern like name, address, organizations, and more; and run real-time anonymization.

-   **[Configuring Data Privacy for Now Assist](https://www.servicenow.com/docs/access?context=configure-now-assist-data-privacy&family=yokohama&ft:locale=en-US)**

Sanitize sensitive data entered in Now Assist prompts to prevent data leakage without impacting the response.

-   **[Discover sensitive data from attachments.](https://www.servicenow.com/docs/access?context=configure-data-discovery-jobs&family=yokohama&ft:locale=en-US)**

Discover and report on sensitive data from attachments.


</td></tr><tr><td>

Zurich

</td><td>

-   **[New Data Discovery experience](https://www.servicenow.com/docs/access?context=data-discovery-landing&family=zurich&ft:locale=en-US)**

Use the new Data Discovery experience, which simplifies the experience of discovering and anonymizing PII.

-   **[Column-level discovery](https://www.servicenow.com/docs/access?context=granular-configuration&family=zurich&ft:locale=en-US)**

Select a specific column of a table for granular scanning during data discovery jobs.

-   **[Anonymization of encrypted field](https://www.servicenow.com/docs/access?context=dps-data-anonymization&family=zurich&ft:locale=en-US)**

Anonymize encrypted columns to help you achieve compliance with data privacy regulations and defense-in-depth data protection.


</td></tr><tr><td>

Australia

</td><td>

-   **[Real-time alerting and blocking of sensitive data](https://www.servicenow.com/docs/access?context=real-time-protection&family=australia&ft:locale=en-US)**

Analyze user input in real time at the field level to identify sensitive data and alert users about potential sensitive data entry. You can also choose to block users from saving this information.

-   **[Data logs for real-time sensitive data](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&family=australia&ft:locale=en-US)**

Leverage real-time alerting and blocking capabilities to obtain insights into where sensitive data is being entered into the instance and by which users.

-   **[Real-time sensitive data-scanning for attachments](https://www.servicenow.com/docs/access?context=attachment-quarantine-policies&family=australia&ft:locale=en-US)**

Scan attachments for sensitive data during user uploads into fields. If sensitive data is detected, the attachment is quarantined. This restricts the access and download of the file to the original document owner and authorized users until the admin reviews the files.

-   **[New Named Entity Recognition \(NER\) model data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&family=australia&ft:locale=en-US)**

Employ new AI/ML-based model data patterns \(Address, City, State, Country, Job Position, and Salary\) to detect and anonymize sensitive data.

-   **[Anonymization support for catalog variables](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&family=australia&ft:locale=en-US)**

Anonymize sensitive data in catalog items \(including record producers\) using anonymization jobs \(in production and during cloning\).

-   **[New base system Regular Expression \(RegEx\) data patterns](https://www.servicenow.com/docs/access?context=dds-review-discovery-findings&family=australia&ft:locale=en-US)**

Employ new base system regular expression data patterns to detect and anonymize sensitive data in line with global compliance requirements.

-   **[Enhanced anonymization reporting](https://www.servicenow.com/docs/access?context=dps-create-anonymization-job&family=australia&ft:locale=en-US)**

Demonstrate defensible compliance to regulators, auditors and internal teams using the new anonymization dashboard to provide quantitative insights into anonymization and data protection operations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Data Privacy features.

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

-   **[Discover and anonymize journal fields](https://www.servicenow.com/docs/access?context=classifying-data&family=xanadu&ft:locale=en-US)**

Journal fields are now supported for Data Discovery and Data Anonymization with Workspace UI.

-   **[Data pattern regular expression length increased](https://www.servicenow.com/docs/access?context=configure-data-discovery-patterns&family=xanadu&ft:locale=en-US)**

The data pattern regular expression length limit is increased to 1000 characters.

-   **[New base system data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&family=xanadu&ft:locale=en-US)**

New base system data patterns are supported. See [Default data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&family=xanadu&ft:locale=en-US) for more information.

-   **[Indicators for Security Center dependencies](https://www.servicenow.com/docs/access?context=sec-center&family=xanadu&ft:locale=en-US)**

Indicators for missing Security Center dependencies have been added.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Full scan support added](https://www.servicenow.com/docs/access?context=configure-data-discovery-jobs&family=zurich&ft:locale=en-US)**

Data Discovery jobs support full type scans, which scan for sensitive data patterns in all the records. You can also use an incremental scan, which acts as a delta scan from the point of the last full scan.

-   **[XLS and CSV support added](https://www.servicenow.com/docs/access?context=data-discovery-attachment-scanning&family=zurich&ft:locale=en-US)**

Data Discovery attachment scan type jobs now support XLS and CSV files. Attachment scans are incremental scans by default.

-   **[Text to Regex from a LLM](https://www.servicenow.com/docs/access?context=configure-data-discovery-patterns&family=zurich&ft:locale=en-US)**

Create a regex data pattern with the help of Now Assist, which supports all third-party LLMs approved by ServiceNow.


</td></tr><tr><td>

Australia

</td><td>

-   **New experience**
    -   [Optional condition filter](https://www.servicenow.com/docs/access?context=dps-create-anonymization-job&family=australia&ft:locale=en-US) when running anonymization jobs to fine tune the scope of data to be anonymized.
    -   [Specific anonymization policy](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&family=australia&ft:locale=en-US) for catalog variables to anonymize sensitive data in catalog requests.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Data Privacy features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Data Privacy features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

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

Data Privacy is available with activation of the Data Privacy Plugin \(sn\_dp\_store\_app\). For details, see [Activate data privacy](https://www.servicenow.com/docs/access?context=dps-activate-data-privacy&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Data Privacy is available with activation of the Data Privacy plugin \(sn\_dp\_store\_app\). For details, see [Activate data privacy](https://www.servicenow.com/docs/access?context=dps-activate-data-privacy&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Data Privacy is available with activation of the Data Privacy plugin \(`sn_dp_store_app`\). For details, see [Activate data privacy](https://www.servicenow.com/docs/access?context=dps-activate-data-privacy&family=australia&ft:locale=en-US).

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

 See [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Navigate an improved Data Privacy and Data Discovery UI in Next Experience dashboards.
-   Discover and anonymize sensitive data as it's entered with the real-time anonymization policy.
-   Anonymize and discover journal fields with expanded support and an increased data pattern regular expression limit of up to 1000 characters.

 See [Platform Privacy](https://www.servicenow.com/docs/access?context=privacy-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Leverage Data Privacy in Now Assist to discover sensitive data in Now Assist prompts and data send to models.
-   Sanitize sensitive data from Now Assist prompts without impacting response.
-   Discover sensitive data from attachments using enhanced Data Discovery jobs.

 See [Platform Privacy](https://www.servicenow.com/docs/access?context=privacy-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use a revamped Data Discovery interface, enhancing your Data Discovery experience with intuitive widgets, a streamlined user experience, and a guided setup for first-time users.
-   Target scans on specific table columns for discovery using column-level discovery and expanded support for Field Encryption.
-   Discover PII in Microsoft Excel and CSV files with expanded file support.
-   Generate regex patterns using prompts with the text-to-regex feature, which leverages Now Assist and supports all large language models \(LLMs\) approved by ServiceNow.

 See [Platform Privacy](https://www.servicenow.com/docs/access?context=privacy-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Discover and block sensitive data from user inputs to prevent it from entering the platform, alert users when sensitive data is entered to raise awareness, and leverage sensitive data logs to understand where and who is entering sensitive data.
-   Scan and quarantine attachments that contain sensitive data to restrict their access and downloading.
-   Define conditions for the anonymization of sensitive data to meet business specific requirements. Use the enhanced data anonymization dashboard to obtain insights and metrics about data protection and anonymization for executive reporting.

 See [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

