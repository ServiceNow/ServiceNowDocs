---
title: Exploring Financial Services Operations Integration with FRISS
description: With Financial Services Operations Integration with FRISS, your insurance company can embed the FRISS API for Claims in workflows, detect and prevent fraud, and improve your underwriting and claims processes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [FRISS, Integrate, Financial Services Operations \(FSO\)]
---

# Exploring Financial Services Operations Integration with FRISS

With Financial Services Operations Integration with FRISS, your insurance company can embed the FRISS API for Claims in workflows, detect and prevent fraud, and improve your underwriting and claims processes.

## Overview of the application

By using FRISS, you can detect fraud, assess your risks, and perform compliance management. You can also improve your profitability, customer satisfaction, and operational efficiency.

You can use the Financial Services Operations Integration with FRISS application to do the following tasks:

-   Integrate with the FRISS API for Claims to save the scores returned by FRISS into the relevant claim data object.
-   Detect fraud as you manage your claims cases.
-   Get real-time scores of your claims data at different stages of the claims process.
-   Use the user interface for portfolio monitoring.

## FRISS workflow

The following diagram is a workflow of the FRISS integration. The diagram shows the role that each layer plays in the Financial Services Operations application.

![Diagram of a high-level overview of the design of the FRISS integration and the role each layer plays in Financial Services Operations applications. For more details, refer to the following table.](../../fso-common/image/jha-thirdparty-integ.png "Workflow of Financial Services Operations integration with FRISS")

|Layer|Description|
|-----|-----------|
|Workflow Layer|Layer that contains the Commercial Lines Claims and Personal Lines Claims applications for triggering and storing fraud scores.|
|Adapter/Integration Layer|Layer that contains the Financial Services Operations Integration with FRISS subflow to execute the FRISS spoke actions and to provide a fraud score. Additional tables are added to this service to store the fraud score.|
|Spoke Layer|Layer that contains the FRISS spoke actions that use REST APIs to interact with FRISS. For more information on the FRISS spoke actions, see[FRISS Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/friss-spoke.md).|

## Financial Services Operations Integration with FRISS benefits

FRISS can help you solve the fraudulent activity that occurs in the insurance industry, such as false reporting of claims, staged accidents, and inflation of claims. Currently, investigations into these activities are often carried out manually, which results in a slow and inefficient claims process. This inefficient process increases the risk of human error and allows fraudulent activity to go undetected.

FRISS provides real-time, data-driven scores and insights that can help you to assess the inherent risks of your customers and interactions quickly. Because your services are primarily focused on Auto, Property, and General Liability claims, by using FRISS, you can build automated fraud detection into your claims processes. By scoring the claims in real time, Financial Services Operations Integration with FRISS helps your company to reduce the number of false positives, increase the number of avoided claims, and process the genuine claims immediately.

**Parent Topic:**[Financial Services Operations Integration with FRISS](fso-integration-with-friss-overview.md)

