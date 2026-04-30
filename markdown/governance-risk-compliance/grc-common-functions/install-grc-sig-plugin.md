---
title: Install the GRC: SIG Questionnaire Integration
description: The GRC: SIG Questionnaire Integration plugin installs the SIG questionnaire templates for use with the GRC: Third-party Risk Management application.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Standardized Information Gathering \(SIG\) Questionnaire Integration, GRC integrations, Common GRC features, Governance, Risk, and Compliance]
---

# Install the GRC: SIG Questionnaire Integration

The GRC: SIG Questionnaire Integration plugin installs the SIG questionnaire templates for use with the GRC: Third-party Risk Management application.

## Before you begin

Role required: sn\_vdr\_risk.admin, admin

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation.

<table id="table_gd1_sfv_zcb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that the ServiceNow plugins are activated.

</td><td>

Activate the Third-party Risk Management \(com.sn\_vdr\_risk\_asmt\) plugin.

 To verify that this plugin is activated, navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.

 For more information, see [Configuring Third-party Risk Management](../../grc-vendor-risk/concept/tprm-configuring.md) and the instructions for activating an entitled GRC application from the ServiceNow® Store: [Activate an entitled GRC ServiceNow Store application](../../grc-common/task/activate-entitled-grc-app.md) and [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

</td></tr></tbody>
</table>## Procedure

1.  Log in to the instance you want to install the application on.

2.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    A list of apps available for installation is displayed.

3.  Locate the app, select it, and select **Install**.

    The app installs GRC: Third-party Risk Management \(com.sn\_vdr\_risk\_asmt\) plugin and GRC SIG Questionnaire Integration \(com.sn\_sig\_asmt\) plugin.

    **Note:** When uninstalling the app, select the check box to retain the profile types profiles and indicators.


**Parent Topic:**[Standardized Information Gathering \(SIG\) Questionnaire Integration](../concept/grc-sig-integration.md)

