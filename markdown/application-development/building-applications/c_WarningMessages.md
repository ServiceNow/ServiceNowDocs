---
title: Contextual development edit messages
description: The platform displays a message if you attempt to edit a Store Application record when you're in a different application scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/c\_WarningMessages.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Lists and forms in scoped applications, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Contextual development edit messages

The platform displays a message if you attempt to edit a Store Application record when you're in a different application scope.

\[Omitted image "ApplicationContextWarningMessage.png"\] Alt text:

This message can be used to:

-   Open the application to which the current configuration record belongs.
-   Open the application of the currently selected application in the application picker.
-   Temporarily switch to the application to which the current configuration record belongs and edit it.

**Note:** The system returns you to the current application context after you save or cancel out of the record.

The system also displays a message when a user attempts to configure a list or form layout while working from another application scope.

\[Omitted image "FormLayoutContextWarnings.png"\] Alt text:

The message provides a list of valid options:

-   Edit the current section by temporarily switching to the application that owns it.
-   Create a new section in the current application context.
-   Create a new view in the current application context.

**Note:** The system returns you to the current application context after you save or cancel out of the record.

