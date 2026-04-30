---
title: Normalization suggestions for discovery models
description: Normalization suggestions are created for discovery models with field values that differ from those in the package or pattern rules. You can accept or reject these suggestions.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Software discovery and normalization, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Normalization suggestions for discovery models

Normalization suggestions are created for discovery models with field values that differ from those in the package or pattern rules. You can accept or reject these suggestions.

During the weekly normalization process, if there are differences \(or updates\) identified between the manually normalized value for Publisher, Product, Version, Edition, Platform, and Language, and the corresponding values in the package or pattern, a Normalization Suggestion record is created.

**Note:** Normalized suggestions are generated only when the normalized values differ from what the content library displays. If its an exact match, a suggestion is not made.

You can evaluate suggestions to normalize discovery models that were manually normalized incorrectly. Suggestions can either be accepted, which updates the Discovery Model with the correct values, or rejected, which does not change the manually normalized values.

The records are contained in the Normalization Suggestion \[samp\_normalization\_suggestion\] table.

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

