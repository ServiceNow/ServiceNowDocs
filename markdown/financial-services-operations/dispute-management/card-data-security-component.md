---
title: Card Data Security container
description: The Card Data Security container enables secure handling of Payment Card Information \(PCI\) card data within Financial Services Operations card dispute workflows through integration with a tokenizer service. This allows users to work with sensitive card information without exposing PCI data directly.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Card Data Security container

The Card Data Security container enables secure handling of Payment Card Information \(PCI\) card data within Financial Services Operations card dispute workflows through integration with a tokenizer service. This allows users to work with sensitive card information without exposing PCI data directly.

**Note:** Card Data Security container requires context-aware authorization to function correctly. See [Set up OAuth for Card Data Security](set-up-oauth-for-card-data-security.md) for more information.

## Key capabilities

This component offers the following capabilities:

-   Secure card number display within the ServiceNow interface via integration with the tokenizer service
-   Secure card number input through an embedded iframe interface
-   Document upload functionality for files containing PCI data
-   Secure viewing of uploaded documents containing PCI data
-   Configurable features through UI Builder properties

## Card Number Reveal Component

After installing Card Data Security, the card dispute workflow includes this component as a card number reveal component. This component is in the transaction record and the Card details section of the Dispute Workspace.

In the transaction record page, the value is derived from the PAN field of the payment card linked to the transaction.

In the dispute workspace, the value is the payment card's tokenized PAN from the disputed financial transaction.

**Note:** The tokenized PAN value from the tokenizer service is stored in the payment card record's PAN field. When you select the show icon, the card number reveal component detokenizes and displays the original PAN. When you select the hide icon, it restores the redacted value.

![Dispute Workspace showing Card details section with masked card number field.](../image/card-data-security-card-details.png "Card number reveal component in Dispute Workspace")

![Transaction details form showing card number reveal component in card details section.](../image/card-data-security-card-details-txn.png "Card number reveal component in Transaction record")

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

## Implementing and modifying the component

This component displays within UI Builder views. To make changes to the preconfigured Card Data Security components, use UI Builder.

For more information about adding this component to a workspace, see the following resources:

-   [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-components.md)
-   [Components documentation for Card Data Security](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/sn-card-data-security-container/overview)
-   [UI Builder setup documentation for Card Data Security](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/sn-card-data-security-container/uib-setup)

**Related topics**  


[UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md)

[Page collections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/page-collections.md)

[Extend your UI experience with viewport components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/viewports-overview.md)

