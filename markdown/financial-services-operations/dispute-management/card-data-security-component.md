---
title: Card Data Security container
description: The Card Data Security container enables secure handling of Payment Card Information \(PCI\) card data within Financial Services Operations card dispute workflows through integration with a tokenizer service. This allows users to work with sensitive card information without exposing PCI data directly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/card-data-security-component.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [card data security container, pci card data, tokenizer service integration, card number reveal, reveal pan, mask pan, primary account number, pan, dispute workspace, ui builder component, payment card information, fso card number reveal viewport pages]
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Card Data Security container

The Card Data Security container enables secure handling of Payment Card Information \(PCI\) card data within Financial Services Operations card dispute workflows through integration with a tokenizer service. This allows users to work with sensitive card information without exposing PCI data directly.

**Note:** Card Data Security container requires context-aware authorization to function correctly. See [Set up OAuth for Card Data Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-oauth-for-card-data-security.md) for more information.

## Key capabilities

This component offers the following capabilities:

-   Secure card number display within the ServiceNow interface via integration with the tokenizer service \(preconfigured in Card Data Security\)
-   Secure viewing and download of documents stored in the tokenizer service containing PCI data \(preconfigured in Card Data Security\)
-   Secure card number input through an embedded iframe interface
-   Document upload functionality for files containing PCI data
-   Configurable features through UI Builder properties

## Implementing and modifying the component

This component displays within UI Builder views.

Two capabilities are preconfigured in Card Data Security: a card number reveal component and a secure attachment viewer. Use UI Builder to make changes to the preconfigured Card Data Security components.

You may also use UI Builder to implement features in the Card Data Security container that aren't preconfigured in Card Data Security, such as card number input and document upload.

For more information about this component's configuration options and adding it to a workspace, see the following resources:

-   [Component developer documentation for Card Data Security](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/sn-card-data-security-container/overview)
-   [UI Builder setup documentation for Card Data Security](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/sn-card-data-security-container/uib-setup)
-   [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-components.md)

## Card Number Reveal Component

After installing Card Data Security, the card dispute workflow includes this component as a preconfigured card number reveal component. This component is in the transaction record and the Card details section of the Dispute Workspace.

In the transaction record page, the value is derived from the PAN field of the payment card linked to the transaction.

In the dispute workspace, the value is the payment card's tokenized PAN from the disputed financial transaction.

**Note:** The tokenized PAN value from the tokenizer service is stored in the payment card record's PAN field. When you select the show icon, the card number reveal component detokenizes and displays the original PAN. When you select the hide icon, it restores the redacted value.

\[Omitted image "card-data-security-card-details.png"\] Alt text: Dispute Workspace showing Card details section with masked card number field.

\[Omitted image "card-data-security-card-details-txn.png"\] Alt text: Transaction details form showing card number reveal component in card details section.

This component is a UI Builder page collection called **FSO Card Number Reveal Viewport Pages**.

Use UI Builder to move this component elsewhere as required.

1.  Add a viewport to your desired page.
2.  Add the **FSO Card Number Reveal Viewport Pages** page collection to the viewport.
3.  Create a Viewport load request and define the following values:

<table id="table_g4p_fvv_33c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Viewport

</td><td>

Card Number Reveal Viewport

</td></tr><tr><td>

Viewport Route

</td><td>

&lt;The viewport variant you want to use - select the design from the dispute workspace or the record page form&gt;

</td></tr><tr><td>

Viewport Fields

</td><td>

&lt;The paymentCardSysId value.&gt;**Note:** This value is required for the component to function.

</td></tr></tbody>
</table>
Refer to the related links for more information.

## Displaying and downloading secure attachments

After installing Card Data Security, the Attachments view in the contextual side panel displays attachments differently at the transaction level. It displays two preconfigured tabs:

-   **Issuer**, which shows files added by the dispute agent.
-   **Merchant**, which shows files received from the card network, acquirer, or merchant, stored in the tokenizer service vault.

For more information, see [Manage attachments in Card Data Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/manage-attachments-in-card-data-security.md).

**Related topics**  


[UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md)

[Page collections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/page-collections.md)

[Extend your UI experience with viewport components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/viewports-overview.md)

