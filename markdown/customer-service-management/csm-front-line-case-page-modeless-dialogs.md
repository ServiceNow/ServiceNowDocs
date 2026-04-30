---
title: Modeless dialogs
description: Modeless dialogs are windows that overlay the main window content in CSM Configurable Workspace. Customer service agents can use modeless dialogs to create and post comments and work notes to the activity stream and to compose and send emails.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Front-line case page, CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Modeless dialogs

Modeless dialogs are windows that overlay the main window content in CSM Configurable Workspace. Customer service agents can use modeless dialogs to create and post comments and work notes to the activity stream and to compose and send emails.

A modeless dialog is a window that appears in a workspace as an overlay on top of the main window content. This overlay enables agents to interact with the window content and the overlay content at the same time. Agents can use modeless dialogs to do the following:

-   Create comments and work notes to post to the activity stream.
-   Create and send emails and reply to or forward emails.

After opening a modeless dialog, agents can move it around the screen and put it where they need it. This feature enables agents to reference information from the main window while drafting text in the overlay window.

## Thin compose modeless dialogs

The thin compose modeless dialog feature incorporates modeless dialogs into the activity stream. It enables agents to initiate a comment, work note, or email in the activity stream and then open the text in a modeless dialog. Thin compose modeless dialogs:

-   Auto-expand to accommodate the text.
-   Can be manually resized.
-   Can be minimized after they're opened.
-   Have the rich text editor enabled even when the **glide.ui.journal.use\_html** system property is set to false.

Thin compose modeless dialogs are available on the following record pages:

-   [Front-line case page](csm-front-line-case-page.md)
-   [CSM default record page](csm-default-record-page.md)
-   [CSM Interaction record page](csm-interaction-record-page.md)
-   [CSM centered chat interaction record page](csm-centered-chat-interaction-page.md)
-   [CSM voice interaction record page](csm-native-voice-record-page.md)
-   [Email interaction record page](csm-email-interaction-record-page.md)

