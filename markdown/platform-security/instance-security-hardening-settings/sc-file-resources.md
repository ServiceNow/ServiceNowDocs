---
title: File and resources
description: The file and resources category ensures applications handle untrusted file data securely and store untrusted data from untrusted sources with limited permissions in an appropriate location.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Hardening settings, Platform Security]
---

# File and resources

The file and resources category ensures applications handle untrusted file data securely and store untrusted data from untrusted sources with limited permissions in an appropriate location.

This includes controls such as avoiding denial of service through large or unexpected file types, validating file type and preventing against path traversal.

-   **[Disallow infected file download \[Updated in Security Center 1.5 and 2.0\]](sc-disallow-infected-files-download.md)**  
Control whether users can download non-scanned attachments if the antivirus service is down or unreachable.
-   **[Enable email spam scoring and filtering \[Updated in Security Center 1.3\]](sc-email-spam-scoring-and-filtering.md)**  
Install the Email Filter \(**com.glide.email\_filter**\) plugin to install email filtering within the instance. This filtering identifies existing headers, which enables you to decide what to do with the email based on the associated header. Alternatively, set **com.glide.email\_filter** to false.
-   **[Enable antivirus scan](sc-enable-antivirus-scan.md)**  
The **com.glide.snap.enable\_scan** property activates the antivirus scan functionality.
-   **[Restrict downloadable files types in static content \[Updated in Security Center 1.3\]](sc-files-types-download-restrictions-from-static-content.md)**  
Use the **glide.ui.strict\_customer\_uploaded\_static\_content** property to enable restrictions on the file types that can be downloaded when they have been uploaded using the Upload File functionality.
-   **[Limit attachment size in training and prediction flows for GraphQL endpoints \[New in Security Center 1.3 and updated in 1.5\]](sc-limit-attachment-size-in-training-and-prediction-flows-for-graphql-enpoints-plugin-applicability-platform-document-intelligence.md)**  
The **glide.platform\_ml\_di.max\_attachment\_size\_graphql** property controls the maximum allowed size limit for returning attachments in GraphQL endpoints of training or prediction flows.
-   **[Limit attachment size in training and prediction flows \[New in Security Center 1.3 and updated in 1.5\]](sc-limit-attachment-size-in-training-and-prediction-flows-plugin-applicability-platform-document-intelligence.md)**  
The **glide.platform\_ml\_di.max\_attachment\_size** property controls the maximum allowed size limit for returning attachments in training and prediction flows.
-   **[Limit HTTP response body size \[New in Security Center 1.3 and updated in 1.5\]](sc-limit-http-response-body-size.md)**  
Configure the **glide.http.response.get\_body.limit.enabled** and **glide.http.response.get\_body.limit** properties to protect your instance against OutOfMemoryExceptions.
-   **[Limit maximum number of attachments in email](sc-limit-maximum-number-of-attachments-in-email.md)**  
Configure the number of inbound email attachments allowed per Email \[sys\_email\] record on your instance.
-   **[Maximum allowed attachment size \[Updated in Security Center 1.3\]](sc-max-allowed-attachment-size.md)**  
Configure the **com.glide.attachment.max\_size** property to control the maximum size \(in megabytes\) permitted for an uploaded attachment.
-   **[Set Allowed MIME Child Types \[New in Security Center 2.0\]](sc-set-allowed-mime-child-types.md)**  
Learn how to configure the **glide.security.mime.type.allowed\_child\_types** property to a secure setting so that file types will not pass the Multipurpose Internet Mail Extensions \(MIME\) type checking. This reduces the risk of remote code execution on an uploaded file.
-   **[Validate file mime type in AttachmentCreator soap web service \[New in Security Center 1.3 and updated in 1.5\]](sc-validate-file-mime-type-in-attachmentcreator.md)**  
The **glide.attachment.enforce\_security\_validation** property determines whether Multipurpose internet Mail Extensions \(MIME\) files undergo validation.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

