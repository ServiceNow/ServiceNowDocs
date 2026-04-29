---
title: Connect to a provider
description: Complete the registration process to establish a connection to the provider instance.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Connect to a provider

Complete the registration process to establish a connection to the provider instance.

## Before you begin

-   Role required: admin
-   Run the **Key Management** &gt; **Health \(Diagnostics\)** to ensure that the Key Management Framework health check has passed. Your administrator must have the sn\_kmf.admin and sn\_kmf.cryptographic\_manager roles to access the health diagnostics. If your administrator does not have access, follow the instructions in [Assign Key Management Framework roles](https://www.servicenow.com/docs/access?context=assign-kmf-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US) to grant the required roles.

## About this task

Before proceeding, the provider should have requested the contact details of an admin to set as the main point of contact on their registration record. This designated contact person will receive an email either from the provider's instance or directly from the provider's admin, containing a registration link. Clicking on this link will generate a Provider Connection record in your consumer instance. The following steps assume that you have already clicked the registration link.

## Procedure

1.  Select the **Connect to Provider** link sent in the provider's registration email or follow the link given to you directly by the provider’s admin.

    This link will generate the Provider connection record.

    **Note:** The consumer admin completing the registration process must be the named contact on the provider’s registration task or an admin in the provider's instance. Registration will fail during the OAUTH authentication step if attempted by another user.

2.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Provider Connections**.

3.  On the Provider Connection form in the consumer instance, select the name of the Company that the provider is associated with and select **Save**.

    After you save the provider connection record, the state changes to Awaiting Validation while the pre-onboarding scan suite runs validation checks on the background.

    -   If all validation checks pass, the state changes to Validated.
    -   If any validation checks fail, the state changes to Validation Failed. A banner appears at the top of the provider connection record indicating that one or more pre-onboarding suite checks did not pass, along with a link to the Health Dashboard. Review the Health Dashboard to fix the issues. When the all the issues are resolved, the connection automatically moves to Validated.
4.  Select **Connect to Provider** in the Provider connection record page.

    The **Connect to Provider** button is not available if there are any unresolved validation errors. Resolve all pre-onboarding scan issues before proceeding.

5.  Select **Authenticate** when the Service Exchange registration message appears.

    The OAuth authentication page appears.

6.  Select **Allow** and then select **Submit** to proceed with the registration.

    You are redirected to the Registration task where you can view the state. When registration is completed, a connection is established between the provider and the consumer instances, and the registration task State is set to **Closed Complete** on the provider's instance.


If the state is **Validation Failed**, you must resolve all issues identified during the pre-onboarding checks.

1.  Select the **Health Dashboard** link in the Validation Failed banner at the top of the Provider Connection record.
2.  Review and resolve all the pre-onboarding scan issues.

    After all issues are resolved, the state automatically changes to Open and the registration process resumes.


**Related topics**  


[Service Exchange Center](../concept/se-se-center.md)

[Instance scan checks](../concept/service-bridge-v2-scan-checks.md)

[Register a Service Exchange consumer](service-bridge-v2-onboarding.md)

