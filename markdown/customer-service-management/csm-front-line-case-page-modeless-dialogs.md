---
title: Modeless dialogs
description: Use modeless dialogs, windows that overlay the main window content, to create and post comments and work notes to the activity stream and to compose and send emails.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-11-05"
reading_time_minutes: 11
breadcrumb: [Front-line case page, CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Modeless dialogs

Use modeless dialogs, windows that overlay the main window content, to create and post comments and work notes to the activity stream and to compose and send emails.

A modeless dialog is a window that appears in a workspace as an overlay on top of the main window content. This overlay enables users to interact with the window content and the overlay content at the same time. Agents can use modeless dialogs to do the following:

-   Create comments and work notes to post to the activity stream.
-   Create and send emails and reply to or forward emails.

After opening a modeless dialog, agents can move it around the screen and put it where they need it. This feature enables agents to reference information from the main window while drafting text in the overlay window.

The Front-line case page includes the following modeless dialogs:

-   Compose Activity - for creating and posting comments and work notes
-   Compose Email - for creating and sending emails

## Create comments and work notes

Agents can use the Compose Activity modeless dialog to create comments and work notes and post them to the activity stream. See the following table for more information about creating these activities.

**Note:** This feature is available with the Front-line case page in CSM Configurable Workspace.

<table id="table_ikh_tsd_w1c"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create a comment or work note

</td><td>

To create a comment or a work note:1.  Select one of the following actions from the action bar to open a Compose window:
    -   **Compose** &gt; **Compose Comments**
    -   **Compose** &gt; **Compose Work notes \(Private\)**
2.  Add the text to the Compose window.

When creating comments and work notes:

-   Agents can create one draft comment and one draft work note at a time before posting the text to the activity stream.
-   Agents can open one Compose window at a time. If an agent opens a second window, the previously opened window is minimized.

</td></tr><tr><td>

Post a comment or work note to the activity stream

</td><td>

To post a comment or work note, select one of the following actions from the Compose window:-   **Post Comment**
-   **Post Work Notes \(Private\)**

The Compose window automatically closes after the text is posted to the activity stream.

Saving the case record also posts the comment or work note to the activity stream and closes the Compose window.

</td></tr><tr><td>

Minimize a Compose window

</td><td>

Composed windows can be minimized and moved to the In-process Actions menu in the action bar. Minimized comments and work notes appear in a list in the In-process Actions menu. Compose windows can be minimized in the following ways.

-   Select the Minimize button in the Compose window header.
-   One Compose window can be open at a time. If an agent opens another Compose window, the first window is minimized.

</td></tr><tr><td>

Open a minimized Compose window

</td><td>

Select the In-progress Actions menu in the action bar and then select an item from the list to open the window.Items in the In-process Actions menu appear in a list with the action type \(email, comment, or work note\) and an abbreviated title.

-   For email, the title is the email subject.
-   For comments and work notes, the title is the first line of text.

</td></tr><tr><td>

Discard a comment or work note

</td><td>

To discard a comment or work note:1.  Select the Close button in the Compose window header.
2.  Confirm the Discard action by selecting **Discard** in the confirmation pop-up window.

The system closes the Compose window and discards the comment or work note.

</td></tr></tbody>
</table>The following guidelines apply to Compose windows:

-   Draft comments and work notes are local to the browser and are cleared if the browser page is reloaded.
-   Comments and work notes stay in sync on the form and in the modeless dialogs.
-   The Compose window has a fixed size.

## Create emails

Agents can use the Compose Email modeless dialog to create and save email drafts and to send emails. This feature increases the speed of drafting emails while referencing record information.

Emails that are sent from a Compose Email window are posted to the activity stream. Agents can reply to and forward emails from the activity stream. See the following table for more information about creating and sending emails.

**Note:** This feature is available with the Front-line case page in CSM Configurable Workspace.

<table id="table_bmb_hzd_w1c"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create and send an email

</td><td>

To create and send an email:1.  Select **Compose** &gt; **Compose Email** from the action bar to open a Compose Email window.
2.  Fill out the fields:
    1.  To, Cc, Bcc
    2.  Subject
    3.  Email body
3.  Select **Send email**.

When creating emails and sending emails:

-   The Compose Email window automatically closes after the email is sent.
-   The email is posted to the activity stream.

</td></tr><tr><td>

Reply to or forward an email

</td><td>

To reply to or forward an email:1.  Expand an email in the activity stream.
2.  Select one of the following buttons to open the Compose Email window:
    -   **Reply**
    -   **Reply all**
    -   **Forward**
3.  Add the desired text.
4.  Select **Send email**.

The Compose Email window automatically closes after the email is posted to the activity stream.

</td></tr><tr><td>

Add a link to a knowledge article

</td><td>

To add a link to a knowledge article:1.  Select the Agent Assist tab in the contextual side panel.
2.  View the list of knowledge articles or search for an article.
3.  Select the More Actions menu on the knowledge article card.
4.  Select **Add link in email**.

The system adds the title of the article with a link in the body of the email.

</td></tr><tr><td>

Apply a template to an email

</td><td>

To apply a template to an email:

1.  Select the Apply templates icon \(![Compose email apply templates icon](../image/csm-email-modeless-dialog-apply-template.png)\) in the Compose email modeless dialog footer to display a list of available templates in the Template preview modal.

The Template preview modal displays the available email templates. It does not display quick messages or response templates.

2.  Select a template from the list. You can also search for a specific template.

The system adds the contents of the template to the body of the email.

**Note:** If no templates are available, the icon does not appear in the footer.

</td></tr><tr><td>

Minimize a Compose Email window

</td><td>

Minimized emails appear in a list in the In-process Actions menu in the action bar.Select the Minimize icon \(![Compose email minimize icon](../image/csm-email-modeless-dialog-minimize.png)\) in the Compose Email window header to move the email draft to the In-progress Actions menu.

</td></tr><tr><td>

Open a minimized Compose Email window

</td><td>

Select an item from the In-progress Actions menu to open the Compose Email window.Items in the In-process Actions menu appear in a list with the action type \(email, comment, or work note\) and an abbreviated title.

-   For email, the title is the email subject.
-   For comments and work notes, the title is the first line of text.

</td></tr><tr><td>

Maximize a Compose Email window

</td><td>

Select the Maximize icon \(![Compose email maximize icon](../image/csm-email-modeless-dialog-maximize.png)\) in the Compose Email window header to expand the Compose Email window to the full screen.Select the Maximize icon again to exit the Maximize mode.

</td></tr><tr><td>

Open a draft email in a sub-tab

</td><td>

Select the Pop out icon \(![Compose email pop out icon](../image/csm-email-modeless-dialog-pop-out.png)\) in the Compose Email window header to open the draft email in a sub-tab.The Compose Email window closes when the email opens in the sub-tab.

</td></tr><tr><td>

Close a Compose Email window

</td><td>

Select the Close icon \(![Compose email close icon](../image/csm-email-modeless-dialog-close.png)\) in the Compose Email window header.The system saves the text as a draft email and closes the Compose Email window.

</td></tr><tr><td>

View a list of draft emails

</td><td>

Select the View drafts icon \(![Compose email view drafts icon](../image/csm-email-modeless-dialog-view-drafts.png)\) in the Compose Email window footer. Selecting this icon displays a list that includes the most recent email drafts. The list also includes the following actions:

-   **Manage drafts**: Displays the Manage drafts pop-up window. From this window, you can view a list of all draft emails. You can also delete email drafts from this window.
-   **Create new email**: creates a new email in the Compose email window.

</td></tr><tr><td>

Select an email draft

</td><td>

Select the View drafts icon \(![Compose email view drafts icon](../image/csm-email-modeless-dialog-view-drafts.png)\) in the Compose Email window footer. Selecting this icon displays a list that includes the most recent email drafts. You can select a recent draft from this list.

 To view a list of all email drafts:

1.  Select the View drafts icon and then select **Manage drafts**.
2.  Select a draft from the list in the Manage drafts pop-up window.

The system saves the current draft email and opens the selected draft email in the Compose Email window.

</td></tr><tr><td>

Select an email draft from the Draft Emails related list

</td><td>

1.  Select the Related Lists tab in the contextual side panel.
2.  Expand the Draft Emails related list.
3.  Select the Open draft icon on the desired draft email card.

The system opens the selected draft email in a sub-tab.

</td></tr><tr><td>

Discard the current draft email

</td><td>

1.  Select the Discard draft icon \(![Compose email discard draft icon](../image/csm-email-modeless-dialog-discard-draft.png)\) in the Compose Email window footer.
2.  Confirm the Discard action by selecting **Discard** in the confirmation pop-up window.

The system displays a message that the draft email has been discarded.

</td></tr><tr><td>

Delete an email draft from the Manage drafts pop-up window

</td><td>

1.  Select the View drafts icon \(![Compose email view drafts icon](../image/csm-email-modeless-dialog-view-drafts.png)\) in the Compose Email window footer.
2.  Select **Manage drafts** to display the Manage drafts pop-up window.
3.  Select an email to delete by enabling the check box.
4.  Select **Delete** in the pop-up window.
5.  Confirm the action by selecting **Delete** again.

</td></tr></tbody>
</table>The following guidelines apply to the Compose Email window:

-   An agent can create multiple email drafts.
-   An agent can have one Compose Email window open at a time. The system displays a message if an agent tries to open another Compose Email window while the first Compose Email window is still open.
-   An agent has to manually close a Compose Email window before opening a new window.
-   The Compose Email window can be resized.

## Collapsing and expanding the email header

The email header includes the following fields:

-   **To**
-   **Cc**
-   **Bcc**
-   **Subject**

You can expand and collapse the email header as needed by selecting the expand header \(![Compose email expand header icon](../image/csm-email-modeless-dialog-header-expand.png)\) and collapse header \(![Compose email collapse header icon](../image/csm-email-modeless-dialog-header-collapse.png)\) icons.

When the email header is expanded, you can edit the information in these fields. When the email header is collapsed:

-   The names in the **To**, **Cc**, and **Bcc** fields are combined into one line. If there is a long list of recipients, some of the names are replaced with "and more".
-   The subject is displayed in a second line.
-   The fields are not editable.

When you create a new email or forward an email, the header is expanded by default and displays the **To** and **Subject** fields. If you expand the **Cc** and **Bcc** fields, the collapse header icon is displayed.

When you reply to an email, the header is collapsed by default. Expanding the header shows all of the fields that contain information.

## Compose Email modeless dialog footer icons

Several icons appear in the Compose Email modeless dialog footer that you can use when creating email drafts.

<table id="table_mdf_gwj_4bc"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Discard draft \(![Compose email discard draft icon](../image/csm-email-modeless-dialog-discard-draft.png)\)

</td><td>

Select this icon to delete the current draft. Then confirm the delete action in the resulting confirmation message.

</td></tr><tr><td>

Apply template \(![Compose email apply templates icon](../image/csm-email-modeless-dialog-apply-template.png)\)

</td><td>

Select this icon to display a list of available templates. You can select a template from the list or search for a specific template. The list can display up to 10 templates. Selecting a template applies that template to the draft email.**Note:** If no templates are available, the icon does not appear in the footer.

</td></tr><tr><td>

View drafts \(![Compose email view drafts icon](../image/csm-email-modeless-dialog-view-drafts.png)\)

</td><td>

Select this icon to display a list with recent draft emails as well as email-related actions.You can select an email draft from the list to display that draft in the Compose Email window.

Email-related actions include:

-   **Manage drafts**: Displays the Draft Management pop-up window which includes a list of email drafts. Select a draft to display the contents in the Compose Email window. You can also delete email drafts from this pop-up window.
-   **Create new email**: Creates a new email draft in the Compose Email window.

</td></tr><tr><td>

Attach file \(![Compose email attach file icon](../image/csm-email-modeless-dialog-attach-file.png)\)

</td><td>

Select this icon to attach files to an email draft **From computer** or **From record**. After attaching one or more files, you can hide or show the attachments.

</td></tr></tbody>
</table>## Auto loading the latest email draft

The Compose Email modeless dialog opens with the last saved email draft. When a user selects **Compose** &gt; **Compose Email**, the Compose Email modeless dialog opens and displays this latest draft. If there are no recent drafts for the current case, the system loads a new draft. This feature is enabled by default.

**Note:** This feature is controlled by component properties in UI Builder. These properties are located on the Configure tab in the Advanced section:

-   **Load latest draft**: When enabled, the system loads the latest email draft.
-   **sys ID**: Set this property to -1.

When the property is enabled and a specific sys\_id is passed to the email client, the system can load the particular email draft in the Email Compose modeless dialog.

