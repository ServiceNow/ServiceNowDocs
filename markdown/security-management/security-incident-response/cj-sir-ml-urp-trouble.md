---
title: Troubleshooting Predictive Intelligence for User Reported Phishing
description: This section covers a few common problem scenarios.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage Predictive Intelligence for User Reported Phishing, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Troubleshooting Predictive Intelligence for User Reported Phishing

This section covers a few common problem scenarios.

-   Problem: I cannot modify the Predictive Intelligence configuration.

    Solution: Check if you have permissions to do so. You must login as a user with the ml\_admin role to modify thresholds. Some scenarios may require even higher privileges, like, for example, you need to modify the training data limit. For such scenarios, you must contact Customer Support for assistance.

-   Problem: The model training failed.

    Solution: Check if the URLs of the ML scheduler have been setup. Navigate to **System Properties** &gt; **All Properties** and check if the `glide.shared_service_scheduler.url` property has been configured.

-   Problem: Prediction results are not available on a security incident.

    Solution:

    -   Check if the predictor URL has been set up in the `glide.prediction_service.url` system property and make sure the data center matches with the URL.
    -   Check if the Predict User Reported Phishing Email scheduled job is active.

