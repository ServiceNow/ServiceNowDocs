---
title: Approval rule types
description: Reference information for the approval rule types available in the invoice approval process, including approval conditions, routing methods, and decision methods.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-approval-rule-types.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice approval, invoice processing, invoice automation]
breadcrumb: [Create an approval rule, Invoice approvals, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Approval rule types

Reference information for the approval rule types available in the invoice approval process, including approval conditions, routing methods, and decision methods.

The approval rule types determine the conditions under which approval plans are created and routed.

|Approval rule type|Description|
|------------------|-----------|
|Dynamic Users or Groups|Approvals are dynamically created and sent to the specified user or group. Approvals are triggered based on the purchasing user's attributes. The approval routing method is restricted to just sending approvals in parallel.|
|Managerial Job Code Hierarchy|Approvals are triggered based on the purchasing user's job code and manager's job code. The approval routing method can be parallel or sequential, and the approval decision method can be all approvers or any approver.|
|Managerial Hierarchy|Approvals are triggered based on the purchasing user's manager's hierarchy. The approval routing method can be parallel or sequential, and the approval decision method can be all approvers or any approver.|
|Specified Users or Groups|Approvals are triggered based on the specified users or groups. The approval routing method is restricted to just sending approvals in parallel.|

**Parent Topic:**[Create an approval rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-approval-rule.md)

