---
title: Configurable workspace components examples
description: To grasp how to interact with configurable workspace components, review these examples.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Testable Configurable Workspace components, Reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
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

    ![Screenshot showing tooltip error](../image/atf-sn-canvas-comp-tooltip-error.png)

    **Note:** An error is shown if the toolTip name doesn't exactly matches the tab name you want to open up.

-   order: Depending on the group entry, the order number is decided. The order starts at 1. For instance, if you've selected 'top' for a group in a toolbar with six items and want to access the second tab from the top, you'd enter '2' as the order number. Similarly you'd enter '5' as the order number if you've selected 'bottom' for a group.

    ![Screenshot showing order number depending on the group](../image/atf-sn-canvas-comp-order.png)


**Note:** When you submit an action to select a specific tab \(based on its group and order\), that tab becomes focused or highlighted. When you enter the exact name of the tab in the toolTip, that tab opens up.

## now-uxf-tab-set

For now-uxf-tab-set component, it has the following three actions:

-   Assert tab selected by label
-   Select tab by order
-   Select tab by label

These are the expected values for the actions:

-   label: Enter the exact name of the tab that you want to assert if it exists. For example, after selecting the Assert tab selected by label action, enter 'Hardware assets' to check if the 'Hardware assets' tab is present. The expected return value is True if it exists. If you select Select tab by label action, enter the name of the tab in the toolbar you want to open.
    -   Assert tab selected by label

        ![Screenshot showing Assert tab selected by label action](../image/atf-tab-comp-label-assert.png)

    -   Select tab by label

        ![Screenshot showing Select tab by label action](../image/atf-tab-comp-label.png)

-   order: The order number you enter determines which tab opens on the selected toolbar.

    ![Screenshot showing Select tab by order action](../image/atf-tab-comp-order.png)


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

    ![Screenshot showing selecting list UI action](../image/atf-now-record-clickUI.png)

-   Select the record from the list you want to validate.

    **Note:** All the records in the list show up when you select the Validate record visibility in the list action.

    ![Screenshot showing selecting record to validate](../image/atf-now-record-validate.png)

-   Select the required UI action to validate its visibility in the list.

    ![Screenshot showing list UI action validation](../image/atf-now-record-UI-validate.png)

-   Select the required record to open from the list.

    **Note:** All the records in the list show up when you select the Open a record in the list action.

    ![Screenshot showing to select a record to open](../image/atf-now-record-open.png)


**Parent Topic:**[Testable Configurable Workspace components](../reference/atf-conf-ws-components.md)

