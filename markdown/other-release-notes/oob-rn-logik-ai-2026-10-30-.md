---
title: ServiceNow CPQ 2026/10/30 release notes
description: ServiceNow CPQ October 30, 2026 release notes include new enhancements and bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2026-10-30-.html
release: other
topic_type: reference
last_updated: "2026-11-03"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# ServiceNow CPQ 2026/10/30 release notes

ServiceNow CPQ October 30, 2026 release notes include new enhancements and bug fixes.

## Schedule

This build upgrades ServiceNow CPQ environments according to the following schedule:

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Oct 29, 2026, 8 pm CT|
|Test|Thursday, Oct 29, 2026, 8 pm CT|
|Prod|Friday, Nov 06, 2026, 8 pm CT|

Example: an environment with URL, https://\[YourLogikURL\].prod.logik.io, receives this build Nov 06, 2026.

## Release notes

This release version includes the following new enhancements and fixes.

## ServiceNow CPQ Configurator MCP

Lets an AI assistant start, configure, review, and save product configurations in ServiceNow CPQ through the Model Context Protocol \(MCP\). In this first phase, the feature is available on Quote Experience-enabled instances and Quote Experience-connected Salesforce instances.

## Product Configurator runtime MCP improvements

Limits what an external AI agent can see and set to the fields and options a user can see and set in the UI. Hides admin tools from non-admin agents, adds ServiceNow JWT-based authentication that matches the standard used for configurations and Quote Experience, and supports the full configuration lifecycle: creating and initializing, saving, and reconfiguring.

## Quote Experience version and quote revision integration

Productizes the integration between Quote Experience versions and quote revisions, and supports the existing quote revision functionality.

## AI-assisted quote line upload from CSV and Excel

Transaction AI translates CSV and Excel quote data into quote lines, including files with a few or hundreds of columns and a few or thousands of rows. Uploaded data never applies items outside the user's permission scope. When a line fails to upload, the user can download a file with the reason for each failure.

## Quote Experience PDF document generation

Productizes the PDF document generation event and integration in Quote Experience.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|PRB2060558|Fixed issue where the Blueprint layout editor reverted styles when opened.|
|PRB2085867|Addressed issue with UI warning message colors not meeting accessibility standards.|
|PRB2087372|Fixed issue where saving a configuration during Add Lines in Quote Experience generated many unnecessary option requests, many of which failed.|
|PRB2097676|Fixed issue where the Add Approver modal in Quote Experience advanced approvals appeared behind the UI effect modal.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other ServiceNow CPQ users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

