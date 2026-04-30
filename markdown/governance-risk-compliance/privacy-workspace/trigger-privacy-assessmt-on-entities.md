---
title: Initiating privacy assessments for an entity or a processing activity
description: To discover whether a business process or an application is processing personal data, you can use privacy screening assessments. To regularly assess how processing activities are processing personal data, you can use privacy assessments such as privacy impact assessment \(PIA\).
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Types of privacy assessments, Use, Privacy Management, Governance, Risk, and Compliance]
---

# Initiating privacy assessments for an entity or a processing activity

To discover whether a business process or an application is processing personal data, you can use privacy screening assessments. To regularly assess how processing activities are processing personal data, you can use privacy assessments such as privacy impact assessment \(PIA\).

## Privacy screening assessment

Conducting a privacy screening assessment helps you discover whether the entity is processing personal information or not.

You can send the privacy screening assessments in the following ways:

-   From the entity record only when a processing activity is not available.
-   From the entities related list in entity types.

When you initiate privacy screening assessments for entities, processing activities are created based on the responses submitted by the entity owners.

**Note:** The processing activity creation rules can be configured based on the screening assessment responses.

After a processing activity is created, based on the assessment configurations, the following events occur:

1.  The necessary information objects are mapped to the processing activity record. To understand more about information objects and their uses, see [Information objects](../../grc-risk/reference/information-objects.md).
2.  The necessary controls are mapped to the processing activity record.
3.  Critical assessment responses such as the purpose of the processing activity, data subject type and so on are copied over to the processing activity record.

**Note:** If you accidentally send an assessment and the assessment is not completed, you can cancel the assessment.

## Privacy assessments

When processing activity records are identified, to understand how a processing activity is processing personal information, various types of privacy assessments such as privacy impact assessments \(PIA\) and transfer impact assessment \(TIA\) are sent. You can trigger PIAs from a single processing activity record. For more information, see [Send a privacy assessment from a processing activity](../task/send-privacy-asmt-from-pa.md). Alternatively, you can send privacy impact assessments to multiple processing activities, using the Entity type capability or from the processing activity list view. For more information on how to send an assessment to multiple entities, see [Send a privacy assessment to multiple entities](../task/send-privacy-assessment.md).

-   **[Send a privacy assessment from an entity](../task/send-privacy-assessmt-entity.md)**  
Send a privacy assessment to an entity owner to determine if there's personal data involved in the processing activities.
-   **[Send a privacy assessment to multiple entities](../task/send-privacy-assessment.md)**  
Send the privacy screening assessment or the Privacy impact assessment \(PIA\) assessments to multiple entities to understand why and how personal data is being processed.

**Parent Topic:**[Types of privacy assessments](privacy-assessments.md)

**Related topics**  


[Send a privacy assessment to multiple entities](../task/send-privacy-assessment.md)

