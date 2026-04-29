---
title: Contextual development edit messages
description: The platform displays a message if you attempt to edit a Store Application record when you're in a different application scope.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lists and forms in scoped applications, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Contextual development edit messages

The platform displays a message if you attempt to edit a Store Application record when you're in a different application scope.

![If you're not in the scope for a store application, a message appears with options to edit the record or switch scope.](../image/ApplicationContextWarningMessage.png "Application context edit message")

This message can be used to:

-   Open the application to which the current configuration record belongs.
-   Open the application of the currently selected application in the application picker.
-   Temporarily switch to the application to which the current configuration record belongs and edit it.

**Note:** The system returns you to the current application context after you save or cancel out of the record.

The system also displays a message when a user attempts to configure a list or form layout while working from another application scope.

![If you want to edit a list or form layout from a different scope, a message appears with some options for editing.](../image/FormLayoutContextWarnings.png "Application context edit message for form layout or design")

The message provides a list of valid options:

-   Edit the current section by temporarily switching to the application that owns it.
-   Create a section in the current application context.
-   Create a view in the current application context.

**Note:** The system returns you to the current application context after you save or cancel out of the record.

