---
title: Playbook modeless dialogs
description: Use modeless dialogs, windows that overlay the main window content, to create and post comments and work notes to the activity stream and to compose and send emails.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Playbook page templates, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Playbook modeless dialogs

Use modeless dialogs, windows that overlay the main window content, to create and post comments and work notes to the activity stream and to compose and send emails.

A modeless dialog is a window that appears in a workspace as an overlay on top of the main window content. This overlay enables users to interact with the window content and the overlay content at the same time. Agents can use modeless dialogs to do the following while working in a playbook:

-   Create comments and work notes to post to the activity stream.
-   Create and send emails and reply to or forward emails.

After opening a modeless dialog, agents can move it around the screen and put it where they need it. This feature enables agents to reference information from the main window while drafting text in the overlay window.

The playbook page templates include the following modeless dialogs:

-   Compose Activity - for creating and posting comments and work notes
-   Compose Email - for creating and sending emails

You can access the modeless dialogs by selecting the **Compose** button in the action bar and then selecting one of the following actions:

-   Compose Comments
-   Compose Email
-   Compose Work notes \(Private\)

## Create comments and work notes

Agents can use the Compose Activity modeless dialog to create comments and work notes and post them to the activity stream. See the following table for more information about creating these activities.

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

<table id="table_bmb_hzd_w1c"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create and send an email

</td><td>

To create and send an email:1.  Select **Compose** &gt; **Compose Email** from the action bar to open a Compose Email window.

The system automatically applies the email template with the lowest order to the new email.

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

1.  Open the Email Templates tab in the contextual side panel.
2.  Select the More Actions menu on the desired email template.
3.  Select **Apply template**.

The system adds the contents of the template to the body of the email.

**Note:** When you create a new email, the system automatically applies the email template with the lowest order.

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

Select an email draft from the Draft Emails related list

</td><td>

1.  Select the Related Lists tab in the contextual side panel.
2.  Expand the Draft Emails related list.
3.  Select the Open draft icon on the desired draft email card.

The system opens the selected draft email in a sub-tab.

</td></tr></tbody>
</table>## Modeless dialog guidelines

The following guidelines apply to the Compose Email window:

-   An agent can create multiple email drafts.
-   An agent can have one Compose Email window open at a time. The system displays a message if an agent tries to open another Compose Email window while the first Compose Email window is still open.
-   An agent has to manually close a Compose Email window before opening a new window.
-   The Compose Email window can be resized.

