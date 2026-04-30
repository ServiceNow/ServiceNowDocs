---
title: Integrating EcoVadis with Third-party Risk Management
description: Integrating EcoVadis into your third-party risk management program can enhance your ability to assess and mitigate risks associated with sustainability and corporate social responsibility \(CSR\). By leveraging EcoVadis' comprehensive sustainability ratings, you can gain detailed insights into the environmental, ethical, and social practices of your third parties.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Integrating EcoVadis with Third-party Risk Management

Integrating EcoVadis into your third-party risk management program can enhance your ability to assess and mitigate risks associated with sustainability and corporate social responsibility \(CSR\). By leveraging EcoVadis' comprehensive sustainability ratings, you can gain detailed insights into the environmental, ethical, and social practices of your third parties.

## Configuring the Vendor Risk Management integration with the EcoVadis application

The following pre-requisite configurations are required to use the Vendor Risk Management integration with the EcoVadis application.

-   Activate the Vendor Risk Management integration with EcoVadis application \[com.sn\_app\_grc\_ecovadis\]. To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

-   Create a connection and authenticate your credentials with EcoVadis for more information, see [Create an EcoVadis connection and configuration](../task/tprm-config-connection-ecovadis.md).
-   Request EcoVadis ratings using the EcoVadis website. After the request is accepted, scores will become available in TPRM. For more information on the EcoVadis website, see [https://support.ecovadis.com/hc/en-us](https://support.ecovadis.com/hc/en-us).

**Note:** You can customize the system properties for EcoVadis. For more information, see [Customize system properties for EcoVadis integration](../task/tprm-config-properties-ecovadis.md).

## EcoVadis integration actions

As part of the EcoVadis integration with TPRM, you can Fetch and view risk intelligence scores including theme scores and scorecards from EcoVadis.

For more information, see [Fetch and view EcoVadis scores](../task/tprm-ecovadis-scores.md).

The following example shows the theme scores and scorecard link that you can view after fetching scores.

![EcoVadis risk intelligence score record.](../image/ecovadis-score-example.png "Example of EcoVadis Risk intelligence score record")

The following example shows a company's sustainability performance across four key areas: environment, labor practices, ethics, and sustainable procurement. It provides a detailed breakdown of the company's strengths and areas for improvement, along with a final overall score out of 100.

![Scorecard example showing a detailed breakdown of a company's strengths and areas for improvement, along with a final overall score.](../image/scorecard-example.png "Example of EcoVadis scorecard")

**Note:** Confirm that all third parties that you want to assess using EcoVadis has a website listed as part of their third-party record. EcoVadis confirms that a third party is registered by referencing the website URL.

-   **[Create an EcoVadis connection and configuration](../task/tprm-config-connection-ecovadis.md)**  
Create a connection to fetch and update scores from EcoVadis to help ensure that your risk and theme scores remain current when using Third-party Risk Management.
-   **[Customize system properties for EcoVadis integration](../task/tprm-config-properties-ecovadis.md)**  
You can optionally customize the default values of the sn\_ecovadis.token\_uri and sn\_ecovadis.score\_uri system properties. These properties manage tokens and access risk scores from EcoVadis when using Third-party Risk Management.
-   **[Fetch and view EcoVadis scores](../task/tprm-ecovadis-scores.md)**  
Retrieve current scores and scorecards from EcoVadis on demand or at a set frequency of time using Third-party Risk Management. Customizing settings for the EcoVadis Fetch Score Scheduler can help you get the latest scores when you need them.

**Parent Topic:**[Integrating TPRM with other applications](integrating-with-tprm.md)

