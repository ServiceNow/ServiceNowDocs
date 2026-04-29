---
title: Components installed with case digests
description: Several types of components are installed with the Case Digests plugin.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Components installed with case digests

Several types of components are installed with the Case Digests plugin.

## Tables

The Case Digests plugin adds the following tables:

-   Case Digest Configuration \(sn\_csm\_case\_digest\_config\)
-   Case Digest \(sn\_csm\_case\_digest\_task\)
-   Post Case Review \(sn\_csm\_case\_digest\_pcr\)
-   Case Action Summary \(sn\_csm\_case\_digest\_cas\)

The Customer Service Document Template plugin adds the CS Document Template \(sn\_csm\_doctemplate\_template\) table.

## Extension points

The Case Digests plugin includes the following extension points. Customers can use these extension points to customize the publish action.

|Extension point|Description|
|---------------|-----------|
|sn\_csm\_case\_digest.CASPublish|Use this extension point to alter the functionality of publishing a case action summary to a case.|
|sn\_csm\_case\_digest.PCRPublish|Use this extension point to alter the functionality of publishing a post case review document to a case.|
|sn\_csm\_case\_digest.MajorPCRPublish|Use this extension point to alter the functionality of publishing a post case review document to a major case.|

