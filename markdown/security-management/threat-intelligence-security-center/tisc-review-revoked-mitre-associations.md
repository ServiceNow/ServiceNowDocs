---
title: Review revoked MITRE tactic and technique associations
description: Review the tactic and technique pairs that MITRE no longer maps, then delete or remap the entity and case associations that were created from them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/threat-intelligence-security-center/tisc-review-revoked-mitre-associations.html
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 3
keywords: [revoked tactic technique, MITRE ATT&amp;CK, Delete Associations, Re-Map Associations]
breadcrumb: [MITRE-ATT&amp;CK repository, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Review revoked MITRE tactic and technique associations

Review the tactic and technique pairs that MITRE no longer maps, then delete or remap the entity and case associations that were created from them.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

A MITRE ATT&amp;CK release may revoke a technique or remove a technique-to-tactic mapping. When this occurs, the next MITRE ingestion retires the tactic and technique link, along with all entity and case associations built from it. Retirement is a soft delete. If MITRE restores a pair in a later release, the pair is reinstated automatically.

Retired associations no longer appear on the MITRE ATT&amp;CK canvas, on the technique cards, or in the MITRE reports. The associations themselves remain on the entity and case records until you act on them from the review list.

**Note:**

A review record is created only when at least one entity or case association was built from the revoked pair. If nothing was ever derived from the pair, there is nothing to review and no record appears.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **MITRE ATT&amp;CK** &gt; **Revoked Tactic-Techniques**.

    The list displays the revoked pairs that have a status of **Review**, **In Progress**, or **Error**. The pairs with the status of **Complete** move out of the list.

2.  Select a record to open it, and review the **Review Reason** and **Revoked Collection Version** values.

    **Review Reason** distinguishes the two ways a pair can be revoked. Either the technique itself was revoked in the MITRE collection, or the technique is no longer mapped to this tactic. For a description of every field on the record, see [Revoked MITRE tactic-technique review fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-revoked-review-fields.md).

3.  Review the **Entity Associations** and **Case Associations** related lists.

    These lists show the entity and case records that the pair produced, so that you can see the full scope of an action before you run it.

4.  To remove every association that the pair produced, select **Delete Associations**.

    The pair is removed from the entity, entity source, and case association records within the domain of the review record. **Action Taken** is set to **Delete**.

    **Warning:**

    Deleting the associations can't be undone. Nothing is removed until you run this action.

5.  To move the associations onto a different pair instead, select **Re-Map Associations**.

    1.  Select the new tactic.

    2.  Select the new technique.

        Only pairs that MITRE currently maps are offered, so you can't remap onto another revoked pair.

    3.  Select **Submit**.

        Every entity and case association moves to the pair that you selected. Where the target association already exists on a record, the retired association is removed rather than duplicated. **Action Taken** is set to **Update mapping**, and the pair that you selected is recorded in **New Tactic** and **New Technique**.


## Result

Both actions run in the background. The status of the review record moves from **Review** to **In Progress** and then to **Complete**, and the requested action is recorded in the work notes of the record. Values on the review record change only through the two actions.

## What to do next

To clear a completed record from the worklist, open it and select **Delete**. This action is available only on completed records, and it requires the sn\_sec\_tisc.admin role.

-   **[Revoked MITRE tactic-technique review fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-revoked-review-fields.md)**  
Fields on the review record that MITRE ingestion creates for a revoked tactic and technique pair, and the values that each field can hold.

**Parent Topic:**[MITRE-ATT&amp;CK repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-att-ck-framework-overview.md)

**Related topics**  


[Revoked MITRE tactic-technique review fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-revoked-review-fields.md)

[MITRE-ATT&amp;CK repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-att-ck-framework-overview.md)

