---
title: Email Composer component setup
description: The Email Composer component enables requestors and fulfillers to use email to communicate. The component is associated with a record to include conversations as part of the record.Configure the tables and properties for your Email Composer component.Select event handlers to configure the actions \(events\) provided with the Email Composer component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/email-composer-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Email Composer component setup

The Email Composer component enables requestors and fulfillers to use email to communicate. The component is associated with a record to include conversations as part of the record.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Email Composer that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "email-composer-content-tree.png"\] Alt text: Email Composer content tree.

2.  Select the Email Composer component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Email Composer label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Email Composer component properties

Configure the tables and properties for your Email Composer component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_y5l_mvl_4nb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sys ID\[sysID\]

</td><td>

Unique identifier of the sys\_email\_draft record to fetch. Use -1 to create a new record.

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

The reply type for a response message. The possible types are: **Reply**, **Reply all** or **Forward**.

</td></tr><tr><td>

Email record ID\[replyId\]

</td><td>

Unique identifier of the sys\_email record for a response message

</td></tr><tr><td>

Show minified composer\[isCompact\]

</td><td>

Type of email composer to load. Loads either the full composer or the mini composer \(compact\). When true, the mini composer loads.Default: **false**

</td></tr><tr><td>

Show email details\[showEmailDetails\]

</td><td>

Toggle to display or hide the email details, including the **To**, **Cc** and **Bcc** fields. Default: **false**

</td></tr><tr><td>

Enable horizontal layout\[forceHorizontalLayout\]

</td><td>

Displays the field labels horizontally. For use with Modeless dialog only.Default: **false**

</td></tr><tr><td>

Template details\[templateDetails\]

</td><td>

Details of the template to be applied.

</td></tr><tr><td>

Allow email creation\[showCreateNewEmail\]

</td><td>

Displays the **Create new email** button.Default: **true**

</td></tr><tr><td>

Allow discarding\[showDiscardDraft\]

</td><td>

Displays the **Discard draft** button.Default: **true**

</td></tr><tr><td>

Link details\[insertLinkInEmail\]

</td><td>

Link details to add in the email. Inserts the message in the last active cursor position.

</td></tr><tr><td>

Allow managing drafts\[showViewDrafts\]

</td><td>

Displays the **Manage drafts** button.Default: **true**

</td></tr><tr><td>

Allow attachments\[showAttachments\]

</td><td>

Displays the **Attach files** button.Default: **true**

</td></tr><tr><td>

Send email button variant\[sendEmailButtonVariant\]

</td><td>

Sets the style variant for the **Send email** button. Options are primary, secondary, and tertiary.Default: **primary**

</td></tr><tr><td>

Fix resizable pane\[sidebarDisabled\]

</td><td>

Prevents the user from resizing the sidebar panes by moving the divider.Default: **false**

</td></tr><tr><td>

Enable mentioning users\[enableMentioningUsers\]

</td><td>

Enable user mentions in the email compose area.Default: **true**

</td></tr><tr><td>

Column layout property value\[columnLayout\]

</td><td>

Sets the column layout value of the connected component.

</td></tr><tr><td>

Initiate send email \[initiateSendEmail\]

</td><td>

Triggers the send action.Default: **false**

</td></tr><tr><td>

Default divider position\[sidebarDefaultDividerPosition\]

</td><td>

Sets the default location of the sidebar divider using a number between 0 and 100. To place the divider all the way to the left, enter 0. To place the divider all the way to the right, enter 100. To place the divider exactly in the middle of the panes, enter 50.

</td></tr><tr><td>

Pane minimum width\[sidebarRightPaneConstraints\]

</td><td>

Sets the minimum width of the right pane of the sidebar. You can set this value as a range of 0 to 100 and/or as a number of pixels. Enter a JSON string in the format `{minRatio:number, minPixels:number}`.

</td></tr><tr><td>

Pane-sidebar ratio\[sidebarRatioPreference\]

</td><td>

Sets the user preference for the ratio of sidebar inside the right pane of the resizable panes. When set, this ratio is used every time that user access the email composer.

</td></tr><tr><td>

Hide Send Button\[hideSend\]

</td><td>

Hides the **Send email** button.Default: **false**

</td></tr><tr><td>

Load latest draft \[loadLatestDraft\]

</td><td>

Loads the latest saved draft or sys\_email\_draft record.Default: **false**

</td></tr></tbody>
</table>## Email Composer component events

Select event handlers to configure the actions \(events\) provided with the Email Composer component.

The Events tab shows the events used by the Email Composer component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Email Composer actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_bkk_3xl_4nb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email InitialisedDRAFT\_INITIALISED

</td><td>

An email record is initializedPayload:

-   table: Table name
-   sys\_id: Sys ID of the record
-   subject: Subject of the email

</td></tr><tr><td>

Email draft modifiedDRAFT\_MODIFIED

</td><td>

User modifies an email draftPayload:

-   table: Table name
-   sys\_id: Sys ID of the record

</td></tr><tr><td>

Email savedDRAFT\_SAVE\_SUCCEEDED

</td><td>

User selects the Save buttonPayload:

-   table: Table name
-   sys\_id: Sys ID of the record

</td></tr><tr><td>

Email sentDRAFT\_SEND\_SUCCEEDED

</td><td>

User selects the Send buttonPayload:

-   table: Table name
-   sys\_id: Sys ID of the record

</td></tr><tr><td>

Email record status changedRECORD\_STATUS\_CHANGED

</td><td>

Status of an email record changesPayload:

-   table: Table name
-   sys\_id: Sys ID of the record
-   status: Record status \(Default: inserted\)

</td></tr><tr><td>

Email tab header updateFORM\_UPDATE\_HEADER

</td><td>

Updates the value of the email tab headerPayload:

-   table: Table name
-   sys\_id: Sys ID of the record
-   recordDisplayValue: Tab header displa value

</td></tr><tr><td>

Email tab updateUPDATE\_ONE\_TAB

</td><td>

Closes out the workspace email tab-   type: Type of action \(Default: UPDATE\_ONE\_TAB\_CLOSE\)
-   tab\_id: Workspace tab ID of the record

</td></tr><tr><td>

Resizable pane size changedRESIZABLE\_PANES\_SIZE\_CHANGED

</td><td>

Sets the sidebar ratio when the user changes the pane size-   sidebarRatio: Ratio of the sidebar panes
-   sidebarRatioPreference: User's preference for the ratio of the sidebar panes

</td></tr><tr><td>

Email subject changedEMAIL\_SUBJECT\_CHANGED

</td><td>

Dispatch event when email subject changedsubject: Subject value for email record

</td></tr></tbody>
</table>