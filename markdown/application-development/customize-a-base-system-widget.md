---
title: Customize a base system widget
description: Customize a base system or store app widget by cloning it to get an editable copy, or migrate a legacy widget to the current Lux format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/customize-a-base-system-widget.html
release: brazil
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 2
keywords: [Customize a base system widget, Clone to customize, Migrate a legacy widget to Lux]
breadcrumb: [Lux Widgets, Build with Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Customize a base system widget

Customize a base system or store app widget by cloning it to get an editable copy, or migrate a legacy widget to the current Lux format.

## Before you begin

Role required: admin

## About this task

A widget included with the base system, a widget that came from a store app, or one you haven't created or cloned yourself, opens read-only in the Editor. Widget Builder shows a banner explaining why: "This widget was created in a different project and cannot be edited directly. Clone the widget to create your own editable copy." Both code editors are read-only, and **Save**/**Publish** are disabled. Trying to delete such a widget from the Widgets catalog is blocked outright, with no confirmation dialog. That's a stricter block than editing, since removing it can affect other widgets that depend on it.

\[Omitted image "aiux-builder-locked-banner.png"\] Alt text: Locked editor banner with an explanation and a Clone button

**Note:** Clone-to-customize is a new way of customizing widgets, made possible by Lux's code-as-source-of-truth architecture. Because a widget's code is the definitive record, cloning it gives you a real, independent copy to edit. There's no risk of your changes being lost or conflicting the next time the platform or app is upgraded.

## Procedure

-   Clone to customize

    1.  Select **Clone** on the banner in the locked editor, or from the widget's action menu in the Widgets catalog.

    2.  Widget Builder creates a new widget, seeded with the base system or store app widget's current source.

        There's no restriction on scope, you can clone into any application scope, including the base system scope itself.

    3.  Edit the clone freely, as nothing you do to it changes the original.

    4.  Publish the clone to make your customized version available.

        The original base system or store app widget is unaffected and remains locked.

-   Migrate a legacy widget to Lux

    Older, pre-Lux widgets show an **Upgrade** button in the editor toolbar. Selecting it rewrites the widget's source into the current Lux component format locally, using the widget's existing metadata. No AI call is made, and nothing is sent over the network.

    1.  Select **Upgrade** in the toolbar.

    2.  Review the rewritten source in the Component tab.

        Widget Builder confirms success, or shows a warning if it couldn't fully convert something.

    3.  Select **Save**, then **Publish** as usual to complete the migration. Upgrading doesn't save or publish on its own.

    \[Omitted image "aiux-builder-upgrade-widget.png"\] Alt text: Upgrade button in the editor toolbar


