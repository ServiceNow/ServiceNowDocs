---
title: Alternative dispute resolution management
description: Use the Alternative Dispute Resolution \(ADR\) case to resolve customer disputes efficiently while confirming transparency, accountability, and regulatory conformance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Alternative dispute resolution management

Use the Alternative Dispute Resolution \(ADR\) case to resolve customer disputes efficiently while confirming transparency, accountability, and regulatory conformance.

## ADR overview

ADR is a specialized complaint management system within ServiceNow, Inc.'s CSM/FSM workspace. An ADR in the context of customer complaints is a formal process used to address and resolve disagreements between a customer and an organization. ADR extends the complaint case functionality to handle dispute resolution processes. The ADR case provides an end-to-end workflow that includes the necessary steps to resolve a customer complaint.

## ADR workflow

The ADR workflow begins when a customer raises a complaint regarding a product, service, billing issue, or contractual matter. As an ADR manager records the escalated complaint, captures requester details, the reviews the related complaint cases, and gathers relevant evidence. Then, communicate with the customer to understand the issue clearly and propose a solution. The objective is to investigate fairly, provide a justified response, and reach a mutually acceptable solution. If the customer accepts the resolution plan, the ADR manager creates the case tasks and resolves the customer issue. If the customer rejects the resolution plan and chooses to escalate the issue externally, the ADR manager issues and shares a deadlock letter with the customer.

|Component|Description|
|---------|-----------|
|ADR case type|Captures all necessary details, including the ADR category, customer information, and previous interaction history. Also includes partner contact information for disputes involving third parties.|
|Fact capture|Captures all facts, investigation details, findings, and proposed resolutions, such as credit notes or bill corrections.|
|Service Level Agreements \(SLAs\)|Defined and adhered to based on the severity of the ADR, confirming issues are addressed within specified timeframes to maintain customer trust and satisfaction.|
|Audit trail|Maintains a comprehensive record of all interactions and root cause analysis \(RCA\) details, including evidence, for reporting and compliance purposes.|
|Deadlock letter|Created in cases where a deadlock is reached, capturing the history and RCA of the ADR and informing the customer of the deadlock situation and dispute details.|

## ADR stages and activities

The ADR case record uses the Case Playbook for Complaints feature to capture the details and execute the workflow. To learn more about the Case Playbook for Complaints, see [Case Playbook for Complaints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-complaint-overview.md). The following table lists the stages and activities that agents can use to resolve customer issues in the ADR case record.

<table id="table_nrj_z2s_llb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

**Intake** Guides the agent to collect the needed to create the ADR case.

</td><td>

Capture initiator details

</td><td>

Captures the details of the requester such as contact information, communication channel, and involved parties.

</td></tr><tr><td>

 

</td><td>

Capture ADR information

</td><td>

Captures the details of the complaint such as product or service details, complaint date, complaint description, and any other additional information relevant to the complaint.

</td></tr><tr><td>

 

</td><td>

Upload documents

</td><td>

Captures any evidence related to the complaint.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

Displays the details of the email that was automatically sent to the customer at the completion of the Intake stage.

</td></tr><tr><td>

**Investigate**Enables the agent to do the initial troubleshooting on the case.

</td><td>

Lookup record history

</td><td>

Captures the complaint case records related to the customer complaint.

</td></tr><tr><td>

 

</td><td>

Analyze linked fats

</td><td>

Analyzes the linked records details to understand the complaint details.

</td></tr><tr><td>

**Resolution**Manages the activities for case resolution.

</td><td>

Propose resolution plan

</td><td>

Proposes a resolution for the complaint and sends the details to the customer.

</td></tr><tr><td>

 

</td><td>

Resolution feedback

</td><td>

Captures the feedback from the customer after sending the resolution plan to the customer.

</td></tr><tr><td>

 

</td><td>

Generate deadlock letter

</td><td>

If customer rejects the resolution plan, this activity enables you to create a deadlock letter and share with the customer. Customer may escalate the issue with an external authority.

</td></tr><tr><td>

OutcomeEnables the agent to create the case tasks and send to different back-office teams for resolution.

</td><td>

implement resolution

</td><td>

If customer accepts the resolution plan, this activity enables you to create a deadlock letter and share with the customer.

</td></tr><tr><td>

**Closure**Close the activities for closing the case.

</td><td>

Close ADR

</td><td>

When the customer accepts the resolution, the Outcome stage completes and the Close stage is also marked as complete. When the customer rejects the resolution, the deadlock letter is created, and the Close stage is also marked as complete.

</td></tr></tbody>
</table>## Using ADR case

To learn more about how to use ADR case, see [Using alternative dispute resolution case](use-alternative-dispute-resolution-case.md).

**Related topics**  


[Customer service case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-types.md)