**Note:** The thin compose modeless dialog feature has the Rich Text Editor enabled, which can add HTML tags along with the text to the **Additional comments** and **Work notes** fields on the case record. To remove these tags, see [Updating the glide.ui.journal.use\_html property](csm-front-line-case-page-modeless-dialogs.md#section_jxd_1pl_1gc).

## Creating comments and work notes

Use modeless dialogs to create comments and work notes and post them to the activity stream.

<table id="table_ikh_tsd_w1c"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create a comment or work note

</td><td>

To create a comment or a work note:1.  Select one of the following tabs at the top of the activity stream:
    -   **Comments**
    -   **Work notes**
2.  Add the text to the Compose window.

</td></tr><tr><td>

Post a comment or work note to the activity stream

</td><td>

To post a comment or work note, select one of the following actions from the Compose window:-   **Post Comments**
-   **Post Work notes**

The system posts the comment or work note to the activity stream. Saving the case record also posts the comment or work note to the activity stream.

</td></tr><tr><td>

Open a comment or work note in a modeless dialog

</td><td>

Select the pop out \(![modeless dialog pop out icon which is a smaller solid square within a larger square](../image/modeless-dialog-pop-out-icon.png)\) icon to open a comment or work note in a modeless dialog.You can open a modeless dialog before or after you start entering text in the Compose window.

**Note:** You can have one modeless dialog of each type \(comments, work notes, and email\) open at a time.

</td></tr><tr><td>

Return a comment or work note to the Compose window

</td><td>

After opening a comment or work note in a modeless dialog, you can return the text to the Compose window in the activity stream in the following ways:-   Select the Continue editing in compose \(![square icon with down arrow](../image/modeless-dialog-continue-editing-icon.png)\) button at the top of the modeless dialog.
-   Select the **Pop in** link in the Compose window in the activity stream.

</td></tr><tr><td>

Minimize a modeless dialog

</td><td>

To minimize a modeless dialog, select the Minimize dialog \(![minimize icon is a flat white line at the bottom of a black box](../image/modeless-dialog-minimize-icon.png)\) button in the window header. Minimized modeless dialogs are added to the Minimize modeless dialogs \(![Minimize modeless dialogs icon n the action bar](../image/modeless-dialog-minimized-window.png)\) menu in the action bar and appear in a list in this menu.

</td></tr><tr><td>

Open a minimized modeless dialog

</td><td>

Select the Minimize modeless dialogs \(![minimize modeless dialogs menu](../image/modeless-dialog-minimized-window.png)\) menu in the action bar and then select an item from the list.Items in the Minimize modeless dialogs menu appear in a list with the action type \(email, comment, or work note\) and an abbreviated title.

</td></tr><tr><td>

Discard a comment or work note

</td><td>

To discard a comment or work note:1.  Select the Close dialog \(![close icon is a white X on a black background](../image/modeless-dialog-close-icon.png)\) button in the modeless dialog header.
2.  Confirm the Close Dialog action by selecting **Continue** in the confirmation pop-up window.

</td></tr></tbody>
</table>The following guidelines apply to Compose windows for comments and work notes:

-   Draft comments and work notes are local to the browser. If the browser page is reloaded, the draft text is cleared.
-   Comments and work notes stay synchronized on the form and in the modeless dialogs.
-   The Compose window can be resized.

## Creating emails

Use modeless dialogs to create and save email drafts and to send emails.

Emails that are sent from a modeless dialog are posted to the activity stream. Agents can reply to and forward emails from the activity stream.

<table id="table_bmb_hzd_w1c"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create and send an email

</td><td>

To create and send an email:1.  Select the **Email** tab at the top of the activity stream.
2.  Fill out the fields on the email form:
    1.  To, Cc, Bcc
    2.  Subject
    3.  Email body
3.  Select **Send email**.

When creating emails and sending emails:

-   The Compose window automatically closes after the email is sent.
-   The email is posted to the activity stream.

</td></tr><tr><td>

Open an email in a modeless dialog

</td><td>

Select the pop out \(![modeless dialog pop out icon which is a smaller solid square within a larger square](../image/modeless-dialog-pop-out-icon.png)\) icon to open an email in a modeless dialog.You can open a modeless dialog either before or after you start entering text in the Compose window.

**Note:** You can have one modeless dialog of each type \(comments, work notes, and email\) open at a time.

</td></tr><tr><td>

Return an email to the Compose window

</td><td>

After opening an email in a modeless dialog, you can return the email to the Compose window in the activity stream in the following ways:-   Select the Continue editing in compose \(![square icon with down arrow](../image/modeless-dialog-continue-editing-icon.png)\) button at the top of the modeless dialog.
-   Select the **Pop in** link in the Compose window in the activity stream.

</td></tr><tr><td>

Minimize a modeless dialog

</td><td>

To minimize a modeless dialog, select the Minimize dialog \(![minimize icon is a flat white line at the bottom of a black box](../image/modeless-dialog-minimize-icon.png)\) button in the window header. Minimized modeless dialogs are added to the Minimize modeless dialogs \(![minimize modeless dialogs menu icon](../image/modeless-dialog-minimized-window.png)\) menu in the action bar and appear in a list in this menu.

</td></tr><tr><td>

Open a minimized modeless dialog

</td><td>

Select the Minimize modeless dialogs \(![minimize modeless dialogs menu icon](../image/modeless-dialog-minimized-window.png)\) menu in the action bar and then select an item from the list.Items in the Minimize modeless dialogs menu appear in a list with the action type \(email, comment, or work note\) and an abbreviated title.

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

The Compose window automatically closes after the email is posted to the activity stream.

</td></tr><tr><td>

Add a link to a knowledge article

</td><td>

To add a link to a knowledge article:1.  Select the Recommended Actions tab in the contextual side panel.
2.  View the list of knowledge articles or search for an article.
3.  Select the More Actions menu on the knowledge article card.
4.  Select **Attach and add link in email**.

The system adds a link to the knowledge article in the body of the email.

</td></tr><tr><td>

Apply a template to an email

</td><td>

To apply a template to an email:

1.  Select the Apply templates icon \(![Compose email apply templates icon](../image/csm-email-modeless-dialog-apply-template.png)\) in the Compose email modeless dialog footer to display a list of available templates.

The Template preview modal displays the available email templates. It doesn't display quick messages or response templates.

2.  Select a template from the list. You can also search for a specific template.

The system adds the contents of the template to the body of the email.

**Note:** If no templates are available, the icon doesn't appear in the footer.

</td></tr><tr><td>

Open a draft email in a subtab

</td><td>

Select the Pop out icon \(![Compose email pop out icon](../image/csm-email-modeless-dialog-pop-out.png)\) in the Compose Email window header to open the draft email in a subtab.The Compose Email window closes when the email opens in the subtab.

</td></tr><tr><td>

View a list of draft emails

</td><td>

Select the View drafts icon \(![Compose email view drafts icon](../image/csm-email-modeless-dialog-view-drafts.png)\) in the Compose Email window footer. Selecting this icon displays a list that includes the most recent email drafts. The list also includes the following actions:

-   **Manage drafts**: Displays the Manage drafts pop-up window. From this window, you can view a list of all draft emails. You can also delete email drafts from this window.
-   **Create new email**: Creates a new email in the Compose email window.

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

The system opens the selected draft email in a subtab.

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
</table>The following guidelines apply to Compose windows for emails:

-   An agent can create multiple email drafts.
-   An agent can have one Compose window open at a time.
-   The Compose Email window can be resized.

## Collapsing and expanding the email header

The email header includes the following fields:

-   **To**
-   **Cc**
-   **Bcc**
-   **Subject**

You can expand and collapse the email header as needed by selecting the expand header \(![Compose email expand header icon](../image/csm-email-modeless-dialog-header-expand.png)\) and collapse header \(![Compose email collapse header icon](../image/csm-email-modeless-dialog-header-collapse.png)\) icons.

When the email header is expanded, you can edit the information in these fields. When the email header is collapsed:

-   The names in the **To**, **Cc**, and **Bcc** fields are combined into one line. If there's a long list of recipients, some of the names are replaced with "and more."
-   The subject is displayed in a second line.
-   The fields aren't editable.

When you create an email or forward an email, the header is expanded by default and displays the **To** and **Subject** fields. If you expand the **Cc** and **Bcc** fields, the collapse header icon is displayed.

When you reply to an email, the header is collapsed by default. Expanding the header shows all the fields that contain information.

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

Select this icon to display a list of available templates. You can select a template from the list or search for a specific template. The list can display up to 10 templates. Selecting a template applies that template to the draft email.**Note:** If no templates are available, the icon doesn’t appear in the footer.

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
</table>## Using form templates to create comments and work notes

You can create and use form templates that add content to the **Additional comments** and **Work notes** fields on a case record and then post that content to the activity stream.

<table id="table_s2l_pmb_s2c"><thead><tr><th>

Content to add

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Comment

</td><td>

If a template includes content to add to the **Additional comments** field on the case record, the system does the following:-   Displays a modeless dialog for composing a comment.
-   Adds the content to the **Comments** field in the modeless dialog.

Selecting **Post Comments** adds the content to the **Additional comments** field on the case record and to the activity stream.

</td></tr><tr><td>

Work note

</td><td>

If a template includes content to add to the **Work notes** field on the case record, the system does the following:-   Displays a modeless dialog for composing a work note.
-   Adds the content to the **Work notes** field in the modeless dialog.

Selecting **Post Work Notes** adds the content to the **Work notes** field on the case record and to the activity stream.

</td></tr><tr><td>

Comment and work note

</td><td>

If a template includes content to add to both the **Additional comments** and **Work notes** fields on the case record, the system does the following:-   Displays two modeless dialogs, one for composing a comment and one for composing a work note.
-   Adds the content for the comment to the **Comments** field in the comment modeless dialog.
-   Adds the content for the work note to the **Work notes** field in the work note modeless dialog.

Selecting **Post Comments** adds the content to the **Additional comments** field on the case record and to the activity stream.

Selecting **Post Work Notes** adds the content to the **Work notes** field on the case record and to the activity stream.

</td></tr></tbody>
</table>If text already exists in the **Additional comments** or **Work notes** fields, applying a template opens a modeless dialog and adds the template content. Selecting **Undo** removes the template content from the modeless dialog and replaces it with the existing text from the fields on the Case record.

## Updating the glide.ui.journal.use\_html property

The Rich Text Editor \(RTE\) is enabled for modeless dialogs and the thin compose modeless dialog feature. It isn't enabled for the instance unless the **glide.ui.journal.use\_html** system property is set to true.

When you enter text in a comment or work note modeless dialog, the system adds that same text to the **Additional comments** and **Work notes** fields on the case record. HTML tags can appear along with the text in these fields.

To remove the HTML tags, enable the **glide.ui.journal.use\_html** system property:

1.  In the navigation filter, enter **sys\_properties.list** to display a list of the properties stored in the System Properties \[sys\_properties\] table.
2.  Search for the **glide.ui.journal.use\_html** property in the **Name** column.
3.  Set the **Value** field to true and select **Update**.
4.  Return to CSM Configurable Workspace and refresh the page.

Setting this property to true enables the Rich Text Editor for the **Additional comments** and **Work notes** fields on the case record and removes the HTML tags.

