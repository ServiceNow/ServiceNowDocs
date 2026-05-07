---
title: Integrating CPQ with visualization tools
description: Learn how CPQ connects to third-party visualization engines—CDS, kBridge, and Threekit—to render 2D/3D product views that respond to configuration inputs in real time.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Integrating CPQ with visualization tools

Learn how CPQ connects to third-party visualization engines—CDS, kBridge, and Threekit—to render 2D/3D product views that respond to configuration inputs in real time.

You can perform the following:

-   Show live visuals as users configure: colors, dimensions, options, and bundles can update the viewer instantly.
-   Coordinate UI + visual states: publish field values, set rows, and selected products to the renderer.
-   \(Optional\) Write back from the viewer: for supported vendors, user actions in the canvas can update fields.

## Supported vendors at a glance

|Vendor|Direction|What you can send|What can be written back|Notes|
|------|---------|-----------------|------------------------|-----|
|CDS|1-way and 2-way|Fields, Sets \(first 25 rows\), product pickers \(first 25 options\), Active Set Index|Fields; Sets via listener field JSON + rule parsing|Good for CAD/2D/3D; flexible mapping objects|
|kBridge|1-way and 2-way|Fields, Sets \(first 25 rows\), product pickers \(first 25 options\), Active Set Index|Fields; Sets via listener field JSON + rule parsing|Real-time 3D with rich event &amp; listener model|
|Threekit|1-way|Fields, Asset Id \(static or via field\), Active Set Index \(visual focus only\)|Not supported \(viewer → Logik\)|Use for high-fidelity visuals; map fields and asset selection|

**Note:** When sending sets or product pickers, CPQ publishes up to 25 rows/options. Indices and options beyond 25 are not transmitted. When using set repeaters, you can publish an Active Set Index trigger so the viewer shows the row the user is editing.

## How the integration works

1.  The layout component in the blueprint defines the visualization panel's position and size.
2.  Connection settings authorize and route traffic \(for example, the script or app URL, the auth token, and the subdomain\).
3.  The mapping block selects what CPQ data to send:
    -   `eventFields` — field variable names and their viewer keys
    -   `eventSets` — set variable names \(first 25 rows published as an array of objects\)
    -   `eventProductPickers` — selected options \(first 25\) as an array of objects
    -   `setActiveTriggers` — Boolean fields that indicate the active index in a set repeater
4.  \(Two-way only\) A listener field \(CPQ text field\) receives JSON from the viewer.
    -   Add a determination rule \(or enrichment\) to parse that JSON and update fields or set rows.
    -   If a listener field is present, only mappings explicitly configured for two-way will write back.

![Tabular format to showcase supported and non supported features of the visualization tools.](../images/cpq-integration-matrix.png)

## Data exchanged

-   Fields: Scalar values \(text, number, Boolean, picklist selection\).
-   Sets: Array of row objects \(first 25\). Use the Active Set Index to keep the visual in sync with the row being edited in a repeater.
-   Product pickers: Array of selected option objects \(first 25\).
-   Assets \(Threekit\): Provide a static `assetId` or an asset-ID field in Logik to enable dynamic asset selection.

## Security and environments

-   Auth and origin: Use vendor tokens and URLs appropriate to prod vs non-prod. Ensure your CPQ Runtime Client origins match calling domains.
-   CSP \(Content Security Policy\): Allow vendor script or app hosts for embedding and messaging. Coordinate with your security team and CPQ support to add domains.
-   Separation of concerns: Keep vendor credentials and tokens out of shared layouts across environments. Swap tokens when promoting.

## When to choose which tool

-   If you need bidirectional edits in the canvas, choose kBridge or CDS and implement a listener field and parsing rules.
-   If you need high-fidelity 3D with asset management and one-way updates, choose Threekit with an assetId or assetId field strategy.
-   If you have a heavy set-driven UX, prefer CDS or kBridge for two-way set JSON handling and Active Set Index synchronization.

## General guidelines

-   Map only what you need: Limit `eventFields`, `eventSets`, and `eventProductPickers` to essential data for performance.
-   Design for the 25-item cap: If users may exceed 25 set rows or product picker selections, add guardrails \(such as validation, paging, or summarization\).
-   Normalize for two-way: Define a stable JSON schema for listener payloads and centralize parsing logic in a managed rule or enrichment.
-   Promote safely: Externalize environment-specific values such as tokens and URLs. Verify visuals in test before production promotion.
-   Troubleshoot systematically:
    -   Check admin logs for runtime or script errors.
    -   Verify CSP and network access to vendor domains.
    -   Use the viewer’s console/devtools and CPQ debugger inputs to reproduce states.

**Related topics**  


[Integrating kBridge visualization](cpq-kbridge-visualization-integration.md)

[Integrating CDS or other third-party visualization tools](cds_visualization_integration.md)

[Integrating Threekit visualization](threekit-visualization-integration.md)

