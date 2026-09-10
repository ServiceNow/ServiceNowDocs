---
title: Configuring case management in Sourcing and Procurement Operations
description: Configure case types, routing rules, specialist workspace, notifications, and AI skills in the Procurement Case Management module of the SPO Configuration Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/configuring-case-management-spo.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-08-23"
reading_time_minutes: 4
keywords: [procurement case management, case configuration, SPO configuration, case routing, Otto skills, Advanced Work Assignment]
breadcrumb: [Configure Sourcing and Procurement Operations, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configuring case management in Sourcing and Procurement Operations

Configure case types, routing rules, specialist workspace, notifications, and AI skills in the Procurement Case Management module of the SPO Configuration Console.

The **Procurement Case Management** module of the SPO Configuration Console groups configuration items into the following areas, in the same order they appear in the console navigation: **Employee Experience**, **Case Types**, **Assignment &amp; Routing**, **Playbooks**, **Notifications**, **Forms and Lists**, **Workspace**, **Properties**, and **Otto Skills**.

## Employee Experience

|Configuration|Description|
|-------------|-----------|
|Intake Forms|Configure the request forms employees use to submit procurement cases through the employee center. Edit an existing form or create one. Each form becomes a tile requesters see when browsing the procurement catalog.|
|Case Creation from Email|Configure the inbound email action to automatically create a procurement case when email is sent to a designated procurement mailbox.|
|Standard Ticket Configuration|Configure the information, fields, and request-specific details displayed on employee tickets. Define the actions, tabs, and supporting content available to employees. Create a consistent ticket experience that helps users track and manage their requests.|
|Stepper Statuses|Configure the plain-language progress labels requesters see as their procurement case moves through its lifecycle.|
|Employee Center Notification|Review and validate the employee center notifications used for procurement cases. Verify they are correctly scoped, render accurately, and fire only at the intended case states.|
|Case Resolution Acceptance|Configure the resolution acceptance workflow, including the auto-close period. Requesters can confirm the outcome of a case before it closes.|

## Case Types

A case type must exist before you can configure an SLA definition that references it.

|Configuration|Description|
|-------------|-----------|
|Create a Case Type, Configure Templates and Intake Forms|Register the choice value on the Case Type field. Create a matching template with default routing and state. Publish a record producer for the case type so employees can raise it from the employee center.|
|SLA Definitions|Create resolution and response SLA definitions for the case type, including breach escalation conditions. Time-based commitments are enforced and visible to specialists and requesters.|

## Assignment &amp; Routing

These configuration items control how procurement cases and work items are routed to specialists.

|Configuration|Description|
|-------------|-----------|
|Template Based Assignment|Configure assignment templates to route incoming procurement cases automatically to the correct team or specialist based on case type and requester attributes.|
|Assignment Rules|Configure platform-level assignment rules to route procurement cases to the correct group based on case attributes and requester details, such as department.|

The **Advanced Work Assignment** node groups the following configurations:

|Configuration|Description|
|-------------|-----------|
|AWA - Service Channels|Configure the Advanced Work Assignment \(AWA\) service channel to capture, queue, and surface procurement work items to specialists correctly.|
|AWA - Assignment Rules|Configure AWA assignment rules to distribute queued procurement work items to specialists based on skills, load, and case attributes.|
|AWA - Assignment Eligibility|Configure assignment eligibility to ensure only the right specialists or groups receive work from each AWA assignment rule.|
|AWA - Presence State|Configure presence states to indicate when specialists are available to receive work.|
|AWA - Rejection Reasons|Configure the rejection reasons specialists select, with optional mandatory-comment rules, when returning a pushed procurement work item.|
|AWA - Queues|Configure named queues and their priority order to buffer and route procurement work items to specialists in a controlled way.|

## Playbooks

Configure playbooks that guide fulfillers through the steps to resolve each procurement case type. Each playbook maps to a case type and defines the activities fulfillers must complete. Clicking a playbook opens it in the Playbook Designer in a new tab.

## Notifications

|Configuration|Description|
|-------------|-----------|
|Procurement Case Email Notifications|Configure outbound email notifications for key procurement case lifecycle events, including SLA breach warnings and escalations. ServiceNow Otto agent assistance is available through **Configure with AI**.|
|In-App Notifications for Cases|Configure in-app notifications to send real-time alerts to procurement specialists and requesters within the ServiceNow interface.|

## Forms and Lists

|Configuration|Description|
|-------------|-----------|
|Case Forms|Configure the procurement case form, including fields, UI policies, and read-only protections. Specialists use the well-structured form to manage cases.|
|Case List Views|Configure procurement case list views and publish them to the right roles. Specialists and managers see the columns relevant to their work.|

## Workspace

The Source-to-Pay Workspace is set up with default views and lists for procurement agents. Customize the workspace layout, navigation, and list configurations in UI Builder to match your team's workflow.

## Properties

Review and update system properties that control Procurement Case Management behavior from a single filtered list.

## Otto Skills

Configure AI skills to enhance procurement case management with automated summarization, email response drafting, and sentiment analysis.

**Note:** ServiceNow Otto uses AI to generate content. AI-generated content may be inaccurate. Review all AI-generated output before using it.

|Configuration|Description|
|-------------|-----------|
|Otto Skills — case summarization|Configure the case summarization skill to enable procurement specialists to generate instant, structured case summaries.|
|Otto Skills — email response|Configure the email response skill to enable procurement specialists to draft accurate, contextually relevant replies directly from the case.|
|Otto Skills — sentiment analysis|Configure the sentiment analysis skill to enable specialists and managers to monitor requester sentiment and intervene proactively. The skill automatically updates the Requester Sentiment field and triggers escalation alerts.|

ServiceNow Otto agent assistance, available through **Configure with AI**, also extends to some of the configuration items described earlier in this topic. An agent can create and edit records for Email Notifications, Create SLA Definitions, Case Forms, and Case List Views.

**Parent Topic:**[Configure Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-spo-apps.md)

