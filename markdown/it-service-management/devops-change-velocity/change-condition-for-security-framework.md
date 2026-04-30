---
title: Change policies based on security summary tables
description: You can use the security conditions that are available in the base system or customize them based on your requirement.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional info - Veracode, Veracode, Integrate, DevOps Change Velocity, IT Service Management]
---

# Change policies based on security summary tables

You can use the security conditions that are available in the base system or customize them based on your requirement.

The vulnerability severity conditions are present in the **Fetch Risk Sonar Security and Incident data** action in the **DevOps Gather Change Policy Data** subflow of the DevOps Default Change Request flow. ![Fetch Risk Sonar Security and Incident data action](../image/severity-condition-sec.png)

If the severity condition is classified as **HIGH** or **VERY HIGH** from Veracode or Checkmarx, then the change request is automatically rejected.

If you are an upgrading customer and you want to customize the conditions with any additional security data or change the existing conditions, you must update the script in the **Fetch Risk Sonar Security and Incident data** action in the change flow. Ensure that you are referring to the **Application Vulnerability Scan Summary Details \(sn\_vul\_app\_vul\_scan\_summary\_details\)** table in the script when you customize. For more information, see [Security scan results](security-tool-framework.md).

**Parent Topic:**[Veracode integration with DevOps Change Velocity](../concept/veracode-integration-with-devops-change-velocity.md)

