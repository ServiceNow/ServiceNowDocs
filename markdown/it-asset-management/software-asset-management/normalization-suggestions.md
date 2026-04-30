---
title: Normalization suggestions for discovery models
description: Normalization suggestions are created for all manually normalized discovery models. You can accept or reject these suggestions.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software discovery and normalization, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Normalization suggestions for discovery models

Normalization suggestions are created for all manually normalized discovery models. You can accept or reject these suggestions.

## Overview of normalization suggestions

During the weekly normalization process, normalization suggestions are created in both the following scenarios:

-   If even one discovery model field value differs from the suggested normalization values in the Content Service.
-   If all the discovery model field values are the same as the suggested normalization values in the Content Service.

If the system property, **com.snc.samp.auto\_accept\_normalization\_suggestion** is enabled, normalization suggestions are automatically accepted if there are no differences between the suggested normalization values and the manually normalized values. This property is enabled by default.

**Note:** For domain separated environments, individual domains can override this system property for their own domain by creating a new sys\_application\_property value record.

If you accept a suggestion or if it was automatically accepted by the system property, then the status of the discovery model changes to **Normalized** and all suggested values are copied over to the discovery model's normalized fields. If you reject a suggestion, the manually normalized values do not get changed.

The records are contained in the Normalization Suggestion \[samp\_normalization\_suggestion\] table.

## Accepting or rejection suggestions

If you **Accept** the suggestion:

-   Publisher, Product, Version, Edition, Platform, and Language of the discovery model is updated with the values from the normalization rule.
-   Normalization status changes from Manually Normalized to Normalized.
-   Normalization Suggestion status changes to Accepted
-   Normalization date on the discovery model is updated to when the suggestion was accepted.

If you **Reject** the suggestion:

-   Discovery Model retains the manually normalized values and remains in Manually Normalized status.
-   Normalization Suggestion status changes to Rejected.

|Field|Description|
|-----|-----------|
|Discovery model|Software discovery model that represents the installed software.|
|Suggestion status|Suggested [status](c_SAMDiscovery.md) of the normalization process.|
|Discovered publisher|Discovered publisher of the software.|
|Discovered product|Discovered name of the software.|
|Discovered version|Discovered version of the software.|
|Suggested Normalization|
|Suggested publisher|Suggested publisher of the software.|
|Suggested product|Suggested name of the software.|
|Suggested version|Suggested version of the software.|
|Suggested edition|Suggested edition of the software.|
|Suggested platform|Suggested platform of the software.|
|Suggested language|Suggested language of the software.|
|Publisher|Normalized publisher of the software.|
|Product|Normalized product name of the software.|
|Version|Normalized version of the software product.|
|Edition|Normalized edition of the software product.|
|Platform|Normalized platform of the software product.|
|Language|Normalized language of the software product.|

**Parent Topic:**[Software discovery and normalization](c_SAMDiscovery.md)

