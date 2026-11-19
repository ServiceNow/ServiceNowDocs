---
title: Email Composer \(mini\) component setup
description: Email Composer \(mini\) renders the email composer in smaller spaces and within another component, such in a side panel on a record page. The mini component shows fewer details, but can be expanded to show the To, Cc, and Bcc fields.Configure the Email Composer \(mini\) component to display in a collapsed or expanded state when the page loads.Select event handlers to configure the actions \(events\) provided with the Email Composer \(mini\) component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/email-composer-mini-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Email Composer \(mini\) component setup

Email Composer \(mini\) renders the email composer in smaller spaces and within another component, such in a side panel on a record page. The mini component shows fewer details, but can be expanded to show the **To**, **Cc**, and **Bcc** fields.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

For instructions on overriding styles using the Styles pane, see [Change the default appearance of components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-styling-to-component.md).

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Email Composer \(mini\) that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "email-composer-mini-content-tree.png"\] Alt text: Shows the email composer mini component in the UI Builder content tree

2.  Select the Email Composer \(mini\) component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Email Composer \(mini\) label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Email Composer \(mini\) component properties

Configure the Email Composer \(mini\) component to display in a collapsed or expanded state when the page loads.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_zdn_dc2_2cc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sys ID\[sysId\]

</td><td>

Sys ID of the email\_draft record.

</td></tr><tr><td>

Target table\[targetTable\]

</td><td>

Name of target table for this record.

</td></tr><tr><td>

Target record\[targetRecord\]

</td><td>

Unique identifier of the associated record.

</td></tr><tr><td>

Response type\[replyType\]

</td><td>

The reply type if the email is a response draft. The possible types are: **Reply**, **reply all** or **Forward**.

</td></tr><tr><td>

Email record ID\[replyId\]

</td><td>

Unique identifier of the sys\_email record for a response message.

</td></tr><tr><td>

Show email details\[showEmailDetails\]

</td><td>

Toggle to display or hide email details, including the **To**, **Cc** and **Bcc** fields. Default: **false**

</td></tr><tr><td>

Enable horizontal layout\[forceHorizontalLayout\]

</td><td>

Displays the field labels horizontally. For use with Modeless dialog only.Default: **false**

</td></tr><tr><td>

Template details\[templateDetails\]

</td><td>

Details of the template to be applied.

</td></tr><tr><td>

Link details\[insertLinkInEmail\]

</td><td>

Link details to insert in email. Inserts message in the last active cursor position of email.

</td></tr><tr><td>

Allow pop out\[showPopOut\]

</td><td>

Displays the pop-out option.Default: **true**

</td></tr><tr><td>

Send email button variant\[sendEmailButtonVariant\]

</td><td>

Style variant for the **Send email** button. Default: **secondary**

</td></tr><tr><td>

Allow email creation\[showCreateNewEmail\]

</td><td>

Displays the **Create new email** button.Default: **true**

</td></tr><tr><td>

Allow discarding\[showDiscardDraft\]

</td><td>

Displays the **Discard draft** button.Default: **true**

</td></tr><tr><td>

Allow managing drafts\[showViewDrafts\]

</td><td>

Displays the **Manage drafts** button.Default: **true**

</td></tr><tr><td>

Allow attachments \[showAttachments\]

</td><td>

Displays the **Attach files** button.

</td></tr><tr><td>

Show recent drafts \[showRecentDrafts\]

</td><td>

Displays the **Recent drafts** button.

</td></tr><tr><td>

Show email templates \[showEmailTemplates\]

</td><td>

Displays the **Email templates** button.

</td></tr><tr><td>

Fit to parent\[fitToParent\]

</td><td>

Fits email client to its parent height.Default: **false**

</td></tr><tr><td>

Enable mentioning users\[enableMentioningUsers\]

</td><td>

Enable user mentions in the email compose area.Default: **true**

</td></tr><tr><td>

Icon\[popoutIcon\]

</td><td>

Defines the icon for the popout button.

</td></tr><tr><td>

Extra params\[extraParams\]

</td><td>

Passes URL extra param values to email client to decode.

</td></tr><tr><td>

Hide Send Button\[hideSend\]

</td><td>

Hides the **Send email** button.Default: **false**

</td></tr><tr><td>

Load latest draft\[loadLatestDraft\]

</td><td>

Loads the latest saved draft or sys\_email\_draft record.Default: **false**

</td></tr><tr><td>

Suppress global events\[suppressGlobalEvents\]

</td><td>

Suppresses events that rely on parent elements handling and only dispatches events that are manually binded.

</td></tr></tbody>
</table>## Email Composer \(mini\) component events

Select event handlers to configure the actions \(events\) provided with the Email Composer \(mini\) component.

The Events tab shows the events used by the Email Composer \(mini\) component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Email Composer \(mini\) actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_f3d_jlj_ktb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email initialisedDRAFT\_INITIALISED

</td><td>

An email draft has been rendered and initialized.Payload:

-   table: Table name
-   sys\_id: Sys ID of the record
-   subject: Subject of the email

</td></tr><tr><td>

Email draft modifiedDRAFT\_MODIFIED

</td><td>

User modifies an email draft.Payload:

-   table: Table name
-   sys\_id: Sys ID of the record

</td></tr><tr><td>

Email savedDRAFT\_SAVE\_SUCCEEDED

</td><td>

User selects the Save button.Payload:

-   table: Table name
-   sys\_id: Sys ID of the record

</td></tr><tr><td>

Email popped outEMAIL\_CLIENT\_POP\_OUT\_BUTTON\_CLICKED

</td><td>

The user has selected the popout button and opened the email in another workspace tab.

</td></tr><tr><td>

Email sentDRAFT\_SEND\_SUCCEEDED

</td><td>

User selects the Send buttonPayload:

-   table: Table name
-   sys\_id: Sys ID of the record

</td></tr><tr><td>

Email attachment addedATTACHMENTS\_ADDED

</td><td>

The user adds attachments to the email for the first time.

</td></tr><tr><td>

Preview RecordPREVIEW\_RECORD

</td><td>

The user selects the popout control and the email is saved successfully.Payload:

-   table: Table name
-   sys\_id: Sys ID of the record

</td></tr><tr><td>

Email subject modifiedEMAIL\_SUBJECT\_CHANGED

</td><td>

Dispatch event when email subject changedPayload:

subject: Subject value for email record

</td></tr></tbody>
</table>