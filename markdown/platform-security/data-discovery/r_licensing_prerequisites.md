---
title: Licensing prerequisites for Text to RegEx
description: Text to RegEx requires specific licenses to be active in your instance and relies on the Now Assist for Vault plugin. This reference describes all licensing requirements you must meet to use Text to RegEx.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/r\_licensing\_prerequisites.html
release: australia
product: Data Discovery
classification: data-discovery
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 2
keywords: [licensing, prerequisites, license check, Now Assist for Vault, Vault, Pro Plus]
breadcrumb: [Using Text to RegEx, Create new data pattern, Data Discovery sources, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Licensing prerequisites for Text to RegEx

Text to RegEx requires specific licenses to be active in your instance and relies on the Now Assist for Vault plugin. This reference describes all licensing requirements you must meet to use Text to RegEx.

## Required licenses

To use Text to RegEx, you must have the following licenses active in your ServiceNow instance:

|License|Requirement|
|-------|-----------|
|Vault license|Required. The core Vault product must be licensed.|
|Any Pro Plus SKU|Required. Your instance must have at least one Pro Plus subscription active. The Pro Plus SKU enables access to advanced AI and automation capabilities.|

## Required plugins

In addition to licenses, the following plugin must be installed and activated:

|Plugin|Requirement|
|------|-----------|
|Now Assist for Vault|Required. The Now Assist for Vault plugin must be installed and activated in your instance. This plugin serves as the container for Vault AI skills, including Text to RegEx. Installation of this plugin also performs a license check to verify you have both the Vault license and a Pro Plus SKU.|

## License check behavior

When you attempt to use Text to RegEx, the system checks whether your instance meets the licensing requirements. If the required licenses are not active or the required plugin is not installed:

-   The Generate Regex button appears grayed out \(disabled\)
-   When you hover over the button, a tooltip message informs you that the feature requires an additional license
-   The message directs you to contact your procurement team to purchase the required licenses or plugins

## Assists balance consumption

Each time you use Text to RegEx to generate and accept a regular expression, credits are consumed from your organization's Assists balance. Credits are deducted at the moment you click Accept to save the generated regex. Monitor your Assists balance regularly, especially if your team uses Text to RegEx frequently, to ensure you do not exhaust your available credits.

## Important constraint

Customers with only a Data Privacy standalone license will not have access to Text to RegEx. You must have both Vault license and a Pro Plus SKU. Data Privacy alone is insufficient.

## What to do if you don't have the required licenses

If Text to RegEx is not available in your instance:

1.  Contact your ServiceNow administrator to verify your licenses and confirm Now Assist for Vault is installed
2.  If licenses are missing, work with your procurement team to purchase a Vault license and a Pro Plus SKU
3.  Once licenses are active and the Now Assist for Vault plugin is installed, Text to RegEx becomes available

