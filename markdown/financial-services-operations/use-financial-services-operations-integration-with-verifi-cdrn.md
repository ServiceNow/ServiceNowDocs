---
title: Using Financial Services Operations Integration with Verifi application
description: As a dispute agent learn how to initiate a dispute transaction using the Financial Services Operations Integration with Verifi application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-07"
reading_time_minutes: 2
breadcrumb: [Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# Using Financial Services Operations Integration with Verifi application

As a dispute agent learn how to initiate a dispute transaction using the Financial Services Operations Integration with Verifi application.

## Before you begin

Role required: dispute\_agent\_connector

## About this task

The Financial Services Operations Integration with Verifi application is built on four sequentially orchestrated subflows. Each maps to a specific Verifi REST endpoint and triggers at a defined point in the dispute workflow. See [../reference/api-subflows-and-endpoints.md](../reference/api-subflows-and-endpoints.md) for more information.

## Procedure

1.  To check the merchant eligibility, the agent opens the **Review Participating Merchant Alerts** task on the dispute record.

    -   The system initiates Subflow 1.
    -   If the merchant is not eligible no CDRN case is created. The **Create alert case** UI action is not displayed. The agent proceeds with the standard dispute lifecycle toward the chargeback process.
    -   **Get case details** on the **Alert Merchant** task is used to fetch the case details from the Verifi system on demand.
2.  The system creates a case.

    -   The system initiates Subflow 2.
    -   If the **Create Case** API is successful, the task status transitions to **Awaiting External Info** and the caseId is stored.
    -   If the **Create Case** API fails, the **Create alert case** UI action appears for manual retry.
3.  The system polls for merchant response.

    Define the required schedule in Verifi Queue Scheduler Flow. Activate this flow to poll the Verifi system at constant intervals.

    The required schedule for polling the Verifi cases from ServiceNow® instance can be defined in this flow. Activate this to poll the Verifi system at constant intervals

    -   The system initiates Subflow 3.
    -   The system polls until the case status changes to **EXPORTING** indicating that the merchant has responded or the 72-hour SLA window expires.
    -   If the status is **EXPORTING** the system retrieves statusCode and auto-fills the **Outcome** and **Description**.
    -   If 72 hours timeout occurs, the agent closes the task after verifying the merchant response. The system proceeds toward the chargeback flow \(statusCode 910: **Case declined due to SLA — no response from merchant** \)
4.  The system displays the merchant response and populates the field based on agent action or system response.

    -   The **Merchant Response** field is auto-populated to one of the following values: Accepted Dispute, Declined Dispute.
    -   **Total Refund Amount** field is auto-populated.
    -   Based on the cardholder's decision, the agent selects **Accept** or **Rejected** from the **Customer Decision** field.
    -   The task status changes from **Awaiting External Info** to **Work in Progress**.
5.  The system closes the case and ends polling.

    -   The system initiates Subflow 4.
    -   The **Status** is changed to **CLOSED**.
    -   This confirms to Verifi that the issuer has received and processed the merchant response.
    -   The case is excluded from further polling.
6.  Record the customer decision based on the cardholder's response to the merchant's offer.

    -   **Accepted**: The cardholder agrees with the merchant response. The case closes and the dispute is resolved.
    -   **Rejected**: The cardholder disagrees with the merchant response. The case proceeds to the chargeback process.

**Parent Topic:**[Financial Services Operations Integration with Verifi](../concept/financial-services-operations-verifi-cdrn-integration-app-landing-page.md)

