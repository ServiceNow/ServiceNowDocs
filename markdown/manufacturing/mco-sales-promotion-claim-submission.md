---
title: Sales promotion claim submission use case
description: Use case scenarios demonstrate when and how to use the Dealer portal application to submit a sales promotion claim. It provides practical examples of common sales promotion management situations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-sales-promotion-claim-submission.html
release: australia
topic_type: concept
last_updated: "2026-03-16"
reading_time_minutes: 2
breadcrumb: [Sales promotion, MCO core, Explore, Manufacturing Commercial Operations]
---

# Sales promotion claim submission use case

Use case scenarios demonstrate when and how to use the Dealer portal application to submit a sales promotion claim. It provides practical examples of common sales promotion management situations.

## Scenario

Sophie, a dealer sales agent, must submit sales promotion claims for vehicles sold at the dealership. The claims include a Senior Citizen Promotion \($1,500\) and a Trade-In Promotion \($2,500\). Dealers submitting sales promotion claims might encounter some of the following challenges:

-   Manual processes: Disconnected systems and scattered documentation cause delays and errors.
-   Claim complexity: Single vehicles qualifying for multiple promotions requires careful tracking.
-   Data quality: Missing or incorrect information leads to rejections and resubmissions.
-   Lack of visibility: Limited access to claim status after submission.

## Solution

Sophie uses the Manufacturing Commercial Operations \(MCO\) Dealer Portal to submit sales promotion claims efficiently:

1.  Access: Opens the Dealer Portal and navigates to Sales Promotion Claims.
2.  Upload: Downloads the bulk upload template \(promotion ID, external ID, sale price, currency, asset serial number\) and completes it with both vehicle details.
3.  Review: Submits the file and reviews auto-filtered eligible promotions for each vehicle.
4.  Select: Chooses Senior Citizen Promotion and Trade-In Promotion from eligible options.
5.  Configure: Enters claim amounts within defined ranges \($2,500 for trade-in, $1,500 for senior citizen\).
6.  Complete: Fills structured questionnaires with auto-populated dealer information and required details using preconfigured drop-downs. Example: customer age and SSN for Senior Citizen; vehicle serial number, make, model, year, trim for Trade-In.
7.  Document: Uploads required supporting documents \(vehicle title\) within the claim form.
8.  Track: Submits the claim and monitors status in real-time, views OEM comments, or cancels if needed.

The [Using dealer portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-use-dealer-portal.md) reduces manual effort and improves accuracy.

## Benefits

|Without MCO|With MCO Sales Promotion|
|-----------|------------------------|
|Manual claim submission for each vehicle|Bulk upload submits multiple claims in one action.|
|Uncertainty about eligible promotions|Auto-filtered promotions display only valid options.|
|Incomplete information causes rejections|Structured questionnaires and validation ensure complete data.|
|No visibility into claim status|Real-time tracking shows claim progress and OEM feedback.|
|Scattered documentation across systems|Centralized file uploads keep all documents with the claim.|
|Range and validation errors|Value-range validation prevents overages and data inconsistencies.|

## Outcome

Sophie submits a complete claim with two incentives. Bulk upload, automated filtering, and structured questionnaires reduce preparation time and rejection risk, enabling faster processing and reimbursement.

