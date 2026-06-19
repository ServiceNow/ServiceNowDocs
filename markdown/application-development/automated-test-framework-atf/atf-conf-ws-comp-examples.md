---
title: Configurable workspace components examples
description: To grasp how to interact with configurable workspace components, review these examples.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-conf-ws-comp-examples.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Testable Configurable Workspace components, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Configurable workspace components examples

To grasp how to interact with configurable workspace components, review these examples.

**Note:** When you submit an action in a component, a test step is created.

## sn-canvas-toolbar

For sn-canvas-toolbar component, it has the following four actions:

-   Assert button exists by group and tool tip
-   Assert button selected by group and tool tip
-   Select button by group and order
-   Select button by group and tool tip

These are the expected values for the actions:

-   group: Enter either 'top' or 'bottom' depending on which tab in the toolbar you want to interact with.
-   toolTip: Name of the tab in the toolbar you want to open.

    \[Omitted image "atf-sn-canvas-comp-tooltip-error.png"\] Alt text: Screenshot showing tooltip error

    **Note:** An error is shown if the toolTip name doesn't exactly matches the tab name you want to open up.

-   order: Depending on the group entry, the order number is decided. The order starts at 1. For instance, if you've selected 'top' for a group in a toolbar with six items and want to access the second tab from the top, you'd enter '2' as the order number. Similarly you'd enter '5' as the order number if you've selected 'bottom' for a group.

    \[Omitted image "atf-sn-canvas-comp-order.png"\] Alt text: Screenshot showing order number depending on the group


**Note:** When you submit an action to select a specific tab \(based on its group and order\), that tab becomes focused or highlighted. When you enter the exact name of the tab in the toolTip, that tab opens up.

## now-uxf-tab-set

For now-uxf-tab-set component, it has the following three actions:

-   Assert tab selected by label
-   Select tab by order
-   Select tab by label

These are the expected values for the actions:

-   label: Enter the exact name of the tab that you want to assert if it exists. For example, after selecting the Assert tab selected by label action, enter 'Hardware assets' to check if the 'Hardware assets' tab is present. The expected return value is True if it exists. If you select Select tab by label action, enter the name of the tab in the toolbar you want to open.
    -   Assert tab selected by label

        \[Omitted image "atf-tab-comp-label-assert.png"\] Alt text: Screenshot showing Assert tab selected by label action

    -   Select tab by label

        \[Omitted image "atf-tab-comp-label.png"\] Alt text: Screenshot showing Select tab by label action

-   order: The order number you enter determines which tab opens on the selected toolbar.

    \[Omitted image "atf-tab-comp-order.png"\] Alt text: Screenshot showing Select tab by order action


## now-record-list-connected

For now-record-list-connected component, it has the following five actions:

-   Apply filter on the list
-   Click a list UI action button
-   Validate record visibility in the list
-   Validate the visibility of list's declarative actions
-   Open a record in the list

These are the expected values for the actions:

-   Select the required UI action.

    **Note:** Only the UI actions which are available in the list shows up.

    \[Omitted image "atf-now-record-clickUI.png"\] Alt text: Screenshot showing selecting list UI action

-   Select the record from the list you want to validate.

    **Note:** All the records in the list show up when you select the Validate record visibility in the list action.

    \[Omitted image "atf-now-record-validate.png"\] Alt text: Screenshot showing selecting record to validate

-   Select the required UI action to validate its visibility in the list.

    \[Omitted image "atf-now-record-UI-validate.png"\] Alt text: Screenshot showing list UI action validation

-   Select the required record to open from the list.

    **Note:** All the records in the list show up when you select the Open a record in the list action.

    \[Omitted image "atf-now-record-open.png"\] Alt text: Screenshot showing to select a record to open


**Parent Topic:**[Testable Configurable Workspace components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-conf-ws-components.md)

