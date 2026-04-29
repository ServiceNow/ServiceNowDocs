---
title: Line breaks in email notifications and rich HTML
description: Rich HTML provides additional control over line breaks in your email notifications and templates.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Line breaks in email notifications and rich HTML

Rich HTML provides additional control over line breaks in your email notifications and templates.

To provide control over line breaks, a **Newlines to HTML** check box is available in the **Email Script** form.

Selecting the **Newlines to HTML** check box indicates that the method for handling line breaks in earlier versions carries forward for email notifications and templates. When an email notification or template is converted to rich HTML, the **Newlines to HTML** check box is automatically selected.

For new mail scripts, add correct HTML line breaks to template.print\(\) statements.

If an email notification or template is not converted to rich HTML, newlines are automatically wrapped with &lt;div&gt; tags, the same as previous versions. The old mail scripts still work. However, the administrator does not enjoy the benefits of working in the rich HTML format, and does not have as much control over exact HTML formatting.

## HTML line breaks in new scripts

When writing new scripts, insert explicit HTML line breaks and clear the **Newlines to HTML** check box so that no HTML tags are injected when email notifications are generated. For existing notifications and templates, replace template.print\("\\n"\) JavaScript function calls with template.print\("&lt;br /&gt;"\). This replacement gives you better control over the HTML formatting of your email notifications.

**Parent Topic:**[Create an email notification](../task/t_CreateANotification.md)

