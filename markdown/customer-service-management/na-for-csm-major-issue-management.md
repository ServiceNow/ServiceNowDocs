---
title: Now Assist for CSM Major Issue Management
description: As a Major Case Manager, you can review and approve or reject a proposed major case when a high-priority case is created with no parent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/na-for-csm-major-issue-management.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Now Assist for CSM Major Issue Management

As a Major Case Manager, you can review and approve or reject a proposed major case when a high-priority case is created with no parent.

The Major Issue Management \(MIM\) agentic workflow evaluates each qualifying case against existing major cases and related cases in your system. Based on what the AI detects, it does one of three things: links the case to an existing major case automatically, proposes a new major case for your review, or determines there is no major case to propose.

## Trigger conditions

Once the workflow is activated, it triggers automatically when a case meets both of the following criteria:

-   Priority is **P1** or **P2**
-   The case has **no parent case**

**Note:** You can configure the similarity thresholds and other detection parameters. For more information see [Configure Now Assist for CSM Major Issue Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-na-for-csm-major-issue-management.md).

## How the workflow runs

The workflow runs in two sequential stages. Each stage uses a different AI search profile and similarity threshold.

-   **Stage 1 — Direct major case search**

    The workflow retrieves the new case details and runs a similarity search against known major cases using the `MIM_MAJOR_CASE_PROFILE` \(default threshold: 0.75\).

    If the case meets the similarity threshold, Option 1 applies and the workflow ends.

-   **Stage 2 — Indirect similarity search**

    If Stage 1 finds no match, the workflow runs a second search using the `MIM_NON_MAJOR_CASE_PROFILE` \(default threshold: 0.70\), comparing the new case against non-major cases that may already be linked to a major case.

    If this search returns no results, the workflow ends with no action. If results are found, the workflow checks the similarity pattern to determine whether Option 2 or Option 3 applies.


## Option 1: Direct match to a major case

The workflow found that the new case closely resembles an existing active major case \(similarity meets the `MIM_MAJOR_CASE_PROFILE` threshold\).

**What the workflow does:**

-   Sets the Suggested Major Case field on the new case to the matching major case
-   Adds a worknote summarizing the match
-   Updates the business impact on the case

No action required. The case is linked automatically. You can monitor it through the standard major case lifecycle.

## Option 2: Indirect match through a child case

Stage 1 found no direct match, but the Stage 2 search found that the new case resembles cases already linked as children to an existing major case.

**What the workflow does:**

-   Sets the **Suggested major case** field on the new case to the existing active major case
-   Adds a worknote summarizing the indirect association
-   Updates the business impact on the case

No action required. The case is linked automatically. Monitor it through the standard major case lifecycle.

## Option 3: Propose a major case

The workflow found no existing major case to link this case to, but the pattern of similar cases meets the threshold required to propose a new major issue.

**What the system does:**

-   Sets `major_case_state` to **Proposed** on the new case
-   Sets the **Suggested major case** field on all similar cases to this new case
-   Adds a worknote and updates business impact across all related cases
-   Writes the `suggested_major_case` value to the `sn_customerservice_case` record
-   Triggers the Major Issue Management lifecycle

The proposed major case appears in the major case manager queue for review, and you can approve or reject it. See Review a proposed major case for more information.

