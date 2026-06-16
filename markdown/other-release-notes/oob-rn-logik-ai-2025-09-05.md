---
title: Logik.ai 2025/09/05 release notes
description: Logik.ai 2025/09/05 release notes include new features and enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-09-05.html
release: other
topic_type: reference
last_updated: "2025-11-26"
reading_time_minutes: 3
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/09/05 release notes

Logik.ai 2025/09/05 release notes include new features and enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, September 04, 2025, 8 pm CT|
|Test|Thursday, September 18, 2025, 8 pm CT|
|Prod|Friday, October 03, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build October 03, 2025.

## Release notes

This release version includes the following new features, new enhancements, and bug fixes.

## New feature: AI rule search

AI rule search lets you quickly search for rule actions and impacted variables from a Blueprint's related rules screen. To enable AI rule search, open a support ticket, and then follow these steps:

1.  Go to **Utilities** &gt; **Settings**, and then under AI Features, toggle Enable Rules Search on.

    \[Omitted image "cpq-rn-ai-search-enable-rules-search-toggle.png"\] Alt text:

2.  In the Blueprint that you want to search, go to the related rules list and toggle **Enable Rules Search** on in the upper right corner.

    \[Omitted image "cpq-rn-ai-search-blueprint.png"\] Alt text:


Turning on AI rules search shows a new AI Search symbol \[Omitted image "cpq-rn-ai-search-icon.png"\] Alt text: in the upper right corner of the related rules list that you can click on the upper right hand corner. Click it to enable the new AI-driven search experience.

The following searches are supported:

-   Search by rule name or variable name
-   Search for rules that condition on a field name or variable name
-   Search for rules that targets a field name or variable name
-   Search for rules that reference on a table
-   Search for rule action type
-   Search for whether rule has advanced scripts
-   Advanced search for rules that add specific products by their product ID \(product rule\)
-   Advanced search for rules that include or exclude specific values \(inclusion/exclusion rule\)
-   Advanced search for rules that throw error, warning, or info messages \(message rule\)
-   Advanced search for rules that hide specific fields \(visibility rule\)
-   Advanced search for rules that set values to specific fields \(determination rule\)
-   Advanced search for rules that condition on a specific clause \(such as a rule that executes when a field's value is greater than x\)

Unsupported searches include searches of fields that are contained in sets and advanced searches for actions that use advanced scripts other than product rules.

## New enhancement: Layout action bar

Buttons that were previously available only in the header can now be inserted into the layout in an action bar. To add the action bar to your layout, follow these steps:

1.  In a tier, click the down arrow icon.

    \[Omitted image "cpq-rn-ai-search-layout-action-bar-1.png"\] Alt text:\[Omitted image "cpq-rn-ai-search-layout-action-bar-2.png"\] Alt text:

2.  In the action bar, click the gear icon to open the edit menu.

    \[Omitted image "cpq-rn-ai-search-layout-action-bar-properties.png"\] Alt text:


## New enhancement: Hide the header

Using a check box in the header settings, you can now hide the entire header from a layout.

\[Omitted image "cpq-rn-ai-search-hide-header.png"\] Alt text:

## Bug fixes

<table id="table_gxv_hvs_l4b"><thead><tr><th>

Fix

</th><th>

Short description

</th></tr></thead><tbody><tr><td>

LGK-18658

</td><td>

Fixed an issue where session expiration was incorrectly extended across contexts, causing session not found errors. To prevent 404 errors, session expiration is now reset only in the correct context and separate heartbeats are maintained for transaction and configuration sessions.

</td></tr><tr><td>

LGK-18666

</td><td>

Made sure cfgRequest.txn.persona.value is correctly populated on initialization.

</td></tr><tr><td>

LGK-18747

</td><td>

Create Transaction History files async so larger files no longer time out. Display file download in admin notifications similar to the UX of blueprint deployments.

</td></tr><tr><td>

LGK-19156

</td><td>

Improved line item grid load speed by reducing fields returned to only those required.

</td></tr><tr><td>

LGK-19157

</td><td>

To enhance performance when adding products to a quote, reduced unnecessary rule executions during upsertLines.

</td></tr><tr><td>

LGK-19180

</td><td>

Fix introduced for the rules engine to return the updatedHiddenFields value only if the value of the field has changed. Changes in the visibility of these fields would still be returned in the normal fields array in the response. This prevents the transaction service from trying to save a changelog entry when it should not be saved.

</td></tr><tr><td>

LGK-19218

</td><td>

Added POST API to getLines. URL path: /txn/\{transactionId\}/lines:. Same request params and headers as the GET getLines API.```
RequestBody:
    LineResponseFilter:
      title: LineResponseFilter
      type: object
      properties:
        filteredFields:
          type: array
          items:
            type: string
```

</td></tr><tr><td>

LGK-19301

</td><td>

Fixed an issue where images inside the image viewer were not center aligned.

</td></tr></tbody>
</table>## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

