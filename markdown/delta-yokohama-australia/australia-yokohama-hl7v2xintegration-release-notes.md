---
title: Combined HL7 v2.x Integration release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for HL7 v2.x Integration from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-hl7v2xintegration-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined HL7 v2.x Integration release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for HL7 v2.x Integration from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family HL7 v2.x Integration release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading HL7 v2.x Integration to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Australia, new features were introduced for HL7 v2.x Integration.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   **[HL7 v2.x Inbound REST API](https://www.servicenow.com/docs/access?context=hl7-inbound-api&family=australia&ft:locale=en-US)**

The HL7 v2.x Inbound REST API receives inbound HL7 v2.x ADT messages from EHR systems over HTTP and returns standard HL7 v2.x acknowledgment responses. It implements the HAPI HL7-over-HTTP convention, accepting raw pipe-delimited ER7 message bodies and processing them against configured parser profiles.

-   **[HL7 message log](https://www.servicenow.com/docs/access?context=hl7-message-log-about&family=australia&ft:locale=en-US)**

Every inbound HL7 v2.x message is stored with its raw payload, ACK response, message metadata \(type, trigger event, sending application and facility, message control ID\), and processing status. Metadata fields are queryable and available as Flow Designer trigger conditions.

-   **[Parser configurations](https://www.servicenow.com/docs/access?context=hl7-parser-configs-about&family=australia&ft:locale=en-US)**

When a message is received, ServiceNow parses it with the matching parser configuration and writes the extracted values to the message log record's structured JSON \(`parsed_data`\). Parser configurations define which segments and fields to extract and the output path for each value.

-   **Demo parser configurations**

Demo parser configurations for ADT A01, A02, A03, and A08 are available when you load demo data, covering the EVN, PID, and PV1 segments. They are editable, and you can clone them for hospital-specific customization.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing HL7 v2.x Integration features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Australia, some HL7 v2.x Integration features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Australia, some HL7 v2.x Integration features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Review information on how to activate HL7 v2.x Integration.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

HL7 v2.x Integration is distributed as a separate application through the ServiceNow Store. Request the application from the ServiceNow Store and install it to activate it on your instance.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for HL7 v2.x Integration we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If any specific browser requirements were introduced or changed for HL7 v2.x Integration we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Review details on accessibility information for HL7 v2.x Integration, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If there are specific localization considerations for HL7 v2.x Integration we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If there are specific highlight considerations for HL7 v2.x Integration we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   Works alongside the HL7 v2.x Inbound REST API to receive HL7 v2.x messages from EHR systems over HTTP and return standards-compliant acknowledgment responses.
-   Receive raw HL7 v2.x messages directly in ServiceNow and automatically return standards-compliant ACK responses — with no custom scripting on the integration engine side.
-   Parse raw HL7 v2.x messages into structured JSON on the message log using a configurable, no-code parser, enabling hospital workflow automation without HL7 v2.x expertise.
-   Demo parser configurations for ADT A01 \(Admit\), A02 \(Transfer\), A03 \(Discharge\), and A08 \(Update\) provide ready-to-edit starting points for the most common hospital ADT workflows.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

