---
title: Tags
description: Tags are text labels that you can associate with items like records and pages. Tags enable you to group and organize the items. Tags can be visible to any user \(global\), visible only to specific groups or users \(shared\), or visible to a single user \(private\).
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Tags

Tags are text labels that you can associate with items like records and pages. Tags enable you to group and organize the items. Tags can be visible to any user \(global\), visible only to specific groups or users \(shared\), or visible to a single user \(private\).

Tags are stored in the Tag \[label\] table. To view tags in a list, navigate to **System Definition** &gt; **Tags** or **Self-Service** &gt; **My Tags**.

## Tag sharing levels

The tag sharing level enables other users to use the tag. The **Viewable by** property setting for a tag controls the sharing level.

|Sharing level|Description|
|-------------|-----------|
|Me|**Private** tag, visible only to the owner.|
|Groups and Users|**Shared** tag, visible to the owner and specific groups or users.|
|Everyone|**Global** tag, visible to everyone. This option is available to users with the admin or tags\_admin role.|

## Tag name conflicts

Conflicts can occur if multiple tags have the same name.

-   If a private tag and a shared or global tag have the same name, the system appends **\[private\]** to the name of the private tag. For example, **Sample tag \[private\]**.
-   There cannot be multiple shared or global tags with the same name. If a user attempts to create a shared or global tag with a name that is already in use, an error message appears and the system prevents the tag from being saved.

-   **[Administering tags](administering-tags.md#)**  
If you have an administrator role, you can configure and manage all tags, even tags created by other users. You can also configure notifications, auto-assignment, and Zing indexing for tags.
-   **[Configure Zing tag indexing for text search](../task/t_ConfZingTagIndexTextSearch.md)**  
Zing text indexing is available for tags on records.
-   **[Assigning tags](c_TagAssignment.md#)**  
You can assign tags to records from the form or list view. You can also add tags to a homepage. Tags enable you to group and organize the items.
-   **[Editing tags](editing-tags.md#)**  
You can edit tags that you created from the list and form views, the **My Tags** module, and the Tagged Documents page. You can also merge tags from the **My Tags** module.
-   **[Using tags](using-tags.md#)**  
Use tags to filter records and view tagged documents. Remove a tag when it is no longer useful.

**Parent Topic:**[Common UI elements](../topic/p_CommonUIElements.md)

