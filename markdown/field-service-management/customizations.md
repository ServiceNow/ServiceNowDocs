---
title: Advanced configurations
description: Describes the customization extension model for separating default functionality from custom scripts using read-only SNC and exposed includes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Script includes installed, Components installed, Reference, Field Service Management]
---

# Advanced configurations

Describes the customization extension model for separating default functionality from custom scripts using read-only SNC and exposed includes.

## Read-only SNC Scripts and Extended API Scripts

In complex FSM implementations, it’s important to maintain a clear separation between the default functionality and customizations. Clear separation between default functionality and custom code helps you quickly identify the source of an issue and streamline issue resolution and upgrades.

The Customization Extension Model introduces read-only SNC script includes and customizable extended API scripts to support:

-   Maintaining default scripts as immutable, providing a reliable fallback.
-   Enabling safe extension of functionality, without altering the original source.
-   Supporting quick issue triage, by reviewing only customized scripts.

The following KB article covers:

-   Implementing read-only SNC script includes for default functionality.
-   Applying standards for creating script includes and macroponent pages.
-   Managing upgrade scenarios and using fallback options effectively.
-   Overriding functions and customizing UI components with examples.

For detailed information, see [https://support.servicenow.com/kb?sys\_kb\_id=ffed91cd93ff2690f538fb2d6cba1047&amp;id=kb\_article\_view](https://support.servicenow.com/kb?sys_kb_id=ffed91cd93ff2690f538fb2d6cba1047&id=kb_article_view).

**Parent Topic:**[Script includes installed with Field Service Management](r_ScriptIncInstWFieldSrvMgmnt.md)

