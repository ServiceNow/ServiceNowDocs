---
title: Attaching files to records from portal pages
description: Attachments can be added to records from portal pages by navigating the file system, pasting files from the clipboard, or dragging and dropping files.Allow portal users to attach files by pasting or dropping files in the Add attachments dialog box.Allow portal users to drop attachments in a dedicated zone of a page to quickly attach files to a record.Allow portal users to paste, drop, or navigate to files in a section of a widget to quickly attach files to a record.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Attaching files to records from portal pages

Attachments can be added to records from portal pages by navigating the file system, pasting files from the clipboard, or dragging and dropping files.

By default, several base system widgets accept attachments from portal users using one or more of these methods. To modify how portal users can add attachments, you can clone and edit widgets to customize the file attachment experience as described in the following procedures.

To track how portal users attach files to records from pages in your portal, see the SP File Attach event in User Experience Analytics for Service Portal. For more information about available events, see [Service Portal events](../reference/sp-analytics-events.md).

**Parent Topic:**[Creating portal pages](../concept/c_Pages.md)

## Add attachments by pasting or dropping files

Allow portal users to attach files by pasting or dropping files in the Add attachments dialog box.

### Before you begin

By default, the Form, Ticket Attachments, Ticket Conversations, and SC Catalog Item base system widgets support adding attachments by pasting or dropping files in the Add attachments dialog box rather than only by navigating the file system.

To configure this functionality for other widgets, you can clone or create a widget that supports adding attachments with the `sp-attachment-button` directive. For more information about cloning widgets, see [Clone a widget](t_CloneAndEditAWidget.md).

**Note:** Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. However, cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from.

Role required: sp\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Widget Editor**.

3.  In the Edit an existing widget menu, select the widget you cloned.

4.  In the **HTML Template** of the widget, locate the `sp-attachment-button` element.

5.  Configure attributes for the `sp-attachment-button` element.

    -   `modal`: Enables copy-paste and drag-and-drop support when set it to `true`.

        To turn off copy-paste and drag-and-drop support, set it to `false`.

    -   `supported-extensions`: Displays a list of supported file extensions for attachments at the bottom of the Add Attachments dialog box.

        To list the supported file extensions specified by the **glide.attachment.extensions** system property, set it to `{{::data.supportedAttachmentExtensions}}`.

    ```xml
    <sp-attachment-button modal="true" supported-extensions="{{::data.supportedAttachmentExtensions}}"></sp-attachment-button>
    ```

6.  Select **Save**.


### Result

On a page with the widget, you can paste or drop files over the Add attachment dialog box to attach them to the record, as shown in the following example.

**Note:** This functionality isn't supported for mobile experiences. Pasting attachments isn’t supported in Firefox.

![Option to choose, drop, or paste files in the Add attachments dialog box](../image/add-attachment-dialog.png)

## Add a drag-and-drop zone for attaching files

Allow portal users to drop attachments in a dedicated zone of a page to quickly attach files to a record.

### Before you begin

To configure a drag-and-drop attachments zone on a page, you must clone or create a widget that supports adding attachments by calling `attachmentHandler` set to an instance of `nowAttachmentHandler` in its client script. For an example of a widget like this, see the [Form widget](../concept/form-widget.md). For more information about cloning widgets, see [Clone a widget](t_CloneAndEditAWidget.md).

**Note:** Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. However, cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from.

Role required: sp\_admin or admin

### About this task

By default, portal users can add attachments on many base system pages by selecting the Add attachments icon \(![Attachment icon](../../../administer/workspace/image/attach-icon.png)\) to open the Add attachments dialog box. With a drag-and-drop attachments zone, portal users can add attachments with fewer clicks. For example, you could drop attachments over an area of a catalog request or a form.

In this example, the zone is an area over the body of a form widget. The zone is only visible when moving a file over it.

![Dragging a file over the attachment zone in a form widget](../image/attachment-zone.png "Attachment zone over a widget")

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Widget Editor**.

3.  In the Edit an existing widget menu, select the widget you cloned to add the attachment zone to.

