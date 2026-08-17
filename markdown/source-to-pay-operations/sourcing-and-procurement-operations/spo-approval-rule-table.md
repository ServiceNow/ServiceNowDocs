---
title: Approval Rule \[sn\_shop\_approval\_rule\] table
description: The Approval Rule \[sn\_shop\_approval\_rule\] table stores the rules that determine how and when approval requests are sent for purchasing objects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-approval-rule-table.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-07-13"
reading_time_minutes: 3
breadcrumb: [Primary data tables, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Approval Rule \[sn\_shop\_approval\_rule\] table

The Approval Rule \[sn\_shop\_approval\_rule\] table stores the rules that determine how and when approval requests are sent for purchasing objects.

This table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Number|String|System-generated number used to identify this approval rule.|
|Name|String|Name of this approval rule.|
|Active|Boolean|When selected, this rule requests approvals.|
|Approval rule type|Choice|Determines how approvals are requested. The options are Cost Center Managers, Dynamic Users or Groups, Managerial Job Code Hierarchy, Managerial Hierarchy, or Specified Users or Groups.|
|Base approvals on|Field name|Person on whom the approval rule is based.|
|Purchasing user \(deprecated\)|Field name|User from whom approvals are triggered. This field is deprecated.|
|Send approval request to|Choice|People who receive an approval request. The options are Direct Manager, Most Senior Manager, All Managers in Hierarchy, All Users up to the User with Authorized Code, or Most Junior User with an Authorized Code.|
|Up to job level|Reference|Highest job level to which an approval request is sent.|
|Authorized job codes|List|Job codes of those who can approve this object.|
|Approval limit|Currency|Maximum amount that can be approved by the authorized job codes.|
|Approval sequence|Choice|Determines whether approval requests are sent all at once or one at a time. The options are Send Approvals in Parallel or Send Approvals Sequentially.|
|Approval required from|Choice|Determines whether all approvers or just one approver must approve. The options are All Approvers Must Approve or Any Approver Can Approve.|
|Users|List|People who can approve this object.|
|Groups|List|Groups that can approve this object.|
|Send approval to purchasing user's \(deprecated\)|Field name|Approval is sent dynamically to a user or group related to the purchasing user. This field is deprecated.|
|Approval trigger conditions|Conditions|Conditions that the object details must meet for an approval request to be sent.|
|Approving object|Table name|Type of item that needs approval.|
|Approving line|Table name|Line items of the approving object that define the triggers for an approval request.|
|Allow automatic approval|Boolean|When selected, the requester receives automatic approval if the role has the required authority.|

**Parent Topic:**[Primary data tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-primary-data-tables.md)

**Related topics**  


[Fixed Asset \[sn\_fin\_fixed\_asset\] table]()

[Finance Exchange Rates \[sn\_fin\_fx\_rate\] table]()

[Ledger Account table]()

[GL rule \[sn\_fin\_gl\_rule\] table]()

[Threshold rule \[sn\_fin\_gl\_threshold\_rule\] table]()

[Industry \[sn\_fin\_industry\] table]()

[Ledger \[sn\_fin\_ledger\] table]()

[Legal Entity \[sn\_fin\_legal\_entity\] table]()

[Office Location table]()

[Organization \[sn\_fin\_organization\] table]()

[Approval Group \[sn\_shop\_approval\_group\] table]()

[Approval Rule Composition table]()

[Attribute \[sn\_shop\_attribute\] table]()

[Attribute Set \[sn\_shop\_attribute\_set\] table]()

[Attribute Type \[sn\_shop\_attribute\_type\] table]()

[Delivery Location \[sn\_shop\_delivery\_location\] table]()

[Job Code \[sn\_shop\_job\_code\] table]()

[Payment Terms \[sn\_shop\_payment\_term\] table]()

[Price Break \[sn\_shop\_price\_break\] table]()

[Pricing \[sn\_shop\_m2m\_product\_contract\] table]()

[Product group \[sn\_shop\_product\_group\] table]()

[Product Visuals \[sn\_shop\_supplier\_product\_artifact\] table]()

[Shipping methods \[sn\_shop\_shipping\_method\] table]()

