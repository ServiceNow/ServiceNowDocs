---
title: Impact categories and ratings
description: Impact categories are the types of an impact that you can assess during a business impact analysis. The BCM administrator of an organization is responsible for defining the impact categories and the timeframe during which an organization may experience a downtime. This information is used to determine the recovery time objective and recovery point objective of the assets.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Impact categories and ratings

Impact categories are the types of an impact that you can assess during a business impact analysis. The BCM administrator of an organization is responsible for defining the impact categories and the timeframe during which an organization may experience a downtime. This information is used to determine the recovery time objective and recovery point objective of the assets.

## Broad classification of the impact categories

When a business service, process, or application experiences downtime due to a disruptive event, its impact can be classified in various broad categories:

-   Legal impact: Classified as an impact with legal implications such as a civil lawsuit or fines that result from a service disruption.
-   Regulatory impact: Classified as an impact due to a change in the existing regulation or the introduction of a new policy.
-   Reputation impact: Classified as an impact to the brand image and reputation of a company.
-   Revenue impact: Classified as an impact due to financial losses or low revenues.
-   Workforce impact: Classified as an impact of a disruptive event on the workforce. For example, a company experiences an increased attrition rate and low employee morale post the pandemic.

## Impact categories in BCM

With the BCM administrator role, you can view the impact categories that are installed with demo data and set up new impact categories in the **Impact categories** module of the BCM application. The example shows the impact categories that are installed with demo data in an instance.

![BIA impact categories that are installed with demo data.](../image/bia-impact-categories.png)

## Configuration of an impact category

The BCM administrators can configure or modify the impact categories by adding key information about the impact. The example shows the configuration details of an impact category in an instance.

![Details of the legal impact category.](../image/configure-impact-category-for-bia.png)

The BCM administrators can configure the details of a new impact category:

-   **Name**

    Classification of the downtime impact for your service, process, or applications through an appropriate name such as Legal or Reputational impact.

-   **Contributes to**

    Selection of whether the impact contributes to recovery time objective or recovery point objective.

-   **Applicable timeframes**

    Timeframe specification for the impact category.

-   **Maximum RTO value**

    Maximum RTO value for the impact category.

-   **Description**

    Description field for the impact category.

-   **Helper text**

    Helper text that provides a hint to users on how to respond to the assessment questions. The helper text is then displayed for the user in the business impact analysis record. In the example, "Select an estimated time for each impact level" is the helper text for the impact category.

    ![Helper text in the Impact Rating record.](../image/imact-category-helper-text.png)


## Impact category configuration by BCM administrators

For more information on how to configure an impact category with the sn\_bcm.admin role, see [Configure impact category for BIA](../task/configure-impact-category-uib-ws.md).

## Impact ratings in BCM

If you have the BCM administrator role, you can view the impact ratings that are installed with demo data and define specific impact ratings in the **Impact ratings** module. The following example shows the impact ratings that are installed with demo data for an impact category.

![Impact ratings that are installed with demo data.](../image/configure-impact-category-for-bia.png)

The impact ratings for an impact category are shown in the example.

![Impact ratings for an impact category.](../image/question-text.png)

## Configuration of an impact rating

The BCM administrators can configure details of an impact rating for the business impact analysis:

-   **Name**

    Unique name to the impact rating.

-   **Impact Category**

    Classification of the impact category that the impact rating is associated with.

-   **Value**

    Unique numerical value to each impact rating. The same value can not be reused for any other impact rating in the BCM application.

-   **Tolerable**

    Option for enabling the RTO impact as tolerable. This check box appears only if the impact category contributes to the recovery time objective.

-   **Description**

    Description about the impact rating.

-   **Question text**

    Question text in the Impact Rating record for the recovery time objective of an impact category. The revised question is then displayed in the RTO assessment form of the business impact analysis record.


## Impact rating configuration by the administrators

For more information on how to configure an impact rating with the sn\_bcm.admin role, see [Configure impact ratings](../task/configure-impact-rating-uib-ws.md).

**Parent Topic:**[Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md)

