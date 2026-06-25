---
title: Composing emails with predefined content from the Source-to-Pay Workspace
description: Insert predefined content into the message body of emails that you send from the email client in the Source-to-Pay Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/email-composer-slm-workspace.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Composing emails with predefined content from the Source-to-Pay Workspace

Insert predefined content into the message body of emails that you send from the email client in the Source-to-Pay Workspace.

You can use this feature to compose and send emails directly from a supplier case or a supplier task. To open the email client, select **Compose Email** from the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: More actions icon.\) from a supplier case or a supplier task. A draft email appears with pre-populated data in the **Cc** and **Subject** fields. The **Cc** field is auto-populated with the email address of the contact who opened the case. The **Subject** field is auto-populated with the case number and issue description.

## Using quick messages

In the email client, you can select a quick message to fill the email body with the content that is specified in the quick message. After you define one or more quick messages, the Quick Messages contextual pane appears in the email client so that you can draft an email with a quick message of your choice.

By default, the following quick messages are provided for the following supplier records:

-   Supplier case: Standard closure response, case progress, primary contact information, Knowledge Base article information, and additional information.
-   Supplier task: Standard closure response, case progress, primary contact information, Knowledge Base article information, and additional information.

**Note:** The quick message templates contain placeholder text that you must replace with the appropriate text.

For more information on how to create a quick message, see [Define a quick message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_QuickMessages.md).

## Using response templates

Resolve cases faster and more efficiently with response templates. Response templates are reusable messages that can be copied to draft emails to provide quick and consistent messages to users.

Open the response template that you want to use for your email and select **Copy to clipboard**. You can now paste the contents of this template at the location of the cursor. It doesn't replace the content that you created before selecting the response template. To replace existing content with a response template content, highlight the text to replace and then select a response template.

For more information on how to work with response templates, see [Create or modify a response template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-modify-templated-snippet.md).

## Viewing draft emails

After you save the emails as draft, you can view the draft emails by selecting the **Draft Emails** tab on the supplier case or supplier task. Alternatively, you can view the draft emails by selecting the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\) and selecting the **Case Draft Emails** or **Task Draft Emails** sub-modules under the **Draft Emails** module.

## Emailed message in activity log

After your email is composed, sent, and received by the intended recipient, you can see the email message in the **Activity** section of the supplier case or task. You can continue to work with this email from the activity log.

## Email composer configuration

To view the **Compose Email** option in the More Actions menu, and to view your emailed message in the activity log of a supplier case or supplier task in Source-to-Pay Workspace, ensure that you add the role required to access this feature in the User Interface Properties page. For more information, see [Configure access to the compose email feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-access-compose-email.md).

-   **[Configure access to the compose email feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-access-compose-email.md)**  
Configure the role required to access the compose email feature that enables you to send emails directly from a supplier case or supplier task in the Source-to-Pay Workspace.
-   **[Communicate using emails from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/send-emails-slm-ws.md)**  
Compose and send emails directly from a supplier case or a supplier task in the Source-to-Pay Workspace.

**Parent Topic:**[Using Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/use-supp-mgr-wsp.md)

**Related topics**  


[Create a supplier from the Source-to-Pay Workspace]()

[Manage supplier details]()

[Manage internal stakeholders]()

[Manage supplier contacts from the Source-to-Pay Workspace]()

[Manage supplier cases from the Source-to-Pay Workspace]()

[Manage supplier tasks from the Source-to-Pay Workspace]()

[Offboard a supplier from the Source-to-Pay Workspace]()

[Accept an incoming chat request from the Source-to-Pay Workspace]()

[Interaction Management in Supplier Lifecycle Operations]()

[Overall supplier dashboard]()

[Create supplier case from Universal Request]()

[Emails view for supplier managers]()

[Configure access to the compose email feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-access-compose-email.md)

[Communicate using emails from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/send-emails-slm-ws.md)

