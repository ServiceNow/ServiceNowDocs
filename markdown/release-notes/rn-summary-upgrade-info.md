---
title: Upgrade information for all Brazil features and products
description: Cumulative release notes summary on upgrade information for Brazil features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-upgrade-info.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 2
breadcrumb: [Release notes summaries for Brazil features, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Upgrade information for all Brazil features and products

Cumulative release notes summary on upgrade information for Brazil features and products.

Before you upgrade to Brazil, review the upgrade information for any products you may have. Some products require you to complete specific tasks before you upgrade.

<table id="rn-summary-upgrade-info-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Desktop Actions

</td><td>

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download AI Desktop Actions installer for defined desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including the Now Assist for Vulnerability Response product name, which will be replaced with ServiceNow Otto for Unified Security Exposure Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

Enhancements to Container Vulnerability Response permit you to see enriched container vulnerability data on data imports from your third-party scanners. After you upgrade, perform a full import to view the features on discovered container image, container image finding, and container vulnerable item records that are described in the following New in the Brazil release section.

If you're currently using Container Vulnerability Response, and you don't intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Brazil release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in CRM Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

Customers who have not opted into new third-party LLM models may be silently routed to them during skill execution. If the new model is not provisioned or available in the customer's environment, this will result in skill execution failures. Check the models your skills are using in the AI Admin Hub console.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Brazil features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/release-notes-summaries.md)

