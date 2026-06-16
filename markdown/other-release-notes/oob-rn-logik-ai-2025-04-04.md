---
title: Logik.ai 2025/04/04 release notes
description: Logik.ai 2025/04/04 release notes include new features, enhancements, and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-04-04.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 3
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/04/04 release notes

Logik.ai 2025/04/04 release notes include new features, enhancements, and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Apr 03, 2025, 8 pm CT|
|Test|Thursday, Apr 10, 2025, 8 pm CT|
|Prod|Friday, May 02, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build May 02, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New enhancement: Customizable UI with themes

\[Omitted image "cpq-rn-customizable-ui.png"\] Alt text:

Users within Logik admin can customize the look and feel of their layout by editing a custom theme. Once enabled, this functionality is visible on the layout page for your blueprint. Themes allow users to customize colors, fonts, spacing and more.

## New enhancement: Embedding Logik UI via the Web Component

The Logik Web Component allows a user to embed the Logik UI directly to a web page without the need to use an iFrame. The UI of the Logik Web Component is also compatible with themes to allow users to easily edit the look of the UI.

## New feature: Transaction Converse

Transaction Converse, a conversational feature in Transaction Manager, enables users to add, update, or delete line items in transactions or quotes by using natural language. This pilot feature streamlines bulk actions, provides preview and feedback controls, and learns from user interactions to improve over time.

## New feature: Smart Predict V2

Smart Predict V2 introduces a more powerful and accurate AI model for configuration predictions, featuring enhanced confidence, broader field support that covers Sets and Product Pickers, and expanded prediction options. Organizations can request access via support ticket, with V1 remaining available during the transition to V2’s superior capabilities.

## New enhancement: Upgraded model for Admin Assist

Admin Assist now leverages enhanced AI models to provide admins with context-aware answers and guidance sourced directly from support knowledge articles. This release enables admins to ask both feature-specific and scenario-based questions, reducing time to insight and improving support accessibility.

## New enhancement: Upgraded model for Function Assist

Function Assist now uses an enhanced AI model to deliver more accurate, compilable scripts from natural language prompts, with the same user experience as before. This update is available to all customers and partners.

## New feature: SF RLM – automatic quantity scaling for child line items

Child line item quantities are now automatically calculated based on the parent configurable line item’s quantity when `QuantityScaleMethod: Proportional/Constant` is used. This ensures all child quantities scale correctly in real time and persist through save operations, maintaining data consistency and reducing configuration errors.

## New enhancement: Validate Configured Items Event setting in Transaction Manager

Validate configured items is a setting on custom header events that, when enabled, will validate configurations of products in the transaction on event execution.

## New enhancement: Logik Configurator – Dropdown controls in sets

Currently, a normal set has inline controls configured as Boolean settings for three options: Add Row Above, Add Row Below, and Dropdown. When the Dropdown option is enabled, the end-user UI displays four actions: Add Above, Add Below, Copy, and Remove. If the Dropdown option is disabled, all four actions are removed simultaneously. With this enhancement, we have added the ability to individually control these four actions, rather than enabling or disabling them as a group.

\[Omitted image "cpq-rn-dropdown-controls-in-sets.png"\] Alt text:

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-15142|When all tiers in a layout were hidden by rules, the accordion tier component could sometimes run into an error. This has been corrected.|
|LGK-15705|When adding more than one solution config Blueprint simultaneously, Logik UI sometimes became unresponsive. This has been fixed.|
|LGK-15744|The word Undefined was observed flashing on the right side of the extended picklist field within a set after making a selection. This flickering in the input field after selection is corrected.|
|LGK-16144|The get configuration API did not include the “layouts”:\[\] portion of the response in some scenarios. This was corrected.|
|LGK-16155|The amendment/renewal Salesforce trigger checked whether the quote lines \(given an amendment or renewal quote\) had a config Id or didn't have a committed config Id. This didn't account for net new configurations created during the amendment. A new option is added for new renewal products to be excluded from the amendment trigger.|
|LGK-16177|In some scenarios, a rule set to "Leave Unchanged" was clearing out option of picklist in a set. This has been fixed.|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

