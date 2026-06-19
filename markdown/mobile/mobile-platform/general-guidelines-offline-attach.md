---
title: General guidelines for using attachments in offline mode
description: When working with attachments in offline mode, keep these general guidelines in mind for usability and a good user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/general-guidelines-offline-attach.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Attachments in offline, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# General guidelines for using attachments in offline mode

When working with attachments in offline mode, keep these general guidelines in mind for usability and a good user experience.

**Note:** Many of the issues discussed can be resolved using system properties. For more information, see [System properties in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-system-properties.md).

-   **Controlling offline attachment file types**

    Define which file types can be downloaded offline using the `glide.sg.offline.attachment.allowed_content_types` system property, for example, `image/png` or `image/jpg`. This property prevents irrelevant or unsafe files from being downloaded, keeping offline storage lean.

-   **Limiting attachment file size for offline use**

    Use the `glide.sg.offline.attachment.max_size` system property to set the maximum size in bytes for a single attachment downloaded offline. Files exceeding this limit aren't downloaded and display as a placeholder, preventing large attachments, such as long videos, from causing performance issues or filling device storage.

-   **Total attachment storage limit**

    Use the `glide.sg.offline.attachment.max_total_bytes` system property to cap the total storage space allocated for offline attachments. The default is 50 MB with a maximum of 2 GB, ensuring attachments don't fill up a user's device storage.

-   **Image attachment handling in offline mode**

    Image handling when taking pictures in the activity stream differs by platform:

    -   Android: Images are automatically compressed to approximately 75% quality and converted to JPEG format, regardless of the original file type.
    -   iOS: Images are uploaded as is, with no compression or format conversion applied.

**Parent Topic:**[Attachment behavior in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-attachment-behavior.md)

