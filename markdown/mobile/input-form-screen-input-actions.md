---
title: Input form actions in an input form screen
description: Learn about adding a button next to input form fields. This button allows users to add comments, attach files, and navigate to other screens.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Input actions and input sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Input form actions in an input form screen

Learn about adding a button next to input form fields. This button allows users to add comments, attach files, and navigate to other screens.

Add a more menu button ![More menu icon.](../image/icon-ifs-input-more-iOS.png) by specified input value fields.

**Note:** The button appearance may vary between iOS and Android operating systems. The button is indicated with three dots either horizontally or vertically.

This button can include any variety of action items: comment, attachment, and navigation buttons.

-   **Comments**: Where users can add, edit, or delete a comment. Users can add only one comment for each input value field.
-   **Attachments**: Users can either select images from the gallery or add a new image to the gallery. Alternatively, they can add an image directly using the camera. Users can add multiple attachments to each input value field.

    **Note:**

    For attachment input actions, when mapping attachments as part of a data source, the field name must be declared as a *sys\_id* so it's automatically added to the Attachment \[sys\_sg\_attachment\] table. You then must define which element identifier the element belongs to using the *values.Mapper* attribute.

-   **Navigation button**: Users tap on this option to open an alternative screen or launcher screen. For example, navigate to a list screen to create a follow-up task or to view a knowledge base article in the context of an input. Any number of navigation buttons can be added to the more menu button.

    **Note:** For navigation functions labeled with a Record context, the data source mechanism is required. For navigation functions labeled with a Global context, the data source mechanism isn't required.


For input actions script examples, refer to the following [Script code for storing user-selected attachments in the database](input-actions-script-attachments.md) and [Script code for comment type and updates for input actions](input-actions-script-comments.md).

![Two images illustrating how a menu opens from the bottom of the screen after you select the input form action button.](../image/icon-ifs-input-action-more.png)

