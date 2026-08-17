---
title: Dealer and OEM support custom API
description: Use case scenario demonstrating dealer and OEM support for warranty claims using a custom API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-dms-integration-custom-api-use-case.html
release: australia
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 2
keywords: [DMS integration, custom API, dealer warranty claims]
breadcrumb: [DMS integration, Integrate, Manufacturing Commercial Operations]
---

# Dealer and OEM support custom API

Use case scenario demonstrating dealer and OEM support for warranty claims using a custom API.

## Scenario

Alectri, an automotive OEM, relies on its dealer network to submit repair order details for warranty claims. A customer brings a vehicle to a dealership for a covered repair. The service advisor then creates a repair order in the dealer management system \(DMS\) for a technician to investigate. The technician identifies the parts and labor required, fixes the vehicle, and updates the repair order in the DMS with the labor and parts used.

Turning that repair order data into a claim, across a dealer network that doesn't share one DMS setup, creates several challenges:

-   Manual data submission: Dealers manually submit repair order details to the OEM to create each claim.
-   Manual claim creation: The OEM manually creates the claim from the submitted repair order details.
-   Integration rigidity: A fixed integration standard doesn't accommodate every dealer's DMS setup.

## Solution

Alectri configures a custom API in the Dealer Integration Framework to retrieve repair order details directly from each dealer's DMS. MCO for Warranty Claims uses this data to automatically create the resulting claims. The integration follows four phases:

1.  Configure: Build the custom API configuration in the Dealer Integration Framework to match the dealer's DMS setup.
2.  Retrieve: Pull repair order details from the DMS, including repair performed, part codes used, labor codes used, and external services used.
3.  Create: Automatically create a claim in MCO using the retrieved repair order details.
4.  Monitor: Track claim creation and status in real time as repair order data arrives from each dealer.

The [Set up inbound DMS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-dms.md) describes how to set up the custom API configuration and map STAR XML payloads to MCO records.

## Benefits

Compare the impact of using MCO DMS integration.

|Without MCO|With MCO DMS integration|
|-----------|------------------------|
|Dealer submits repair order details to the OEM to create a claim.|The custom API configuration built in the Dealer Integration Framework retrieves the repair order details.|
|OEM creates the claim from the submitted repair order details.|MCO automatically creates the claim using the retrieved repair order details.|
|OEM is limited to a fixed integration standard regardless of their DMS setup.|OEM configures the API to match their own Dealer Integration Framework setup.|

## Outcome

After the technician updates the repair order in the DMS, Alectri's custom API configuration in the Dealer Integration Framework retrieves the repair order details. MCO then automatically creates the claim using the retrieved details, without manual submission or a fixed integration standard.

