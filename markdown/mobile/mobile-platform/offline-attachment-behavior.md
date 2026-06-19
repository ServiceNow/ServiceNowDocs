---
title: Attachment behavior in offline mode
description: Learn about the size and type limits applied to attachments in the offline cache.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/offline-attachment-behavior.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Attachment behavior in offline mode

Learn about the size and type limits applied to attachments in the offline cache.

Attachments can be added to input forms, record screens, activity streams, and details views. Applying size and type limits to attachments keep the offline cache small, preventing unnecessary or oversized files from overloading the device. The total storage allocated for attachments on a user's device is limited to 2,048 MB.

The following system properties are available when managing attachments in offline mode.

|Property|Description|
|--------|-----------|
|glide.sg.ofﬂine.attachment.allowed\_content\_types|A comma-separated list of allowed ﬁle types for attachments in ofﬂine mode.|
|glide.sg.ofﬂine.attachment.max\_size|Set the Maximum size per downloaded attachment.|
|glide.sg.ofﬂine.attachment.max\_total\_bytes|Total attachment storage limit.|

For information on these and other related offline system properties, see [System properties in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-system-properties.md).

-   **[General guidelines for using attachments in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/general-guidelines-offline-attach.md)**  
When working with attachments in offline mode, keep these general guidelines in mind for usability and a good user experience.

**Parent Topic:**[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md)

