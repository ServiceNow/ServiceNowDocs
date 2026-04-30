---
title: ExtractTermsFromAttachment - Global
description: The ExtractTermsFromAttachment script include provides methods to extract terms from an attachment.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ExtractTermsFromAttachment- Global

The ExtractTermsFromAttachment script include provides methods to extract terms from an attachment.

This script include is called with the ScriptedExtractor object, SysAttachmentInputStream, the sys\_id for the attachment, and the extension for the attachment. The getTerms\(\) method is called to extract the terms from the attachment that should be indexed. The getTerms\(\) method should just return a string that contains the terms. If you prefer to input a file rather than an inputStream, call extractor.getFile\(\) to get the File object containing the attachment.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

