---
title: Configure application-specific field values for Zoom interactions
description: Use scripted extension points to enable the copying of application-specific field values to interaction records for Zoom meetings initiated from chats.
locale: en-US
release: australia
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Chat Zoom Connector, Chat channel, Enable communication channels, Configure, Customer Service Management]
---

# Configure application-specific field values for Zoom interactions

Use scripted extension points to enable the copying of application-specific field values to interaction records for Zoom meetings initiated from chats.

## Before you begin

Role required: admin

Install the Chat Zoom Connector application. For more information, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallApplications.md).

## About this task

You can enable the copying of any application-specific fields from a parent chat interaction record to its Zoom interaction record by using the sn\_chat\_zoom.ZoomInteractionExtPoint extension point. The parent chat is the chat from which the Zoom meeting was initiated.

By using extension points, you can easily integrate customizations without having to alter the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).

An implementation is available in the base system for scripted extension points. You can modify the data and add additional fields.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and select **sn\_chat\_zoom.ZoomInteractionExtPoint**.

3.  On the Extension Point form, select a script include to use the sn\_chat\_zoom.ZoomInteractionExtPoint extension point.

    -   Create and register a custom script include.

        For more information, see [Registering custom script includes against the scripted extension points](../../../build/applications/concept/impl-scripted-ext-pts-custom-code.md).

    -   Modify the existing script include by going to the Implementations related list and selecting a script include in the **Class** column. The script includes are displayed in the **Class** column.

        **Note:** By default, the ZoomInteractionExtPoint and CSMZoomInteractionImpl script includes that use the sn\_chat\_zoom.ZoomInteractionExtPoint extension point are available for Global and Chat Zoom Connector applications.

        -   The ZoomInteractionExtPoint script include for the Global application copies the field values from the parent chat interaction record to the Zoom interaction record.
        -   If the Customer Service application is installed, the CSMZoomInteractionImpl script include for the Chat Zoom Connector application copies the value of the **Consumer**, **Account**, and **Contact** fields from the interaction record of the parent chat to the Zoom interaction record. The CSMZoomInteractionImpl script include is available only when the Customer Service application is installed.
4.  Include application-specific fields by adding the sn\_chat\_zoom.ZoomInteractionExtPoint extension point in the script include.

    You can create multiple implementations for an extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

5.  On the Extension Point form, select **Update**.


