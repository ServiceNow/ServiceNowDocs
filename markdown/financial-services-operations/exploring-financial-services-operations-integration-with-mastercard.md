---
title: Exploring Financial Services Operations Integration with Mastercard
description: Use the Financial Services Operations Integration with Mastercard to automate and simplify how financial institutions manage Mastercard disputes. This integration leverages Mastercard Spoke actions and Mastercom APIs to support a range of dispute lifecycle events and ensure alignment with Mastercard specific business rules.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mastercard, Integrate, Financial Services Operations \(FSO\)]
---

# Exploring Financial Services Operations Integration with Mastercard

Use the Financial Services Operations Integration with Mastercard to automate and simplify how financial institutions manage Mastercard disputes. This integration leverages Mastercard Spoke actions and Mastercom APIs to support a range of dispute lifecycle events and ensure alignment with Mastercard specific business rules.

## Overview of Financial Services Operations Integration with Mastercard

Financial Services Operations Integration with Mastercard helps manage disputes easily and efficiently within ServiceNow. It uses Mastercard Spoke actions to support key steps in the dispute process, such as searching transactions, creating claims and chargebacks, handling pre-arbitration and arbitration, and reporting fraud.

You can find more information about the Mastercard Spoke actions and setup details in the [Mastercard Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/mastercard-spoke.md) documentation.

The application includes predefined subflows for common use cases, and you can extend them to meet custom requirements. Its adapter layer simplifies the connection to dispute workflows, helping you resolve cases faster and more accurately.

**Important:** The Financial Services Operations Integration with Mastercard provides predefined subflows. However, these subflows are not yet integrated with the Workspace.

## Use Mastercard Spoke actions and APIs

![Diagram showing the interaction of issuers, acquirers, cardholders, merchants, and the global clearing management system through the MastercomAPI.](../image/mastercard-integration-overview.png "Overview of Mastercard and Mastercom API")

The Mastercard Spoke includes actions that use Mastercom APIs to automate key dispute events, such as:

-   Collaboration
-   First chargebacks
-   Second presentments
-   Arbitration
-   Pre-arbitration

## Financial Services Operations Integration with Mastercard benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Automatically connects workflows with Mastercom and shows real-time updates to track cases easily.|[Enables seamless integration with Mastercard’s Mastercom API Suite and Mastercom Extended APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/mastercard-spoke.md)|Administrator|
|Uses predefined subflows with built-in error handling and retry logic to reduce development time and errors.|[Financial Services Operations Integration with Mastercard subflows](../reference/financial-services-operations-integration-with-mastercard-subflows.md)|Administrator|

## What to explore next

To learn more about configuring Financial Services Operations Integration with Mastercard, see:

-   [Mastercard Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/mastercard-spoke.md)
-   [Configuring Financial Services Operations Integration with Mastercard](configuring-financial-services-operations-integration-with-mastercard.md)
-   [Components installed with the Financial Services Operations Integration with Mastercard](../reference/components-installed-with-the-financial-services-operations-integration-with-mastercard.md)

