---
title: Associating an AI-recommended citation to an open regulatory alert
description: Associate a citation to an open regulatory alert by using the GRC: Predictive Intelligence application and a similarity solution model that uses an AI-recommended citation. Your compliance team can check the incoming regulatory alerts to determine if the citations or requirements apply to your organization.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Associating an AI-recommended citation to an open regulatory alert

Associate a citation to an open regulatory alert by using the GRC: Predictive Intelligence application and a similarity solution model that uses an AI-recommended citation. Your compliance team can check the incoming regulatory alerts to determine if the citations or requirements apply to your organization.

## Overview of associating a citation to a regulatory alert

Traditionally, if you had a subscription license, you could download a citation from a third-party provider or create a citation from an authority document by using Compliance Workspace.

**Note:** An authority document is a document that contains the external regulations, such as the laws, regulations, and standards, that your organization must comply with.

A citation is a passage or an expression from an authority document that your business must comply with. It’s an individual requirement within an authority document.

Now, you can use AI and machine learning \(ML\) to train a similarity solution model that automatically suggests which citations to add to the regulatory alerts. The citations are based on a confidence score that indicates the level of confidence that a prediction is correct. A higher score means that the match has a higher probability of being correct.

The Governance, Risk, and Compliance: Predictive Intelligence application uses AI and ML to make the GRC application adding citations smarter. These suggestions are based on a confidence score that is based on the recommended citation.

A user with the sn\_compliance\_admin role must train the solution definition after they install the GRC: Predictive Intelligence application with its dependencies. A user with the ml\_admin role can also customize the solution definition. This modification is based on the data in the \[`sn_complaince_citation`\] and the \[`sn_grc_reg_change_reg_feed`\] table. If you have the sn\_compliance\_admin role, you can select how frequently you want to refresh the data that you use to retrieve your similarity results. For more information about solution definitions, see [https://servicenow.com/docs/bundle/xanadu-customer-service-management/page/product/customer-service-management/reference/similar-cases-solution-definitions.html](https://servicenow.com/docs/bundle/xanadu-customer-service-management/page/product/customer-service-management/reference/similar-cases-solution-definitions.html).

## Key benefits of associating a citation to a regulatory alert

By associating an AI-recommended citation to an open regulatory alert, your organization gets the following key benefits:

-   Enhanced regulatory compliance mapping for effective reporting.
-   Reduced manual effort by your compliance team to identify and discover citations that are mapped to the incoming regulatory alerts.

## What you see when associating an AI-recommended citation card to a regulatory alert

When you use AI to associate a recommended citation card to a regulatory alert, you see the following details:

-   The confidence score of the recommended citation.
-   The citation name and authority document name that links with the citation and authority. You can open the links in separate windows.
-   An option to ignore the recommendation.
-   An option to associate the recommendation.
-   The history icon that enables you to view the history of actions that were taken on the regulatory alert, including the dates when the recommendations were added or ignored by your users.