4.  In the **HTML Template** of the widget, add the `sp-attachment-picker attachment-handler="attachmentHandler"` directive as an attribute of a `<div>` or `<section>` element.

    The zone can include the entire widget or only part of it.

    ```xml
    <div sp-attachment-picker attachment-handler="attachmentHandler">
    ```

5.  Configure attributes for the `sp-attachment-picker` directive.

    -   `disable-picker-overlay="true"`: Turns off showing an overlay over the attachment zone when you drag a file over it. By default, the overlay is enabled.
    -   `onFilePick`: Implements custom logic by triggering an event when any file is picked. Set the value to a function that takes in the references of all the selected files as an array as the first parameter. For example, `on-file-pick="attachFiles($files)"`. Examples of custom logic that could be implemented include previewing the files, custom validations, or custom upload logic. If this attribute is configured, the `attachment-handler="attachmentHandler"` attribute isn’t needed and can be removed.
6.  Hide the attachment zone on mobile devices.

    1.  Add the `ng-if="isDesktopBrowser"` directive to the `sp-attachment-picker` directive.

        ```xml
        <div sp-attachment-picker attachment-handler="attachmentHandler" ng-if="isDesktopBrowser">
        ```

    2.  In the **Client Script** of the widget, add the following script.

        ```javascript
        $scope.isNative = cabrillo.isNative();
        $scope.isMobileBrowser = spUtil.isMobile() && !$scope.isNative;
        $scope.isDesktopBrowser = !$scope.isNative && !$scope.isMobileBrowser;
        
        ```

7.  Select **Save**.


### Result

On a page with the widget, you can drag one or more selected files over the attachment zone and drop them to attach them to the record.

## Add an attachments section to a widget

Allow portal users to paste, drop, or navigate to files in a section of a widget to quickly attach files to a record.

### Before you begin

To configure an attachments section in a widget, you must clone or create a widget that supports adding attachments by calling `attachmentHandler` set to an instance of `nowAttachmentHandler` in its client script. For an example of a widget like this, see the [Form widget](../concept/form-widget.md). For more information about cloning widgets, see [Clone a widget](t_CloneAndEditAWidget.md).

**Note:** Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. However, cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from.

Role required: sp\_admin or admin

### About this task

By default, portal users can add attachments on many base system pages by selecting the Add attachments icon \(![Attachment icon](../../../administer/workspace/image/attach-icon.png)\) to open the Add attachments dialog box. With an attachments section, portal users can add attachments with fewer clicks.

In this example, the attachments section is added to the bottom of a catalog item widget.

![A section to add attachments in within the catalog item widget](../image/attachment-zone-element.png "Attachment section in a widget")

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Widget Editor**.

3.  In the Edit an existing widget menu, select the widget you cloned to add the attachment section to.

4.  In the **HTML Template** of the widget, add the `sp-attachment-picker` directive as an element where you want the attachments section to appear.

    ```xml
    <sp-attachment-picker attachment-handler="attachmentHandler"></sp-attachment-picker>
    ```

5.  Configure attributes for the `sp-attachment-picker` directive.

    -   `disable-picker-overlay="true"`: Turns off showing an overlay over the attachment section when you drag a file over it. By default, the overlay is enabled.
    -   `onFilePick`: Implements custom logic by triggering an event when any file is picked. Set the value to a function that takes in the references of all the selected files as an array as the first parameter. For example, `on-file-pick="attachFiles($files)"`. Examples of custom logic that could be implemented include previewing the files, custom validations, or custom upload logic.
6.  Hide the attachment section on mobile devices.

    1.  Add the `ng-if="isDesktopBrowser"` directive to the `sp-attachment-picker` directive.

        ```xml
        <sp-attachment-picker attachment-handler="attachmentHandler" ng-if="isDesktopBrowser"></sp-attachment-picker>
        ```

    2.  In the **Client Script** of the widget, add the following script.

        ```javascript
        $scope.isNative = cabrillo.isNative();
        $scope.isMobileBrowser = spUtil.isMobile() && !$scope.isNative;
        $scope.isDesktopBrowser = !$scope.isNative && !$scope.isMobileBrowser;
        
        ```

7.  Select **Save**.


### Result

On a page with the widget, you can paste or drop one or more selected files over the attachment section to attach them to the record.

**Note:** Pasting attachments isn't supported on Firefox.

