---
title: AI governance email notifications
description: Email notifications are sent automatically when specific events occur across AI governance workflows, including AI Control Tower, AI Risk and Compliance, and inherited Risk Management processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc\_email\_notifications.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-03-31"
reading_time_minutes: 5
breadcrumb: [Reference, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI governance email notifications

Email notifications are sent automatically when specific events occur across AI governance workflows, including AI Control Tower, AI Risk and Compliance, and inherited Risk Management processes.

Email notifications are sent automatically when specific events occur across AI governance workflows. These notifications help ensure timely awareness, review, and action across governance, risk, and compliance activities.

These notifications are part of the base system. Availability and behavior may vary depending on configuration and inherited Risk Management workflows. To customize notification content or recipients, see .

## AI Asset Approval Request

The following notifications are sent for events related to AI asset approval requests and associated approval tasks.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Approval request – work note added|A work note is added to an AI Asset Approval Request record.|Assigned To|
|Approval request – approved / rejected|An AI Asset Approval Request is approved or rejected.|Asset Managed By|
|Approval request – comment added|A comment is posted on an AI Asset Approval Request record.|Asset Managed By|
|Approval request created – unassigned \(Stewards\)|An AI Asset Approval Request is created and remains unassigned.|AI Stewards Group|
|Approval request created – unassigned \(Asset Manager\)|An AI Asset Approval Request is created and remains unassigned.|Asset Managed By|
|Approval task created|An AI Asset Approval Task record is created.|Assigned To|

## AI Assessment / Risk Assessment

The following notification is sent when AI Assessments or Risk Assessments are cancelled using a bulk action.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Bulk assessment cancellation|One or more AI Assessments or Risk Assessments are cancelled in bulk from the related list.|AI Analyst and Assigned To \(AI Assessments\); AI Analyst \(Risk Assessments — Assigned To notification handled by Risk Management\)|

## AI Asset

The following notification is sent when an AI asset is retired or cancelled.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|AI asset retirement / cancellation|An AI Asset record transitions to Retired or Cancelled state.|AI Analyst, Policy Exception Owners, Issue Owners, AI Case Analysts|

## Policy Exception

The following notifications are sent as Policy Exception records progress through review, approval, extension, and closure states.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Requester notified – exception rejected|State changes to Rejected.|Opened By, Watchlist|
|Extension request sent to approver|Extension Date is updated and Substate changes to Under Review.|Assigned To, Watchlist|
|Watchlist notified – new comment|Additional Comments field is updated.|Watchlist|
|Policy exception closed|State changes to Closed.|Assigned To, Opened By|
|Approver notified for review|State changes from Risk Assessment to Review, and an Approver is assigned.|Assigned To|
|Requester notified – extension rejected|Substate changes to Extension Rejected.|Opened By, Watchlist|
|Confidential users notified|Confidential flag or related confidential-user criteria are met on the Policy Exception.|Confidential Users|
|Requester notified – exception approved|State changes to Approved and Extension Date is empty.|Opened By, Watchlist|
|Requester notified – extension approved|Substate changes to Extension Approved, Valid To date is updated, and Extension Date is populated.|Opened By, Watchlist|
|Assignment group notified|Approval Group changes while State is not New, or State changes from New to Analyze while Extension Date is empty.|Assignment Group|
|Approver group notified for review|State changes from Risk Assessment to Review and no individual Approver is assigned.|Assignment Group|
|Requester provided more information|State is Analyze and Substate changes from Awaiting Requester Information to none.|Assigned To, Watchlist|
|Exception period 80% elapsed|A scheduled job detects that 80% of the Policy Exception validity period has elapsed.|Opened By, Assigned To|
|Approver changed|Assigned To field is updated while State is not New.|Assigned To, Watchlist|
|Risk managers notified for assessment|State changes to Risk Assessment.|Risk Managers Group|
|Watchlist notified – BU approval pending|State changes to Awaiting Approval.|Watchlist|
|Requester notified – more info needed|State is Analyze and Substate changes to Awaiting Requester Information.|Opened By, Watchlist|

## Smart Control Attestation

The following notification is sent when a Smart Control Attestation is assigned.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Attestation assigned|A Smart Control Attestation record is assigned to the Control Owner.|Control Owner, Attestation Respondents|

## Approval \(Policy Exception\)

The following notifications are sent when approval records are created for Policy Exceptions.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Verification request created|A verification-type Approval record is created for a Policy Exception.|Approver|
|Approval request created|An approval-type Approval record is created for a Policy Exception.|Approver|

## Risk Assessment

The following notifications are sent as Risk Assessments progress through their lifecycle.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Reassessment requested|State changes from Awaiting Approval back to an assessment state. \(Inherent, Control, or Residual Assessment\)|Assessor|
|Final notice – due date passed|A scheduled job detects that the Risk Assessment due date has elapsed with no completion.|Assessor, Entity Owner|
|Approver changed \(risk-based\)|Approver field is updated on a risk-based assessment.|Approver, Entity Owner|
|Reassessment completed|Substate changes from Reassessment Requested to none.|Approver|
|Assessing group notified|State changes to Ready to Assess for a risk-based assessment.|Assessor Group|
|Approver changed \(object-based\)|Approver field is updated on an object-based assessment.|Approver|
|Assessment cancelled – assessor notified|A Risk Assessment record is cancelled.|Assessor|
|Assessor notified – ready to assess|State changes to Ready to Assess.|Assessor|
|Enterprise assessment – assessor notified|An enterprise-level Risk Assessment is assigned or reaches readiness.|Assessor|
|Assessment approved / monitoring|State changes to Monitor.|Entity Owner, Assessor|
|Upcoming due date reminder|A scheduled job detects that the Risk Assessment due date is approaching.|Assessor, Entity Owner|
|Assessment cancelled – owner notified|A Risk Assessment record is cancelled.|Assessor, Approver|
|Assessor changed \(risk-based\)|Assessor field is updated on a risk-based assessment.|Entity Owner, Assessor|
|Assessor changed \(object-based\)|Assessor field is updated on an object-based assessment.|Assessor|

## Bulk Risk Assessment

The following notifications are sent for lifecycle events associated with Bulk Risk Assessments.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Project rejected / sent back|State changes from Awaiting Approval back to Assessment.|Assessor, Owner|
|Owner changed|Owner field is updated on the Bulk Risk Assessment record.|Owner|
|Assessment reassigned – owner notified|Assessor field is updated on the Bulk Risk Assessment record.|Owner|
|Assessment phase started|State changes from Scope Risk to Assessment.|Assessors, Assessor Group, Owner|
|Assessment reassigned – assessor notified|A Bulk Risk Assessment is reassigned to a different Assessor.|Assessor|
|Project completed|State changes to Completed.|Owner|
|New owner notified|Owner field is updated on the Bulk Risk Assessment record.|Owner|
|Project created|A new Bulk Risk Assessment record is created.|Owner|
|Reassign assessor notification|Assessor field is updated on the Bulk Risk Assessment record.|Assessor|
|Assessment updated – owner notified|A Bulk Risk Assessment record is updated.|Owner|

## Approval \(Risk Assessment\)

The following notifications are sent when approvals are requested for individual or bulk Risk Assessments.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Approver notified – bulk risk approval|An Approval record is created requesting sign-off on a Bulk Risk Assessment.|Approver|
|Approver notified – risk assessment approval|An Approval record is created requesting sign-off on an individual Risk Assessment.|Approver|

**Parent Topic:**[AI Risk and Compliance reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-reference.md)

