---
title: Components installed with Financial Services Operations Integration with Visa
description: Reference topics provide additional information on the installed components and subflows that you use to configure and administer Financial Services Operations Integration with Visa application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Visa, Integrate, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Operations Integration with Visa

Reference topics provide additional information on the installed components and subflows that you use to configure and administer Financial Services Operations Integration with Visa application.

**Important:** Set the `sn_bom_credit_card.is_visa_integration_enabled` property to `True` to enable Financial Services Operations Integration with Visa. By default, this property is set to `False`, so you need to update it manually. Financial Services Operations Integration with Visa will not function until this property is enabled.

## Plugins installed

These plugins are installed with the Financial Services Operations Integration with Visa application \(com.sn\_fso\_intg\_visa\):

|Plugin|Description|
|------|-----------|
|Visa Spoke \[com.sn\_visa\_spoke\]|This application provides a list of actions to help users search for transactions, collaborate with merchants, manage disputes and perform other functions with enhanced security.|
|Dispute Rules Content Pack for Visa \[com.sn\_bom\_visa\_cp\]|This applications provides questionnaire for intake of dispute related information under various dispute categories as per Visa guidelines.|

-   **[Financial Services Operations Integration with Visa subflows](components-installed-with-the-financial-services-operations-integration-with-visa.md)**  
You can use the following Financial Services Operations Integration with Visa application subflows to handle the card dispute management process.

**Parent Topic:**[Financial Services Operations Integration with Visa reference](../concept/FSO-integration-with-visa-reference.md)

