---
title: Required components and plugins
description: To use Predictive Intelligence for User Reported Phishing, you must install the following applications
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage Predictive Intelligence for User Reported Phishing, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Required components and plugins

To use Predictive Intelligence for User Reported Phishing, you must install the following applications

|Plugin name|Minimum version|
|-----------|---------------|
|Security Incident Response|9.0.1 or 10.0.2|
|Predictive Intelligence|Orlando version|
|Predictive Intelligence for User Reported Phishing|10.0.2|

**Note:** The following new enhancements are available with Security Incident Response 10.4:

-   The ability to choose close codes from custom fields for model training.
-   The ability to explicitly activate predictions after model building.
-   The ability to generate a final verdict on the User Reported Phishing submission using a decision table. \(requires Security Operations Spoke 10.3.0\)

To use the new enhancements, you must upgrade the following applications:

|Plugin name|Upgrade to|
|-----------|----------|
|Security Incident Response|10.0.4|
|Predictive Intelligence for User Reported Phishing|10.3.1|

**New and updated tables**

-   sn\_sir\_ml\_urp\_config \(New\): Contains the configuration for the URP ML application.
-   sn\_sir\_ml\_urp\_feature \(New\): Records extracted from the sn\_si\_phishing email table.
-   sn\_sir\_ml\_urp\_feature\_import \(New\): Used to upload historical phishing email data.
-   sn\_si\_incident \(updated\): The following new fields were added:
    -   Prediction accepted
    -   Prediction result
    -   Confidence score
-   **Script includes**
    -   URPMLUtil: Retrieves configuration, run prediction job, and track prediction process.
    -   URPMLProcessor: Extracts and processes data from the sn\_si\_phishing\_email table.
    -   URPMLAction: Executes flow to accept prediction result.

