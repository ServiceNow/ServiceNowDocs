---
title: App Readiness and Compliance Report
description: App Engine Admins can use the App Readiness and Compliance Report dashboard to check if the apps they’re creating are ready to go live.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [AEMC \(App Engine Management Center\)]
breadcrumb: [Managing requests using AEMC, Managing app development using the App Engine Management Center, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# App Readiness and Compliance Report

App Engine Admins can use the App Readiness and Compliance Report dashboard to check if the apps they’re creating are ready to go live.

App Engine Admins can use the App Readiness and Compliance Report dashboard within the App Engine Management Center \(AEMC\) to verify that the apps that they’re creating are fully prepared for a live launch. This dashboard provides detailed insights from the Product Instance scans and helps to identify any issues or requirements that must be addressed before the app goes live, facilitating a smooth and compliant deployment process.

![App Readiness and Compliance Report Dashboard](../image/app-readiness-report-dashboard.png)

## Testing and Validation Categories for the Readiness Score

The readiness score evaluates the following categories of testing and validation:

-   **Readiness Score**

    The readiness score serves as an indicator for the overall validation checks. It provides a comprehensive assessment of how well a system or product meets the required standards across various categories.

-   **Manageability**

    Checks for effective management and maintenance practices, including configuration, customization, and change management.

-   **Security**

    Identifies vulnerabilities by assessing access controls, password policies, encryption, and security compliance.

-   **User Experience**

    Evaluates UI performance, app responsiveness, and accessibility to provide a smooth user experience.

-   **Upgradeability**

    Confirms readiness for ServiceNow upgrades by validating deprecated features and potential breakpoints.

-   **Performance**

    Identifies system bottlenecks, optimizing database performance, script efficiency, and load responsiveness.

-   **Test failure count**

    Shows the number Instance scan checks that failed to run.


**Note:**

-   You can also visit the AEMC Readiness Instance table in **All** &gt; `sn_aemc_readiness_instance` to view the historical information about checks. Remember that this table retains data for the last three months and any older data are archived.
-   You can create or modify checks, for instance scans in the **All** &gt; **Instance Scans** &gt; **Suites** &gt; **Best Practices- Parent**.

## Run a new app readiness report

To run a new app readiness report, select the **Run new report** button in the dashboard. After generating a report, you can see the readiness status of the app. You can also check issues in detail by selecting **More data available**.

**Parent Topic:**[Managing requests using AEMC](manage-aemc-requests.md)

