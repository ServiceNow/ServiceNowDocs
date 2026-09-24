---
title: TPRM email notifications
description: Email notifications are sent automatically for TPRM events across due diligence requests, third-party risk assessments, issues and tasks, and third-party portal activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm\_email\_notification.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# TPRM email notifications

Email notifications are sent automatically for TPRM events across due diligence requests, third-party risk assessments, issues and tasks, and third-party portal activity.

Email notifications support timely awareness, review, and action across due diligence, third-party risk assessment, issue, task, and third-party portal activities.

These notifications are part of the base system. Availability and behavior may vary depending on configuration and installed TPRM applications. To customize notification content or recipients, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_CreateANotification.md).

**Note:** Notification names are listed as they appear in the application and might not reflect current terminology used elsewhere in the product documentation. Notification availability and behavior can vary depending on installed applications, plugins, and product configuration.

## Due diligence request

The following notifications are sent as a third-party due diligence request progresses through its lifecycle. Each lifecycle event sends a paired notification: one to internal staff \(assignee, contract negotiator, or both\) and one to the original requester.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Notify group – due diligence request received|A due diligence request record is created.|Assignment Group|
|Notify due diligence requester|A due diligence request record is created.|Opened By|
|Notify due diligence request assignee|**Assigned To** field is updated and is not empty.|Assigned To|
|Notify contract negotiator|**Contract Negotiator** field is updated and is not empty.|Contract Negotiator|
|Due diligence request re-opened|**Active** field changes to true and **State** is not **Contract Executed**.|Assigned To, Contract Negotiator|
|Due diligence request re-opened – requester notified|**Active** field changes to true and **State** is not **Contract Executed**.|Opened By|
|Due diligence request – additional due diligence requested|**State** changes from **Rejected** or **Contract Skipped** back to **Additional DD Requested**.|Assigned To, Contract Negotiator|
|Due diligence request – additional due diligence requested \(requester notified\)|**State** changes from **Rejected** or **Contract Skipped** back to **Additional DD Requested**.|Opened By|
|Due diligence request rejected|**State** changes to **Rejected**.|Assigned To, Contract Negotiator|
|Due diligence request rejected – requester notified|**State** changes to **Rejected**.|Opened By|
|Due diligence request contract executed|**State** changes to **Contract Executed**.|Assigned To, Contract Negotiator|
|Due diligence request contract executed – requester notified|**State** changes to **Contract Executed**.|Opened By|
|Due diligence request contract skipped|**State** changes to **Contract Skipped**.|Assigned To, Contract Negotiator|
|Due diligence request contract skipped – requester notified|**State** changes to **Contract Skipped**.|Opened By|

## Approval \(due diligence request\)

The following notification is sent when an approval record is created for a due diligence request.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Approval request created|An approval record is created for a due diligence request.|Approver|

## Due diligence case

The following are agent-sent email templates, not automatically triggered notifications. An agent selects and sends the applicable template from the case record after a due diligence case is reviewed.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Close due diligence case email|Sent manually by an agent after a due diligence case is approved.|Requested By|
|Reject due diligence case email|Sent manually by an agent after a due diligence case is rejected.|Requested By|

## Third-party risk assessment

The following notifications are sent as third-party risk assessments are assigned, submitted, and responded to.

Different notifications can be sent when assessments are assigned, questionnaire requests are distributed, contacts are reassigned, and responses are received.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Third-party risk assessment assigned|**Assigned To** field is updated on an assessment record by a user other than the assignee.|Assigned To|
|Vendor assessment submitted to third party|An assessment or questionnaire is sent or resubmitted to the third-party contact.|Third-party contact or questionnaire assignees|
|Vendor assessment new request to vendor|A questionnaire or document request is sent to a third party.|Questionnaire assignees|
|Vendor assessment responses received|**State** changes to **Responses Received**.|Assigned To|
|Vendor risk request assigned|A third-party portal user adds or reassigns a stakeholder on a questionnaire request from the Assessment Detail or SAE Assessment Detail widget.|Newly added contact|

## Third-party tiering assessment

The following notifications are sent as third-party tiering assessments are assigned and completed.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Third-party tiering assessment sent to assessor|A tiering questionnaire is sent to an assessor.|Assessor|
|Notify assignee when questionnaire done|**State** changes to **Tiering Assignment** after all tiering questionnaires are completed.|Assigned To|

## Internal risk questionnaire \(IRQ\)

The following notification is sent when responses to an internal risk questionnaire are completed.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Notify assignee when questionnaire complete – IRQ|**State** changes to **Response Received** on an internal assessment record.|Assigned To|

## Third-party assessment reminders

The following notifications are sent by scheduled reminder logic as third-party assessment and questionnaire due dates approach or pass.

**Note:** Starting with version 23.0.x, the reminder flow no longer errors when a questionnaire's due date isn't yet populated. Reminder notifications now send correctly once the due date is set.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Vendor assessment responses overdue|A scheduled reminder flow detects that an assessment's responses are past due.|Primary contact|
|Vendor assessment responses due in 1 week|A scheduled reminder flow detects that an assessment response due date is approaching.|Primary contact|
|Vendor assessment responses due in 3 days|A scheduled reminder flow detects that an assessment response due date is approaching.|Primary contact|
|Questionnaire due reminder|A tiering questionnaire is due within one day.|Tiering assessment assessors|

## Third-party risk issue

The following notifications are sent when a third-party risk issue is assigned to an internal user or a third-party or engagement contact.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Vendor risk issue assigned \(internal\)|**Assigned To** field is updated on an issue record by a user other than the assignee.|Assigned To|
|Vendor risk issue assigned \(external\)|**Vendor Contact** field is updated on an issue record by a user other than the vendor contact.|Third-party contact|

## Third-party risk task

The following notifications are sent when a third-party risk task is assigned to an internal user or a third-party or engagement contact.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Vendor risk task assigned \(internal\)|**Assigned To** field is updated on a task record by a user other than the assignee.|Assigned To|
|Vendor risk task assigned \(external\)|**Vendor Contact** field is updated on a task record by a user other than the vendor contact.|Third-party contact|

## Third-party risk management

The following notifications are sent to third-party risk managers when configured risk or scoring rules are triggered, and when a Software Bill of Materials \(SBOM\) file upload fails processing.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Email vendor manager – rule triggered|A configured third-party tier rule is triggered on an assessment.|Vendor Risk Managers group|
|Email vendor manager – score changed|A risk-scoring rule changes an assessment's normalized score or rating.|Recipient field, Vendor Risk Managers group|
|SBOM upload failure notification|An uploaded SBOM file fails processing; the associated assessment is reopened for resubmission.|SBOM instance primary owner|

## Third-party portal

Portal actions trigger the third-party risk assessment notifications described in the Third-party risk assessment notifications table. The following portal actions trigger those notifications.

|Portal action|Trigger condition|Downstream notification|
|-------------|-----------------|-----------------------|
|Stakeholder added or reassigned on a questionnaire request|A third-party portal user adds or changes a contact on an assessment or SAE assessment through the Assessment Detail or SAE Assessment Detail widget.|Vendor risk request assigned|
|Questionnaire response saved|A third-party portal user saves progress on a questionnaire response.|No notification identified.|
|Questionnaire submitted|A third-party portal user submits a completed questionnaire.|No notification identified.|

**Parent Topic:**[Third-party Risk Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-reference.md)

