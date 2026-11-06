---
title: Configure an estimated data definition
description: Configure an estimated data definition by replacing the approximated data definition behind a success metric with one that matches your own business definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/value-library/configure-estimated-data-definition.html
release: australia
product: Value Library
classification: value-library
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Product value, Value Management, Impact reference, Impact]
---

# Configure an estimated data definition

Configure an estimated data definition by replacing the approximated data definition behind a success metric with one that matches your own business definition.

## Before you begin

Role required: Instance admin.

**Note:** You require an admin, pa\_power\_user, pa\_admin, or a pa\_data\_collector role to apply a data definition. Without one of these roles, the page is read-only and the action on each row is unavailable.

The dependent plugins for the product must be active. If they are not, the page shows a message naming the missing plugins and the path to enable them.

You can also open this page from the banner or from the**Configure metric** modal on the **Manage objectives and outcome**s page. The outcome and metric carry through, and the matching row is highlighted. Select Back to return to Manage objectives and outcomes with your scroll position and filters kept.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Impact Setup Hub**.

2.  On the **Configure impact product console**, select **Enable Value Management Data**.

3.  Select **Configure estimated data definitions** and expand the product group that contains the metric you want to configure.

    Each row shows the outcome details, the metric detail, the estimated data definition currently in use, the status of that definition, and the available action. The status is either **Not configured** or **Configured**.

4.  Select an outcome row with the status **Not configured** and then select the action link.

    A modal opens with three sections describing the current configuration, what you are about to configure, and why it matters, each populated with the selected outcome, its metric, and the estimated definition logic in use.

5.  Review the guidance, then select **Next**.

    Selecting **Cancel** at this point makes no change and leaves the status as **Not configured**.

6.  Set up the data definition for the metric according to your business needs.

    **Apply setup** stays unavailable until the required entries are valid.

7.  Select **Apply setup**.

    The definition is saved, the modal closes, and the status for that row changes from **Not configured** to **Configured**. Subsequent data collection for the metric uses the configuration you saved, and the supplied estimated logic is no longer applied.

    The action link on the row is grayed out and can no longer be selected. A tooltip states that the configuration has already been applied and cannot be changed. On the **Manage objectives and outcomes** page, the estimated indicator no longer appears for that metric and the outcome can be tracked.


**Related topics**  


[Manage objectives and outcomes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/value-library/manage-objectives-and-outcomes.md)

