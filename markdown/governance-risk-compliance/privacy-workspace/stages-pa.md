---
title: Workflow of a processing activity
description: A processing activity workflow helps the privacy analysts to manage the life cycle of a processing activity.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Uses of a processing activity, Reference, Privacy Management, Governance, Risk, and Compliance]
---

# Workflow of a processing activity

A processing activity workflow helps the privacy analysts to manage the life cycle of a processing activity.

The following section explains the different stages of the processing activity workflow.

**Note:** Privacy analysts who do not own the processing activity can only view the processing activity. They cannot edit it.

## New

This is a state to confirm if the business application, business process, vendors, or business service must be considered for determining privacy compliance​. A processing activity is in this state only when it is created manually. A privacy manager or a privacy analyst can create a processing activity manually and then confirm it as a processing activity based on their analysis. In this stage, the following fields of the processing activity can be modified:

-   **Name**
-   **Justification**
-   **Privacy analyst**
-   **Entity**: Only when this field is filled, and the processing activity form is saved. After saving the form, the privacy manager or a privacy analyst can move the processing activity the **Discover** state.

## Discover

In this state, the privacy manager or the privacy analyst, who owns the processing activity, can understand further details about the processing activity such as, why and how a processing activity is processing personal information. These details are collected by sending privacy assessments. Based on the responses, they apply the right set of controls. The following is the list of activities that can be performed on the processing activity form in this state.

-   Send privacy assessments.
-   Update the processing activity **Details** section based on the assessment responses.
-   Assign the processing activity to one of the key stakeholders for the key stakeholders to update the details, the PI-tagged information objects, and the key stakeholders.

    **Note:** You can assign the processing activity to those users who have the sn\_privacy.business\_user role.

-   Review the controls applied based on the privacy assessment responses.
-   Add or remove additional controls as necessary.

The processing activity then moves to the **Review** state.

## Review

In this state, the privacy manager or the privacy analyst, who owns the processing activity, sends control attestations and reviews the compliance posture based on the attestation responses and issues that are created due to non-compliant controls​. The following is the list of activities performed on the processing activity form by a privacy manager or the privacy analyst who owns the processing activity.

-   Update the processing activity Details section based on the assessment responses.
-   Associate information objects and capture additional details related to the information objects based on the assessment responses.
-   Review the controls applied automatically based on the privacy assessment responses, and add or remove additional controls as necessary.
-   Send control attestations and track issues and policy exceptions.

## Monitor

This is a state to track the processing activity for continuous monitoring​. The indicator functionality is used for continuous monitoring. When the processing activity is in this state, the privacy analyst can move the processing activity back to **Discover** or **Review** state based on the processing activity updates that must be assessed by the privacy analyst or the privacy manager. The following is the list of activities that can be performed on the processing activity form by a privacy manager or the privacy analyst who owns the processing activity.

-   Auto execution of indicator functionality to continuously monitor controls associated with processing activity.
-   Create, manage issues, and track issues.

**Note:** When a new privacy assessment is sent for a processing activity while it is in the **Monitor** state, the system automatically moves the processing activity to the **Discover** state.

## Retire

This is a state to retire the processing activity when the respective business application or business process is no longer used in the organization. When moved to this state, all the controls associated with the processing activity are retired. The privacy team cannot make any updates to a processing activity in the retired state. When an entity gets inactivated, the related processing activity is also automatically moved to the Retired state.

**Parent Topic:**[Uses of a processing activity in Privacy Management](states-of-pa.md)

