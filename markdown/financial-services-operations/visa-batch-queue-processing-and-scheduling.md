---
title: Visa batch queue processing and scheduling
description: Financial Services Operations Integration with Visa subflows use VROL RTSI batch queue APIs to process incoming dispute data on a scheduled basis. Unlike real-time subflows that execute in response to user actions, batch queue processing runs on a predefined schedule to poll VROL for new incoming items across the dispute lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/visa-batch-queue-processing-and-scheduling.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 4
breadcrumb: [Integration with Visa subflows, Components installed, Reference, Visa, Integrate, Financial Services Operations \(FSO\)]
---

# Visa batch queue processing and scheduling

Financial Services Operations Integration with Visa subflows use VROL RTSI batch queue APIs to process incoming dispute data on a scheduled basis. Unlike real-time subflows that execute in response to user actions, batch queue processing runs on a predefined schedule to poll VROL for new incoming items across the dispute lifecycle.

## Visa RTSI batch queue process

Implementation partners and developers must understand the end-to-end flow of Visa RTSI batch queue to configure or extend the FSO Disputes batch queue integration. The process involves three layers of orchestration as shown in the following workflow diagram:\[Omitted image "visa\_rtsi\_batch\_queue\_flow\_img.png"\] Alt text: Workflow diagram showing three layers of orchestration for Visa RTSI batch queue processing

## Process steps

1.  Visa queue scheduler flow is initiated:
    -   Location: **All** &gt; **Workflow Studio** &gt; **Flows** &gt; **Visa Queue Scheduler Flow**
    -   The Visa Queue Scheduler Flow is the entry point for all batch queue processing. It is a scheduled Flow that triggers the entire batch queue pipeline.

        **Note:** The Visa Queue Scheduler Flow is set to **Inactive** by default. Clients must activate it before batch queue processing begins. Until activated, no VROL batch queue data will be ingested into ServiceNow.

    -   Configuration details:
        -   Default schedule: Daily at midnight \(00:00:00\)
        -   Configurable: Clients can change the run time or increase the polling frequency based on dispute volumes and operational requirements.
        -   Single action: The flow contains one action — it calls the Batch Queues Flows Adapter subflow and waits for completion. If the adapter fails, the flow logs an error.
2.  Subflow for the batch queue flows executes:
    -   Location: **All** &gt; **Workflow Studio** &gt; **Flows** &gt; **Batch Queues Flows Adapter**
    -   The Batch Queues Flows Adapter is an orchestration subflow that manages the parallel execution of all individual batch queue subflows. The following actions are invoked by the Visa Queue Scheduler Flow:
        -   Sequentially processes queues that must run in order \(for example, Arbitrations and Recalls are processed first\).
        -   Executes the remaining queue subflows in parallel using a parallel branch, so that multiple VROL queues are polled simultaneously within the same run cycle.
        -   Collects error outputs from each subflow and consolidates them.
        -   Evaluates whether any queue processing failed and assigns subflow outputs accordingly.
    -   The BatchQueueType parameter determines which VROL queue each subflow polls through the RTSI API. All subflows use the same underlying RTSI operation: SIGetBatchQueueRequest \(/rsrv\_rolsi/api/SIGetBatchQueue\).
3.  Individual batch queue subflows executes the following actions related to polling and case matching:
    -   Builds the queue request: The subflow calls the Lookup Batch Queue Request Builder to construct the SIGetBatchQueueRequest payload with the appropriate BatchQueueType and page number \(starting at page 1\).
    -   Executes the RTSI API: It calls the Execute Visa Spoke Action Using Token Service action to submit the request to VROL via the configured Visa integration spoke.
    -   Parses the response: The Lookup Batch Queue Response Parser processes the returned FormatDQueueItem or FormatSQueueItem elements \(depending on the queue format\).
    -   Matches to the ServiceNow case: For each item in the queue response, the subflow looks up the matching Card Disputes Task Record in ServiceNow ServiceNow using the Visa Case Number returned in the queue item. It checks that the dispute service is **Initiate chargeback**, the case is active, and not already represented by a merchant.
    -   Updates the case: If a matching case is found, the subflow updates the Card Disputes Task Record and the Card Dispute Transaction Record in ServiceNow to reflect the new state — advancing the case in the dispute lifecycle \(e.g., marking that a dispute response has been received, a pre-arbitration has been filed, or an arbitration ruling has been issued\).
    -   Marks items as read: After processing all items on all pages, the subflow calls the Mark Batch Queue Items as Read Adapter subflow \(see Step 4 below\).

        **Note:** The queue data reflects the state of the case at the time it was added to the VROL batch queue — not necessarily the current real-time state. Fields such as User and Last Action Date may have changed since the item was queued. If a case has advanced further in VROL before the item is processed in ServiceNow, the batch queue item may be stale. Use Hypersearch \(SIHypersearchRequest\) to retrieve the current state of a case when needed.

4.  Executes Mark Batch Queue Items as Read Adapter subflow: Once all items from a queue are retrieved and processed, the subflow calls the Mark Batch Queue Items as Read Adapter subflow, which in turn calls the Mark Batch Queue Item as Read subflow to invoke the RTSI API SIMarkBatchQueueItemAsReadRequest \(/rsrv\_rolsi/api/SIMarkBatchQueueItemAsRead\). See the following four actions executed by this subflow:
    -   Prevents reprocessing: Once marked as read, an item is removed from the RTSI Batch Queue and will not be returned in the next polling cycle.
    -   Executes automated purge: If an item is not marked as read, VROL will automatically purge it from the batch queue after 10 days. After purging, the item can only be recovered using VROL RTSI Queues or Hypersearch — it will no longer appear in batch queue responses.
    -   Marks items in bulk: Items can be marked by individual BatchQueueItemSID or by entire BatchQueueType. A maximum of 400 items can be marked in a single SIMarkBatchQueueItemAsReadRequest \(configurable in VROL\).
    -   Resolves duplication of items in multiple batch queues: An item may appear in multiple batch queues. Marking it as read in one queue removes it from all batch queues for that VROL organization.

**Parent Topic:**[Financial Services Operations Integration with Visa subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/components-installed-with-the-financial-services-operations-integration-with-visa.md)

