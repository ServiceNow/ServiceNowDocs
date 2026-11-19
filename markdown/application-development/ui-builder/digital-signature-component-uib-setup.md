---
title: Digital Signature component setup
description: The Digital Signature component requires users to sign documents digitally to agree to terms in the document.Provide the terms and conditions that the user agrees to with their signature. Configure the Digital Signature properties and reusability preference.Select event handlers to configure the actions \(events\) provided with the Digital Signature component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/digital-signature-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Digital Signature component setup

The Digital Signature component requires users to sign documents digitally to agree to terms in the document.

## Before you begin

Verify that your instance has the Digital Signature API \(com.glide.digital\_signature\_api\) plugin. This plugin is active by default. This plugin includes a data resource that page authors can call to process the signature event and either generate a new document or only save the signature.

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Digital Signature that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "digital-signature-label.png"\] Alt text: Digital signature component in tree.

2.  Select the Digital Signature component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Digital Signature label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Digital signature component properties

Provide the terms and conditions that the user agrees to with their signature. Configure the Digital Signature properties and reusability preference.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_mdl_zpd_xrb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agreement text\[agreementText\]

</td><td>

The terms and conditions that the user agrees to with their signature. You can use a data binding to reference a reusable agreement text, such as `@context.props.documentDetail.acknowledgementText`.Default: I agree to terms and conditions.

</td></tr><tr><td>

Legal text\[legalText\]

</td><td>

The legal status of the digital signature.Default: This constitutes your electronic signature and is the same as signing a printed document.

</td></tr><tr><td>

Hide save signature option\[hideSaveSignature\]

</td><td>

When true, hides the check box for saving the user's signature for future use.

</td></tr><tr><td>

Save signature checked\[saveSignatureChecked\]

</td><td>

When true, the check box for saving the user's signature is checked automatically, and the user's signature is saved for future use.This property is not available when **Hide save signature option** is true.

</td></tr><tr><td>

Typed signature\[typedSignature\]

</td><td>

A typed name that serves as the digital signature.A user provides either a typed signature or a drawn signature, not both.

</td></tr><tr><td>

Drawn signature\[drawnSignature\]

</td><td>

A drawn signature of the user. The user provides either a typed signature or a drawn signature but not both.

</td></tr><tr><td>

Submit button label\[submitBtnLabel\]

</td><td>

Label for the **Submit** button.Default: Submit

</td></tr><tr><td>

Hide secondary action button\[hideSecondaryAction\]

</td><td>

If there is no secondary action, this option hides the secondary action button.Default: True

</td></tr><tr><td>

Secondary button label\[secondaryBtnLabel\]

</td><td>

The label for the secondary action button, if one exists. This property is not available when **Hide secondary action button** is true.

</td></tr><tr><td>

Hide submit button\[hideSubmitButton\]

</td><td>

When true, hides the submit button.Default: False

</td></tr></tbody>
</table>## Digital signature component events

Select event handlers to configure the actions \(events\) provided with the Digital Signature component.

The Events tab shows the events used by the Digital Signature component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Digital Signature actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_ev2_15d_xrb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Submit button clicked

</td><td>

User activates the button to generate a digital signature for the document. Payload:

-   The agreement text, `agreementText`
-   Whether the signature is typed or drawn, `tabFocused`
-   The signature data \(typed or drawn\), `signature`
-   The signature image \(typed or drawn\), `encodedSignature`
-   Whether to store the signature for reuse, `saveSignatureChecked`

 Event handler: Client script that passes the payload and any relevant Digital Signature API calls

</td></tr><tr><td>

Secondary button clicked

</td><td>

\(Optional\) User activates the button to do something other than sign the document. For example, you can provide a **Cancel** button if the user does not want to accept the agreement.Event handler: Client script

</td></tr><tr><td>

Digital signature updated

</td><td>

User finishes updating their digital signature.Payload:

-   The agreement text, `agreementText`
-   Whether the user has agreed to the agreement text, `agreementTextChecked`
-   Whether the signature is typed or drawn, `tabFocused`
-   The signature data \(typed or drawn\), `signature`
-   The signature image \(typed or drawn\), `encodedSignature`
-   Whether to store the signature for reuse, `saveSignatureChecked`

</td></tr></tbody>
</table>### HR Agent Workspace digital signature

If you are using Case and Knowledge Management, you likely have the HR Agent Workspace. This Workspace Experience includes a Digital Signature component. For information about how this component is used in runtime, see E-signature in HR Service Delivery Agent Workspace. In this example, you see the component's event handlers.

The Digital Signature component and data resource don't dictate where the data for the document comes from, or even if there is a document. Therefore, the creators of the workspace added a data resource on the digital signature page's parent page. The data resource fetches details of the document to be signed and passes them down in a **documentDetail** property. You need to create an equivalent solution for your own data.

The **documentDetail** property is added to the page configuration. The page also has the required `table` and `sysId` parameters. You can see this property and these parameters in the client script that serves as the **Submit** button clicked event handler:

```
/**
 * @param {params} params
 * @param {api} params.api
 * @param {any} params.event
 * @param {any} params.imports
 * @param {ApiHelpers} params.helpers
 */
function handler({
    api,
    event,
    helpers,
    imports
}) {
    const input = {};

    input.targetTable = api.context.props.table;
    input.targetSysId = api.context.props.sysId;
    input.tabFocused = event.payload.tabFocused;
    input.signature = event.payload.signature;
    input.encodedSignature = event.payload.encodedSignature;
    input.saveSignature = true;

    const documentDetail = api.context.props.documentDetail;
    input.type = documentDetail.documentType;
    input.agreementText = documentDetail.acknowledgmentText;
    input.operation = input.targetTable == 'sn_hr_core_task' ? 'eSign' : 'signatureImage';

    if (input.type == 'html') {
        input.html = api.state.documentTemplate;
        const draftDoc = {
            'table': input.targetTable,
            'sysId': input.targetSysId,
            'html': input.html,
            'saveSignature': input.saveSignature
        };
        api.data.generate_html_draft_document.execute(draftDoc);
    }

    api.data.save_user_signature.execute(input);
}
```

