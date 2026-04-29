---
title: Install the SOX Content Pack
description: Install the SOX Content Pack for use with the core GRC applications.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOX content pack, GRC content packs, Common GRC features, Governance, Risk, and Compliance]
---

# Install the SOX Content Pack

Install the SOX Content Pack for use with the core GRC applications.

## Before you begin

Role required: sn\_compliance.admin, sn\_risk.admin, or sn\_audit\_admin, admin

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation.

<table id="table_ffc_f5g_lwb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that the ServiceNow plugins are activated.

</td><td>

Activate one of the following GRC plugins:

-   GRC: Policy and Compliance Management \(com.sn\_compliance\)
-   GRC Risk Management \(com.sn\_risk\)
-   GRC: Audit Management \(com.sn\_audit\)

 To verify that this plugin is activated, navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions your organization has purchased.

</td></tr></tbody>
</table>## Procedure

1.  Enter info re: Legal Notice.

2.  If you have not installed the application, follow the instructions to install it.

    1.  Log in to the instance you want to install the application on.

    2.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

        A list of apps available for installation is displayed.

    3.  Locate the app, select it, and click **Install**.

        Your app is automatically installed onto your instance.

        When uninstalling the app, select the check box to retain the profile types profiles and indicators.


**Parent Topic:**[Sarbanes-Oxley \(SOX\) Content Pack](../concept/sn-store-SOX-governance-risk-compliance.md)

