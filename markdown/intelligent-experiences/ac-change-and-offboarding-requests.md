---
title: Change and offboarding requests
description: Make controlled changes to a managed AI asset, or retire an asset that is no longer needed, by submitting a request for AI steward review and approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ac-change-and-offboarding-requests.html
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 1
keywords: [change request, offboarding request, retire]
breadcrumb: [Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Change and offboarding requests

Make controlled changes to a managed AI asset, or retire an asset that is no longer needed, by submitting a request for AI steward review and approval.

A request is a structured submission that an asset owner makes when they need to change or retire a managed AI asset. AI Control Tower routes each request to an AI steward for review, runs the request through the appropriate approval playbook, and either applies the requested change or moves the asset to retirement. Requests give asset owners a controlled way to evolve their AI assets, and they give AI stewards a consistent way to govern those changes.

## Types of requests

AI Control Tower supports two types of requests:

-   **Change request**

    A request to modify a managed AI asset. A change request might propose switching the AI model that backs an agent, updating an asset's version, modifying the asset's use and purpose, or changing the sub-AI systems and AI models associated with the asset. Change requests give asset owners a path to keep their assets current without bypassing governance.

-   **Offboarding request**

    A request to retire a managed AI asset. An offboarding request initiates the offboarding lifecycle stage for the asset, which removes the asset from active use and confirms that dependencies have been resolved and any data the asset produced is handled according to policy.


## Request lifecycle

Both request types follow a similar lifecycle:

1.  An asset owner submits the request from the asset record.
2.  AI Control Tower runs the request through an approval playbook. The playbook might require a review of the asset, an evaluation of the impact, and a remediation plan before the request can be approved.
3.  An AI steward reviews the request, including the impact on related sub-AI systems and AI models. The steward approves or rejects the request.
4.  If approved, AI Control Tower applies the change to the asset \(for a change request\) or moves the asset into the offboarding stage \(for an offboarding request\). If rejected, the asset is unchanged and the request is closed.

## Where requests appear

Requests appear on the **Requests** sub-tab of the **Team**, **Assigned to you**, and **Unassigned** views in Activity Center, depending on assignment. Asset owners can also see requests they have submitted from the affected asset's record.

